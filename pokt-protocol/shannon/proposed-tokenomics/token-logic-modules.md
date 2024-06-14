# Token Logic Modules

Shannon brings a groundbreaking innovation into the POKT network by introducing Token Logic Modules (TLMs). These TLMs are housed within the tokenomic module, a custom component developed using the Cosmos SDK. Each TLM represents a distinct economic model with its own unique logic.

The beauty of this system is that it allows for multiple TLMs to operate concurrently, each applied to different ServiceIDs within the network. This means that POKT can have a fully modular tokenomics system, tailored to the specific needs and dynamics of each service. This is a revolutionary development for a DePIN utility token to scale into completely different markets, each with their own needs.

For example, here's how different TLMs can be applied to different ServiceIDs:

\| ServiceID types 👉

| TLMs 👇           | Blockchain RPC (per relay) | AI Inferencing | Blockchain RPC (per compute cost) | Future data services? |
| ----------------- | -------------------------- | -------------- | --------------------------------- | --------------------- |
| Relay Mint = Burn | ✅                          | -              | -                                 | ❔                     |
| Source Boost      | ✅                          | ✅              | ✅                                 | ❔                     |
| Supplier Boost    | ✅                          | -              | -                                 | ❔                     |
| Compute Tokens    | -                          | ✅              | ✅                                 | ❔                     |
| Future TLMs?      | ❔                          | ❔              | ❔                                 | 🤔                    |

TLM goals:

1. <mark style="color:red;">`Introduce new tokenomic models to the network at a ServiceID level, rather than a global level.`</mark>
2. <mark style="color:red;">`Allow multiple TLMs to interact together to form a complete tokenomics system.`</mark>

With TLMs, we can create novel economic models for new services, such as AI or other data types added to POKT in the future. We can also address immediate tokenomics needs by having three TLMs simultaneously at play for blockchain RPC:

1. <mark style="color:red;">`Relay Burn = Mint`</mark>
2. <mark style="color:red;">`Source Boost`</mark>
3. <mark style="color:red;">`Supplier Boost`</mark>

#### 1. RMB (Relay Burn = Mint) TLM

This is the base mechanism we want in Shannon, where when 1 POKT burned on the demand side, 1 POKT or less is minted on the supply side. Having the mint be less then 1 POKT is how POKT can become deflationary.

|                         | Demand      | Supply      |
| ----------------------- | ----------- | ----------- |
| Burn / Mint             | Burn 1 POKT | Mint 1 POKT |
| Permissionless          | ✅           | ✅           |
| Staking APR             | -           | .08%\*      |
| Self Dealing Mitigation | No need     | No need     |

\*\* Staking APR here is based off POKT doing \~400M relays a day.\*

The 1 POKT minted is distributed to the network actors according to parameters determined by the DAO. For example: 👇

| Suppliers        | Sources | DAO | Validators |
| ---------------- | ------- | --- | ---------- |
| 70% ( .08% APR ) | 15%     | 10% | 5%         |

The issue with just the RMB TLM is that it has a low staking APR with the current number of relays on the network (\~400M a day). This low return could negatively affect our staking ecosystem. Low relays also yield low rewards for Sources.

To boost Source rewards and Supplier APR, we can enable two other TLMs to work in tandem: Source Boost TLM and Supplier Boost TLM.

#### 2. Source Boost TLM

Source Boost is a TLM that provides an increased mint reward for Sources. This incentivizes foundations, indexers, AI, or new data sources to partner with POKT to generate revenue.

Source Boost is designed with these primary goals:

1. <mark style="color:red;">`Source Incentivization`</mark> - Provide meaningful rewards to incentivize Sources.
2. <mark style="color:red;">`Progressive reduction w/ Relays`</mark> - Progressively reduce the percentage of rewards coming from Source Boost as relays increase and more rewards come from RBM.
3. <mark style="color:red;">`Progressive phasing w/ RBM`</mark> - Progresively phase out once there are enough relays to fully sustain Sources with RMB TLM.

Here is an example of what the rewards can be for some Source with RMB TLM and Source Boost TLM with today’s relays (\~400M a day). Note the % coming from each TLM:

|          | Relays per day | Rewards from RMB TML                          | Reward from Source Boost TLM                    | Total Monthly Reward                                                               | Annual Reward                             |
| -------- | -------------- | --------------------------------------------- | ----------------------------------------------- | ---------------------------------------------------------------------------------- | ----------------------------------------- |
| Polygon  | 100M           | $519 <mark style="color:orange;">(25%)</mark> | $1,548 <mark style="color:orange;">(75%)</mark> | <mark style="color:green;">$2,067</mark> <mark style="color:orange;">(100%)</mark> | <mark style="color:green;">$24,821</mark> |
| Ethereum | 74M            | $383 <mark style="color:orange;">(25%)</mark> | $1,159 <mark style="color:orange;">(75%)</mark> | <mark style="color:green;">$1,543</mark> <mark style="color:orange;">(100%)</mark> | <mark style="color:green;">$18,528</mark> |
| Solana   | 15M            | $98 <mark style="color:orange;">(24%)</mark>  | $305 <mark style="color:orange;">(76%)</mark>   | <mark style="color:green;">$404</mark> <mark style="color:orange;">(100%)</mark>   | <mark style="color:green;">$4,855</mark>  |
| DFKchain | 10M            | $55 <mark style="color:orange;">(24%)</mark>  | $172 <mark style="color:orange;">(76%)</mark>   | <mark style="color:green;">$228</mark> <mark style="color:orange;">(100%)</mark>   | <mark style="color:green;">$2,737</mark>  |

With POKT currently on-boarding half a dozen gateways and the growth opportunities that come from permissionless gateways in Shannon, substantial relay growth is expected. Here's how relay growth to \~5B relays a day would look for Champions 👇

<table><thead><tr><th></th><th>Relays per day</th><th>Reward from Mint = Burn</th><th>Reward from Champion Boost</th><th>Total Monthly Reward</th><th width="100">Annual Reward</th></tr></thead><tbody><tr><td>Polygon</td><td>1.1B</td><td>$5,964 <mark style="color:green;">(44%)</mark></td><td>$7,539 <mark style="color:green;">(56%)</mark></td><td><mark style="color:green;">$13,504</mark> (100%)</td><td><mark style="color:green;">$162,133</mark></td></tr><tr><td>Ethereum</td><td>849M</td><td>$4,404 <mark style="color:orange;">(36%)</mark></td><td>$7,723 <mark style="color:orange;">(64%)</mark></td><td><mark style="color:green;">$12,128</mark> (100%)</td><td><mark style="color:green;">$145,615</mark></td></tr><tr><td>Solana</td><td>217M</td><td>$1,127 <mark style="color:orange;">(26%)</mark></td><td>$3,135 <mark style="color:orange;">(74%)</mark></td><td><mark style="color:green;">$4,263</mark> (100%)</td><td><mark style="color:green;">$51,187</mark></td></tr><tr><td>DFKchain</td><td>121M</td><td>$632 <mark style="color:orange;">(25%)</mark></td><td>$1,857 <mark style="color:orange;">(75%)</mark></td><td><mark style="color:green;">$2,490</mark> (100%)</td><td><mark style="color:green;">$29,898</mark></td></tr></tbody></table>

Notice that while the rewards increase with relays, RMB TLM starts to represent a larger percentage of the Source’s rewards. With these calculations, Source Boost would be completely turned off by 20B relays a day.

With the Source Boost TLM, POKT provides real revenue opportunities, enabling Sources to build substantial businesses off their software.

#### 3. Supplier Boost TLM

The Supplier Boost TLM provides POKT’s staking community with a competitive APR while also putting POKT on a path to deflation. It is important to construct the incentives in such a way that good behavior is rewarded, and safeguards against gaming or self-dealing. The primary objectives of Supplier Boost are:

1. <mark style="color:red;">`Even Distribution`</mark> - Distribute rewards evenly amongst all nodes in a session to prevent rewards from being directed to specific nodes.
2. <mark style="color:red;">`Supplier Penalization`</mark> - Ensure nodes are legitimate by penalizing nodes that do not serve a meaningful amount of relays.
3. <mark style="color:red;">`Path to deflation`</mark> - Align rewards with inflation goals, progressively leading POKT to deflation.
4. <mark style="color:red;">`Phase out as relays increase`</mark> - Gradually reduce the proportion of rewards derived from Supplier Boost as relay numbers increase and more rewards originate from RMB.

