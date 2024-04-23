# Part 4 - Proxy Configuration

### SSL Setup <a href="#setup-ssl" id="setup-ssl"></a>

Pocket requires that nodes have an SSL ([Secure Sockets Layer](https://www.cloudflare.com/learning/ssl/what-is-ssl/)) certificate for secure communications. SSL is a layer of security that sits on top of TCP/IP ([Internet Protocol Suite](https://en.wikipedia.org/wiki/Internet\_protocol\_suite)). It’s used to encrypt the data sent between a client and a server. To use SSL, you need to have a certificate and a key. Thankfully, getting an SSL certificate and key is straightforward and free.

To get a certificate, we’ll be using[ Let’s Encrypt](https://letsencrypt.org/), which is a service that issues SSL certificates for free. We’ll also be using software called[ certbot](https://certbot.eff.org/) to register, install, and renew the certificate.

#### Registering an SSL certificate <a href="#registering-an-ssl-certificate" id="registering-an-ssl-certificate"></a>

We installed certbot in a previous step; now we’ll use it to request a certificate.

To get a certificate, we’ll need to use the certbot command with the following options:

* `--register-unsafely-without-email`: This option is required to get a certificate without an email address.
* `--agree-tos`: This option is required to agree to the Let’s Encrypt Terms of Service.
* `--nginx`: This option is required to use the Nginx plugin.
* `--no-redirect`: This option is required to disable the redirect to the Let’s Encrypt website.
* `--domain`: This option is required to specify the domain name.

Here’s an example of how to request a certificate. Just replace `$HOSTNAME` with the DNS name of your node:

CommandResponse

```bash
sudo certbot --nginx --domain $HOSTNAME --register-unsafely-without-email --no-redirect --agree-tos
```

The output from this command should confirm that the certificate was successfully registered.

#### Testing your certificate <a href="#testing-your-certificate" id="testing-your-certificate"></a>

To be sure, you’ll want to test that the certificate is working.

The command that certbot provides to test the auto-renewal of the certificate also confirms that the certificate is working. You can run it using the following command:

CommandResponse

```bash
sudo certbot renew --dry-run
```

The resulting output should confirm that the certificate is working.

### Configure Nginx <a href="#configure-nginx" id="configure-nginx"></a>

Nginx is a web server. We installed it in a previous step but now we need to reconfigure it.

Nginx uses config files to define servers and routes for incoming requests. For Pocket nodes, Nginx needs to relay public requests to a local HTTP server that Pocket Core is running. This is referred to as the proxy. We’ll also need to proxy requests made by the Pocket CLI. For example, when we run the command pocket query height, the CLI makes an HTTP request to the node’s local HTTP server.

**Config files**

The Nginx configuration files we’re interested in are located in the /etc/nginx/sites-available/ directory. In that directory there's a default configuration file named "default." This is the configuration that comes with the Nginx install, but we’ll be creating our own for our node.

To configure Nginx:

1.  Confirm the name of your SSL certificate:

    ```bash
    sudo ls /etc/letsencrypt/live/
    ```
2.  Create a new config file with nano:

    ```bash
    sudo nano /etc/nginx/sites-available/pocket
    ```
3.  Add the following code, making sure to change the hostname values (`pokt001.pokt.run`) to your node’s DNS hostname in the three places found below:

    ```
    server {
        listen 80 default_server;
        listen [::]:80 default_server;

        root /var/www/html;

        index index.html index.htm index.nginx-debian.html;

        server_name _;

        location / {
            try_files $uri $uri/ =404;
        }
    }

    server {
        add_header Access-Control-Allow-Origin "*";
        listen 80 ;
        listen [::]:80 ;
        listen 8081 ssl;
        listen [::]:8081 ssl;

        root /var/www/html;

        index index.html index.htm index.nginx-debian.html;

        server_name pokt001.pokt.run;

        location / {
            try_files $uri $uri/ =404;
        }

        listen [::]:443 ssl ipv6only=on;
        listen 443 ssl;

        ssl_certificate /etc/letsencrypt/live/pokt001.pokt.run/fullchain.pem;
        ssl_certificate_key /etc/letsencrypt/live/pokt001.pokt.run/privkey.pem;

        include /etc/letsencrypt/options-ssl-nginx.conf;
        ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem;

        access_log /var/log/nginx/reverse-access.log;
        error_log /var/log/nginx/reverse-error.log;

        location ~* ^/v1/client/(dispatch|relay|challenge|sim) {
            proxy_pass http://127.0.0.1:8082;
            add_header Access-Control-Allow-Methods "POST, OPTIONS";
            allow all;
        }

        location = /v1 {
            add_header Access-Control-Allow-Methods "GET";
            proxy_pass http://127.0.0.1:8082;
            allow all;
        }
    }
    ```
4. Save the change with `Ctrl+O`.
5. Exit nano with `Ctrl+X`.
6.  Stop Nginx with:

    ```bash
    sudo systemctl stop nginx
    ```
7.  Disable the default configuration:

    ```bash
    sudo rm /etc/nginx/sites-enabled/default
    ```
8.  Enable our new configuration:

    ```bash
    sudo ln -s /etc/nginx/sites-available/pocket /etc/nginx/sites-enabled/pocket
    ```
9.  Start Nginx:

    ```bash
    sudo systemctl start nginx
    ```

### Enable UFW <a href="#enable-ufw" id="enable-ufw"></a>

We’re almost done, but before we finish we’ll make our server more secure by setting firewall rules to limit network exposure. The[ Uncomplicated Firewall](https://wiki.ubuntu.com/UncomplicatedFirewall) (UFW) is a security tool that makes configuring the firewall simple. We’ll use it to disable unnecessary ports.

**Ports you need to open**

To run  a Pocket node, you’ll need to open the following ports on the server:&#x20;

* `22`: SSH
* `80`: HTTP
* `443`: HTTPS
* `8081`: For the Pocket HTTP API
* `26656`: For the Pocket RPC API

#### Use UFW to disable unnecessary ports <a href="#use-ufw-to-disable-unnecessary-ports" id="use-ufw-to-disable-unnecessary-ports"></a>

To use UFW to configure the firewall:

1.  Enable UFW. When prompted, press `y` to confirm:

    ```bash
    sudo ufw enable
    ```
2.  Set the default to deny all incoming connections:

    ```bash
    sudo ufw default deny
    ```
3.  Allow the SSH port:

    ```bash
    sudo ufw allow ssh
    ```
4.  Allow port 80:

    ```bash
    sudo ufw allow 80
    ```
5.  Allow port 443:

    ```bash
    sudo ufw allow 443
    ```
6.  Allow port 8081:

    ```bash
    sudo ufw allow 8081
    ```
7.  Allow port 26656:

    ```bash
    sudo ufw allow 26656
    ```

That’s it for the UFW setup. To confirm that only the necessary ports are open, run the following command:

```bash
sudo ufw status
```

Now you're ready to proceed to the final steps.
