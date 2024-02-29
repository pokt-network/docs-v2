# Hold POKT In a Wallet

Before buying any POKT, you should ensure you know how to store it safely.

In this section, we’ll describe some different wallets that can store and manage POKT:

* [Pocket Wallet](hold-pokt-in-a-wallet.md#pocket-wallet)
* [Pocket Ledger Wallet](hold-pokt-in-a-wallet.md#pocket-ledger-wallet)
* [SendWallet](hold-pokt-in-a-wallet.md#sendwallet)
* [NodeWallet](hold-pokt-in-a-wallet.md#nodewallet)

### Pocket Wallet <a href="#pocket-wallet" id="pocket-wallet"></a>

You can use the [official wallet web app](https://wallet.pokt.network/) to create and manage your wallet. This wallet is a strong choice for holding your POKT but has limited interaction with other websites and no staking functionality. Step-by-step guide available [here](hold-pokt-in-a-wallet.md#pocket-wallet).

### Pocket Ledger Wallet <a href="#pocket-ledger-wallet" id="pocket-ledger-wallet"></a>

This is the ledger integration for the Pocket Wallet. It is currently the only way to interact with Ledger, although this may change over the coming months. Step-by-step guide available here.

### SendWallet <a href="#sendwallet" id="sendwallet"></a>

[SendWallet](https://sendwallet.net/) is a browser-based Pocket Network wallet built by [SendNodes](https://sendnodes.io/) that is available as a browser extension for [Chrome](https://chrome.google.com/webstore/detail/sendwallet/adganlhbinonbpfiehjjpmklkbghkaio?hl=en) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/sendwallet/).

SendWallet includes a custodial staking option.

SendWallet features:

* Import using the Key File from a Pocket Wallet
* Import using a private key
* Generate multiple wallet addresses with one account
* Recovery phrase to recover wallet
* Full screen option

For more information, see the [SendWallet documentation](https://docs.sendwallet.net/).

### NodeWallet <a href="#nodewallet" id="nodewallet"></a>

[NodeWallet](https://docs.decentralizedauthority.com/nodewallet) is an open source, browser-based Pocket Network wallet built by Decentralized Authority, the team behind [Node Pilot](https://nodepilot.tech/). NodeWallet was started as a [Pocket Open Priority (POP)](https://forum.pokt.network/t/allocated-priority-new-wallet/4657/5?u=shane) project from the Pocket Network Foundation.

NodeWallet is deploying a non-custodial staking option that will allow users to stake with any participating node operator in a non-custodial manner.

NodeWallet features:

* Universal Seed Phrase Importer (Import seed phrases from other popular wallets, so you don’t need a POKT specific seed phrase for POKT addresses)
* Key file and private key importer
* Generate multiple wallet addresses with one account
* [wPOKT Bridge](https://wpokt.network/) compatible
* [Open source](https://github.com/decentralized-authority/nodewallet) with plugin design to make it contributor friendly for adding features and expanding to other networks
* Utilizes Argon2 + AES-256 GCM for quantum secure encryption

Install NodeWallet directly from the Chrome Store [here](https://chrome.google.com/webstore/detail/nodewallet/ilibmadejjooogcniiomgdgbojkmlbim).

For more information on how to use NodeWallet, see the [NodeWallet documentation](https://docs.decentralizedauthority.com/nodewallet).

***

### Ledger

### Before You Start

* You’ve [initialized](https://support.ledgerwallet.com/hc/en-us/articles/360000613793) your Ledger Device.
* Ledger Live is [ready to use](https://support.ledger.com/hc/en-us/articles/4404389606417-Download-and-install-Ledger-Live).
* The latest version of the [Pocket Nano app](https://github.com/ledgerhq/app-pocket) is installed.

### Install the Pocket Wallet Web App <a href="#install-the-pocket-app" id="install-the-pocket-app"></a>

* Open **My Ledger** in Ledger Live.
* Connect and unlock your Ledger Device.
* If asked, follow the onscreen instructions and **Allow My Ledger**.
* Find Pocket in the app catalog.
* Click the Install button.
  * An installation window will appear.
  * Your device will display Processing…
  * The app installation is confirmed.
* Close Ledger Live

### Connect to Pocket Wallet <a href="#connecting-to-pocket-wallet" id="connecting-to-pocket-wallet"></a>

* Connect and unlock your Ledger Device.
* Open the Pocket App on your Ledger Device.
* Open the [Pocket Wallet ](hold-pokt-in-a-wallet.md#pocket-wallet)in a browser.
* Follow [Account Import](hold-pokt-in-a-wallet.md#ledger-wallet-import) instructions above.
* Use the Pocket Wallet as normal.

### Sign Transactions with Ledger <a href="#signing-transactions-with-ledger" id="signing-transactions-with-ledger"></a>

* Transactions generated in the Pocket Wallet must be signed using the Nano device buttons.
* The Ledger app provides a series of prompts which can be used to verify the transaction details prior to signing or rejecting.
