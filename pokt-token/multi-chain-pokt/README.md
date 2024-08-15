---
hidden: true
---

# Multi-Chain POKT

$POKT exists on a growing number of L1s and L2s thanks to POKT's Multi-Chain Bridge.

The POKT multi-chain smart contract was audited by [Nethermind](https://github.com/pokt-network/pocket-contracts/blob/cb4b5bb7a7bc9c24e63ddde66f7914185f0b4295/audits/NM0245\_XPOKT.pdf) and can be found on the following chains and DeFi platforms:

<table><thead><tr><th width="133">Chain</th><th width="246">Contract</th><th>Official Liquidity Pools</th></tr></thead><tbody><tr><td>Ethereum</td><td>0x764A726d9ceD0433A8D7643335919dEb03a9a935</td><td><a href="https://app.uniswap.org/explore/pools/ethereum/0x2979E18a7C2086192dB05B97cE180A3647402595">https://app.uniswap.org/explore/pools/ethereum/0x2979E18a7C2086192dB05B97cE180A3647402595</a></td></tr><tr><td>Base</td><td>0x764A726d9ceD0433A8D7643335919dEb03a9a935</td><td></td></tr><tr><td>Solana</td><td>6CAsXfiCXZfP8APCG6Vma2DFMindopxiqYQN4LSQfhoC</td><td></td></tr></tbody></table>

## How to bridge $POKT?

To go from POKT on POKT Network to another chain, you can follow the following steps.

1. First you need to bridge native POKT from POKT Network to wPOKT on Ethereum using the [wPOKT Bridge](../../welcome/usdpokt-token/bridging/wrapped-pokt-wpokt/wrapping-walkthrough.md). wPOKT is a dedicated wrapped token used for entering or exiting the native POKT blockchain.
2. Once you hold wPOKT on Ethereum, you can then convert to POKT on other chains using the [Multi-Chain Bridge](https://bridge.pokt.network).
   1. NOTE: You can not go directly from wPOKT to Solana do to technical limitations. First convert wPOKT to POKT on an EVM chain (like Ethereum), then you can bridge to Solana.
