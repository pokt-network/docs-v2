# Technical Overview

The Shannon upgrade will enter POKT Network into the full Cosmos ecosystem by being built entirely off the Cosmos SDK. Our live protocol, called Morse, was developed as a fork of Tendermint in 2020. At the time, Tendermint wasn't robust enough to handle all the features POKT Network needed at launch. Features like claim and proof lifecycle had to be hard coded into Tendermint, leaving POKT Network outside of compatibility with the rest of the Cosmos Ecosystem.

Thanks to the technical advancements of the Cosmos SDK over the past several years, POKT Network is now able to be a full member and receive all it’s benefits.

### Technical Stack Comparison

|                              | Morse (the live protocol)                 | Shannon (future upgrade)                      |
| ---------------------------- | ----------------------------------------- | --------------------------------------------- |
| App-specific SDK             | Custom (2020 Cosmos SDK inspired)         | Mainline Cosmos SDK                           |
| Consensus                    | Tendermint (2020 Fork)                    | Mainline CometBFT                             |
| Claim & Proof Tree Structure | Merkle Sum Index Tree (using Cosmos IAVL) | Sparse Merkle Sum Trie (using Celestia’s SMT) |

### Shannon Code Base

The Shannon upgrade is built entirely on the Cosmos SDK. This will provide POKT Network with several new benefits (<mark style="color:red;">`MICE`</mark>):

1. <mark style="color:red;">`Modularity`</mark> - The modular design and established framework of the Cosmos SDK make it more inviting for external contributors to join POKT Network.
2. <mark style="color:red;">`Interoperability`</mark> - Through IBC, POKT Network can settle or publish data to other DA networks such as native L1s, Celestia, EigenDA, etc…
3. <mark style="color:red;">`Compatability`</mark> - POKT Network is compatible with any tools or services that are compatible with the Cosmos SDK (wallets, explorers, exchanges, bridges, etc).
4. <mark style="color:red;">`Extensibility`</mark> - Any new features added to the Cosmos SDK in the future can be incorporated into POKT Network.

While our live protocol, Morse, is relatively isolated, <mark style="color:red;">`MICE`</mark> grew out through experimentation, so the Shannon protocol will be compatible with the larger web3 ecosystem through the Cosmos SDK and IBC. 🐭

