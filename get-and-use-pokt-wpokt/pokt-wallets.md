# POKT Wallets

Before buying any POKT, you should ensure you know how to store it safely.

In this section, we’ll describe some different wallets that can store and manage POKT:

* [Pocket Wallet](pokt-wallets.md#pocket-wallet)
* [Pocket Ledger Wallet](pokt-wallets.md#pocket-ledger-wallet)
* [SendWallet](pokt-wallets.md#sendwallet)
* [NodeWallet](pokt-wallets.md#nodewallet)

### Pocket Wallet <a href="#pocket-wallet" id="pocket-wallet"></a>

You can use the [official wallet web app](https://wallet.pokt.network/) to create and manage your wallet.

#### Create wallet <a href="#create-wallet" id="create-wallet"></a>

To create a POKT wallet with the official Pocket wallet web app You can use the [official wallet web app](https://wallet.pokt.network/) to create your wallet.

1. Click “Create”

<figure><img src="../.gitbook/assets/ClickCreate.png" alt=""><figcaption></figcaption></figure>

1. Enter a unique passphrase

<figure><img src="../.gitbook/assets/CreatePassword.png" alt=""><figcaption></figcaption></figure>

&#x20;

{% hint style="warning" %}
Warning

The passphrase unlocks/decrypts an encrypted version of the private key that is stored in a Key File. Make sure to store your passphrase safely, if you lose it you will not be able to unlock your Key File.
{% endhint %}

3. Download the Key File by clicking the blue download icon and click Continue to open your account

<figure><img src="../.gitbook/assets/CreateSaveKeyFile.png" alt=""><figcaption></figcaption></figure>

_If you accidentally click Back, as long as you downloaded your Key File and saved your passphrase, you will now be able to import your new wallet._



{% hint style="warning" %}
&#x20;Warning

Make sure to store your Key File safely, if you lose it you will only be able to use the Private Key method to import your wallet anywhere. The Key File is the more secure method of importing your wallet since it is encrypted by your passphrase.
{% endhint %}

4. Click “Reveal Private Key” then enter your passphrase again to reveal the Private Key for your wallet.

<figure><img src="../.gitbook/assets/CreateRevealPrivateKey.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/ClickRevealKey.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
&#x20;**Warning**

Store your Private Key safely. This will be a second method for you to import your wallet in the event that you lose your Key File or passphrase. However, this is also less secure than the Key File since the Key File is encrypted by your passphrase.
{% endhint %}

{% hint style="warning" %}
**Warning**

Never reveal your Private Key to anyone. If someone has access to your Private Key, they have full access to all the funds. The only application that should ever need access to your Private Key is a wallet.
{% endhint %}

### Backup wallet <a href="#backup-wallet" id="backup-wallet"></a>

It is important that you back up your Key File, passphrase, and private key securely. There are two considerations when choosing a backup method:

* **Theft Prevention**: make sure no-one else can access your Key File, passphrase, or private key
* **Loss Prevention**: make sure you don’t lose access to your Key File, passphrase, or private key

The most secure way to prevent theft is to store your Key File, passphrase, and private key on a USB drive (or other secure external drive), disconnected from any online “cloud” service or internet-connected computer that can be hacked.

{% hint style="info" %}
**Info**

POKT is planned to have Ledger support soon, which will provide more advanced functionality than a USB drive.
{% endhint %}

For extra-secure theft prevention, you should split the Key File, passphrase and private key across separate drives and password-protect these drives so that anyone who gets their hands on a drive can’t access the contents. For extra loss prevention, you should make multiple copies of these drives and store them in different locations, such as a personal safe, the safe of a trusted family member, and a bank safety deposit box.

Once you have created your backups, delete all traces of the Key File, passphrase and private key from the hard drive of the computer you used for account setup. To ensure deletion, consider using software such as sDelete (Windows) or shred followed by rm (Linux).

{% hint style="info" %}
**Info**

For more convenience, you may consider using a password manager that can store encrypted files. Just be mindful that you risk theft if your master password is compromised and you risk loss if you forget your master password.
{% endhint %}

#### Import wallet <a href="#import-wallet" id="import-wallet"></a>

The [official wallet web app](https://wallet.pokt.network/) has three methods of importing your wallet. The Key File is a more secure method of importing your wallet than the Private Key, since the Key File is encrypted by your passphrase.

<figure><img src="../.gitbook/assets/ClickImport.png" alt=""><figcaption></figcaption></figure>

**Key File import**

Click Select File then choose your `keyfile.json` from your local file explorer.

Enter your Key File passphrase, which you specified when creating the wallet.

Click Import.

<figure><img src="../.gitbook/assets/ImportKeyFile.png" alt=""><figcaption></figcaption></figure>

**Private key import**

Enter your Private Key.

Create a temporary passphrase that will secure your session until you log out of the wallet. This is a measure to prevent anyone with access to your computer from stealing your funds.

<figure><img src="../.gitbook/assets/ImportPrivateKey.png" alt=""><figcaption></figcaption></figure>

#### **Ledger wallet import**

Click Connect.

Select the account index you would like to use in Pocket Wallet.

Click Unlock.

<figure><img src="../.gitbook/assets/ImportLedgerAccount.png" alt=""><figcaption></figcaption></figure>

#### Now supporting Unstoppable Domains in the POKT Wallet. <a href="#now-supporting-unstoppable-domains-in-the-pokt-wallet" id="now-supporting-unstoppable-domains-in-the-pokt-wallet"></a>

Users can now send transactions to an Unstoppable Domain from a POKT Wallet address. Create an Unstoppable Domain for your wallet [here](https://unstoppabledomains.com/).

For guidance on how to send a transaction with a UD, check out this video:

### Pocket Ledger Wallet <a href="#pocket-ledger-wallet" id="pocket-ledger-wallet"></a>

Before You Start, Make Sure:

* You’ve [initialized](https://support.ledgerwallet.com/hc/en-us/articles/360000613793) your Ledger Device.
* Ledger Live is [ready to use](https://support.ledger.com/hc/en-us/articles/4404389606417-Download-and-install-Ledger-Live).
* The latest version of the [Pocket Nano app](https://github.com/ledgerhq/app-pocket) is installed.

#### Install the Pocket App <a href="#install-the-pocket-app" id="install-the-pocket-app"></a>

* Open **My Ledger** in Ledger Live.
* Connect and unlock your Ledger Device.
* If asked, follow the onscreen instructions and **Allow My Ledger**.
* Find Pocket in the app catalog.
* Click the Install button.
  * An installation window will appear.
  * Your device will display Processing…
  * The app installation is confirmed.
* Close Ledger Live

#### Connecting to Pocket Wallet <a href="#connecting-to-pocket-wallet" id="connecting-to-pocket-wallet"></a>

* Connect and unlock your Ledger Device.
* Open the Pocket App on your Ledger Device.
* Open the [Pocket Wallet ](pokt-wallets.md#pocket-wallet)in a browser.
* Follow [Account Import](pokt-wallets.md#ledger-wallet-import) instructions above.
* Use the Pocket Wallet as normal.

#### Signing Transactions with Ledger <a href="#signing-transactions-with-ledger" id="signing-transactions-with-ledger"></a>

* Transactions generated in the Pocket Wallet must be signed using the Nano device buttons.
* The Ledger app provides a series of prompts which can be used to verify the transaction details prior to signing or rejecting.

### SendWallet <a href="#sendwallet" id="sendwallet"></a>

[SendWallet](https://sendwallet.net/) is a browser-based Pocket Network wallet built by [SendNodes](https://sendnodes.io/).

<figure><img src="../.gitbook/assets/sendwallet.jpg" alt=""><figcaption></figcaption></figure>

SendWallet features:

* Import using the Key File from a Pocket Wallet
* Import using a private key
* Generate multiple wallet addresses with one account
* Recovery phrase to recover wallet
* Full screen option

You can try SendWallet by downloading the browser extension for [Chrome](https://chrome.google.com/webstore/detail/sendwallet/adganlhbinonbpfiehjjpmklkbghkaio?hl=en) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/sendwallet/).

For more information on how to use SendWallet, see the [SendWallet documentation](https://docs.sendwallet.net/).

### NodeWallet <a href="#nodewallet" id="nodewallet"></a>

[NodeWallet](https://docs.decentralizedauthority.com/nodewallet) is an open source, browser-based Pocket Network wallet built by Decentralized Authority, the team behind [Node Pilot](https://nodepilot.tech/). NodeWallet was started as a [Pocket Open Priority (POP)](https://forum.pokt.network/t/allocated-priority-new-wallet/4657/5?u=shane) project from the Pocket Network Foundation.

[![](https://nodepilot.tech/wp-content/uploads/2023/10/NodeWallet-Splash.png)](https://nodepilot.tech/wp-content/uploads/2023/10/NodeWallet-Splash.png)

NodeWallet features:

* Universal Seed Phrase Importer (Import seed phrases from other popular wallets, so you don’t need a POKT specific seed phrase for POKT addresses)
* Key file and private key importer
* Generate multiple wallet addresses with one account
* [wPOKT Bridge](https://wpokt.network/) compatible
* [Open source](https://github.com/decentralized-authority/nodewallet) with plugin design to make it contributor friendly for adding features and expanding to other networks
* Utilizes Argon2 + AES-256 GCM for quantum secure encryption

Install NodeWallet directly from the Chrome Store [here](https://chrome.google.com/webstore/detail/nodewallet/ilibmadejjooogcniiomgdgbojkmlbim).

For more information on how to use NodeWallet, see the [NodeWallet documentation](https://docs.decentralizedauthority.com/nodewallet).
