# Part 2 - Software Installation

### 1. Install Dependencies

At this point you should be logged in via SSH as the `pocket` user that we set up in a previous step. Before we install the Pocket software, we need to update the existing system packages and add a few dependencies:&#x20;

#### Updating system packages

1.  Update the repository index with the following command:

    ```bash
    sudo apt update
    ```
2.  Update the distribution with the following command:

    ```bash
    sudo apt dist-upgrade -y
    ```

After the update completes, we're ready to install the dependencies.

#### Installing dependencies

Some of the following dependencies might already be installed so if one of the them exists, you can just move on to the next one.

**git**

```bash
sudo apt-get install git -y
```

**build tools**

```bash
sudo apt-get install build-essential -y
```

**curl**

```bash
sudo apt-get install curl -y
```

**file**

```bash
sudo apt-get install file -y
```

**nginx**

```bash
sudo apt install nginx -y
```

**certbot**

```bash
sudo apt install certbot -y
```

**python3-certbot-nginx**

```bash
sudo apt-get install python3-certbot-nginx -y
```

**jq**

```bash
sudo apt install jq -y
```

### 2. Install Go

After installing the dependencies above, there is one more we'll need to add, and that's Go tools. Go (sometimes referred to as "Golang") is the programming language that the Pocket software was written in.

We could install Go using `apt`, but we want to get the latest stable version which probably isn't available by default in the `apt` repository. So, we'll use the steps below to install Go.

1.  Make sure you're in the `pocket` home directory.

    ```bash
    cd ~
    ```
2.  Find the latest version of Go from [https://golang.org/dl/](https://golang.org/dl/) then download it with the following command. (Make sure to change the link below to point to the correct version of Go.)

    ```bash
    wget https://go.dev/dl/go1.22.2.linux-amd64.tar.gz
    ```
3.  Extract the archive:

    ```bash
    sudo tar -xvf go1.22.2.linux-amd64.tar.gz
    ```
4.  Set permissions on the extracted files:

    ```bash
    sudo chown -R pocket ./go
    ```
5.  Add Go to the `PATH` environment variable

    ```bash
    echo 'export PATH=$PATH:$HOME/go/bin' >> ~/.profile
    ```
6.  Set the `GOPATH` and `GOBIN` environment variables:

    ```bash
    echo 'export GOPATH=$HOME/go' >> ~/.profile
    ```

    ```bash
    echo 'export GOBIN=$HOME/go/bin' >> ~/.profile
    ```
7.  Reload your `.profile`:

    ```bash
    source ~/.profile
    ```
8.  Verify the installation:

    ```bash
    go version
    ```

    Ensure this outputs the correct version number. If this doesn't work, try logging out and logging back in.
9.  Verify the `GOPATH` and `GOBIN` variables are set correctly:

    ```bash
    go env
    ```

### 3. Install Pocket

After verifying you have the latest stable version of Go, we're ready to install the Pocket software.

We'll be downloading [Pocket Core](https://github.com/pokt-network/pocket-core/) from GitHub and then compiling it with Go to get it fully installed.

To download and install Pocket Core, do the following:

1.  Create a project directory:

    ```bash
    sudo mkdir -p $GOPATH/src/github.com/pokt-network
    ```
2.  Move to the project directory:

    ```bash
    cd $GOPATH/src/github.com/pokt-network
    ```
3.  Clone the Pocket Core repository:

    ```bash
    sudo git clone https://github.com/pokt-network/pocket-core.git
    ```
4.  Move to the code directory:

    ```bash
    cd pocket-core
    ```
5.  Checkout the latest released version. You can find this by going to the Pocket Core releases on GitHub.

    ```bash
    sudo git checkout tags/<pocket-version>
    ```

    **Note:** You may see a warning about being in a "detached HEAD" state. This is normal.
6.  Build project code:

    {% code overflow="wrap" %}
    ```bash
    go build -o $GOPATH/bin/pocket $GOPATH/src/github.com/pokt-network/pocket-core/app/cmd/pocket_core/main.go
    ```
    {% endcode %}
7.  Test that the build succeeded:

    ```
    pocket version
    ```

That’s it for the software installation. Now let’s move on to the Pocket Core configuration.
