# Use a Public Endpoint

The POKT Network Foundation is funding free public endpoints as a public good, powered by [Nodies](use-a-gateway/nodies.md), POKT Network's second gateway. It's important to note that these endpoints are subject to dynamic throughput limits of around 15-25 requests-per-second (RPS). As such, they are suitable for wallet users, hackathon developers, or anyone sampling POKT's service, but heavier users seeking high-throughput service should explore [creating an account with a gateway](use-a-gateway/), or [self-hosting a gateway](../gateways/host-a-gateway/).

### Endpoints

| Network Name      | Endpoint URL                                                                                                                                                                           | ChainID | Symbol | Explorer    | URL                                                                          |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- | ------ | ----------- | ---------------------------------------------------------------------------- |
| Arbitrum          | [https://arb-pokt.nodies.app](https://arb-pokt.nodies.app)                                                                                                                             | 42161   | ARB    | Arbiscan    | [https://arbiscan.io](https://arbiscan.io)                                   |
| Avalanche Core    | [https://avax-pokt.nodies.app](https://avax-pokt.nodies.app)                                                                                                                           | 43114   | AVAX   | CChain      | [https://cchain.explorer.avax.network](https://cchain.explorer.avax.network) |
| Avalanche C-chain | [https://avax-pokt.nodies.app/ext/bc/C/](https://avax-pokt.nodies.app/ext/bc/C/rpc)                                                                                                    |         |        |             |                                                                              |
| Avalanche DFK     | [https://avax-pokt.nodies.app/ext/bc/q2aTwKuyzgs8pynF7UXBZCU7DejbZbZ6EUyHr3JQzYgwNPUPi/rpc](https://avax-pokt.nodies.app/ext/bc/q2aTwKuyzgs8pynF7UXBZCU7DejbZbZ6EUyHr3JQzYgwNPUPi/rpc) |         |        |             |                                                                              |
| BNB Smart Chain   | [https://bsc-pokt.nodies.app](https://bsc-pokt.nodies.app)                                                                                                                             | 56      | BNB    | Bscscan     | [https://bscscan.com](https://bscscan.com)                                   |
| Ethereum          | [https://eth-pokt.nodies.app](https://eth-pokt.nodies.app)                                                                                                                             | 1       | ETH    | Etherscan   | [https://etherscan.io](https://etherscan.io)                                 |
| Evmos             | [https://evmos-pokt.nodies.app](https://evmos-pokt.nodies.app)                                                                                                                         | 9001    | EVMOS  | EVM         | [https://evm.evmos.org](https://evm.evmos.org)                               |
| Fantom            | [https://fantom-pokt.nodies.app](https://fantom-pokt.nodies.app)                                                                                                                       | 250     | FTM    | Ftmscan     | [https://ftmscan.com](https://ftmscan.com)                                   |
| FUSE              | [https://fuse-pokt.nodies.app](https://fuse-pokt.nodies.app)                                                                                                                           | 122     | FUSE   | Explorer    | [https://explorer.fuse.io](https://explorer.fuse.io)                         |
| Gnosis Chain      | [https://gnosis-pokt.nodies.app](https://gnosis-pokt.nodies.app)                                                                                                                       | 100     | xDAI   | Blockscout  | [https://blockscout.com/poa/xdai](https://blockscout.com/poa/xdai)           |
| Kava Mainnet      | [https://kava-pokt.nodies.app](https://kava-pokt.nodies.app)                                                                                                                           | 2222    | KAVA   | Explorer    | [https://explorer.kava.io](https://explorer.kava.io/)                        |
| Klaytn            | [https://klaytn-pokt.nodies.app](https://klaytn-pokt.nodies.app)                                                                                                                       | 8217    | KLAY   | Scope       | [https://scope.klaytn.com](https://scope.klaytn.com)                         |
| Metis             | [https://metis-pokt.nodies.app](https://metis-pokt.nodies.app)                                                                                                                         |         |        |             |                                                                              |
| Optimism          | [https://op-pokt.nodies.app](https://op-pokt.nodies.app)                                                                                                                               | 10      | ETH    | Optimistic  | [https://optimistic.etherscan.io](https://optimistic.etherscan.io)           |
| Optimism Sepolia  | [https://op-sepolia-pokt.nodies.app](https://op-sepolia-pokt.nodies.app)                                                                                                               |         |        |             |                                                                              |
| Polygon           | [https://polygon-pokt.nodies.app](https://polygon-pokt.nodies.app)                                                                                                                     | 137     | MATIC  | Polygonscan | [https://polygonscan.com](https://polygonscan.com)                           |
| Polygon Mumbai    | [https://polygon-mumbai-pokt.nodies.app](https://polygon-mumbai-pokt.nodies.app)                                                                                                       |         |        |             |                                                                              |
| Harmony           | [https://hmyone-pokt.nodies.app](https://hmyone-pokt.nodies.app)                                                                                                                       |         |        |             |                                                                              |

### How to Add an Endpoint to MetaMask

To change your endpoint in MetaMask, follow these steps, filling in the appropriate fields from the table provided:

1. Click on the **Networks** drop-down menu, then select **Add Network**.
2. In the **Network Name** field, enter `<Network Name> POKT`.
3. For the **New RPC URL** field, copy and paste `<Endpoint URL>`.
4. (Optional) Enter `<ChainID>` in the **ChainID** field.
5. (Optional) Input `<Symbol>` in the **Symbol** field.
6. (Optional) Insert `<Explorer URL>` into the **Block Explorer URL** field.
7. Don't forget to save your changes.

> **Note**: If you encounter an error in MetaMask stating `Invalid number. Enter a decimal or '0x'-prefixed hexadecimal number`, simply leave the optional fields blank.
