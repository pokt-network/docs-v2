# Wrapping and Unwrapping FAQ

### What wallets are approved for wrapping POKT? <a href="#what-wallets-are-approved-for-wrapping-pokt" id="what-wallets-are-approved-for-wrapping-pokt"></a>

You can use: &#x20;

* [Ledger](https://www.ledger.com/)
* [NodeWallet](https://docs.decentralizedauthority.com/nodewallet)

What about the official POKT Wallet?

The official POKT wallet does not have built-in support for wPOKT, but you can import the official wallet to either of the supported options. For instructions on how to import see the documentation here (Ledger) and here (NodeWallet).&#x20;

### How can I swap my POKT for wPOKT?

{% hint style="warning" %}
Before getting started, note that the end-to-end wrapping process is expected to take \~30 mins, and that minting wPOKT will cost gas (in ETH).&#x20;
{% endhint %}

As wrapping POKT requires that you bridge your tokens from the POKT network to the Ethereum network, start by by connecting your Ledger or NodeWallet to the bridge.

* Prepare to mint your wPOKT by connecting your Ethereum wallet. Make sure your Ethereum wallet has some ETH for gas fees. If you don’t have enough ETH for gas, the bridge app will tell you.
* You will not be able to initiate the wrap transaction until you have connected both wallets.
* Specify the amount of POKT to wrap into wPOKT, then click Wrap.
* After \~30 minutes, if you’ve completed all the steps, you will receive your wPOKT.

{% hint style="info" %}
You will be required to sign 2 transactions: first to deposit your POKT, and then to mint your wPOKT. We recommend you keep the modal open and stay in the app until both transactions have been confirmed. If you leave the app before both transactions complete, they will remain pending until you return and finish them.

If the wPOKT isn’t in your wallet after 30 minutes, double check that you’ve completed both transactions.
{% endhint %}

### Why haven’t I received my wPOKT yet? <a href="#why-havent-i-received-my-wpokt-yet" id="why-havent-i-received-my-wpokt-yet"></a>

* **Where did my minting pop-up go?** If you navigate away, the pop-up will disappear until the 2nd transaction (minting) is ready to be proceed. If it’s not appearing, try refreshing your browser after the 30 min waiting period.
* **Are you looking in the right place?** First check that you’re looking at the correct blockchain. wPOKT lives on the Ethereum blockchain, so you will not see wPOKT in your Ethereum wallet unless you are connected to the Ethereum RPC. You can easily connect your wallet to the Ethereum RPC via Pocket Network using this [site](https://rpclist.info/). To cross-check, you can also search your ETH wallet address on [Etherescan](https://etherscan.io/) to see if the wPOKT balance appears there.
* **Have you waited long enough?** End-to-end wrapping of POKT usually takes about 30 minutes. However, in some cases, it may take up to an hour.
* **Have you added the wPOKT token address to MetaMask?** If your MetaMask wallet isn’t auto-populating the wPOKT address, you’ll need to add it manually. Follow the instructions [here](https://support.metamask.io/hc/en-us/articles/360015489031-How-to-display-tokens-in-MetaMask#h\_01FWH492CHY60HWPC28RW0872H). The wPOKT address is 0x67f4c72a50f8df6487720261e188f2abe83f57d7 and it should auto-populate once you've added it.

If you've followed all of the above steps but still don't see your tokens, please contact us for support at the [Help Desk channel](https://discord.com/channels/553741558869131266/1168923397842022571) on our Discord server.

### How can I unwrap my wPOKT back to POKT? <a href="#how-can-i-unwrap-my-wpokt-back-to-pokt" id="how-can-i-unwrap-my-wpokt-back-to-pokt"></a>

Unwrapping wPOKT requires that you bridge your tokens from the Ethereum network back to the POKT network.

End-to-end, the unwrapping process takes up to 30 mins.

* Prepare to burn your wPOKT by connecting your Ethereum wallet to the bridge. Make sure your Ethereum wallet has some ETH for gas fees. If you don’t have enough gas, the bridge app will tell you.
* Prepare to unwrap your POKT by connecting your Ledger, SendWallet, or NodeWallet.
* You will not be able to initiate the unwrap transaction until you have connected both wallets.
* Specify the amount of wPOKT tokens to unwrap into POKT tokens, then click Unwrap.
* After \~30 minutes, you should receive your POKT.

### Why haven’t I received my POKT yet? <a href="#why-havent-i-received-my-pokt-yet" id="why-havent-i-received-my-pokt-yet"></a>

* **Are you looking in the right place?** Make sure you are checking your POKT wallet for the balance, not your Ethereum wallet.
* **Have you waited long enough?** An end-to-end unwrap of POKT is expected to take approximately 30 minutes. If it has not been 30 minutes or it has only recently turned 30 mins, please try waiting a little longer.

If you have confirmed you’re looking in the right place and you have waited a little longer, but you still do not see your tokens, please contact us at our Discord [Help Desk channel](https://discord.com/channels/553741558869131266/1168923397842022571).

### Why does the bridge take up to 30 mins? <a href="#why-does-the-bridge-take-up-to-30-mins" id="why-does-the-bridge-take-up-to-30-mins"></a>

* **Pocket Network block times.** Pocket Network blocks complete every 15 minutes. Depending on when you sign the transaction, it may take up to 15 minutes for your transaction to appear on-chain.
* **Bridge validation time.** The wPOKT bridge verifies your request between chains. It takes up to 10 minutes to reach consensus and start a transaction on-chain.
* **Ethereum block times.** Ethereum blocks complete every 12 seconds. For large balances, it is common to have to wait for up to 32 blocks before proceeding with a transaction.
