# The Economics

POKT is the lifeblood of the POKT Network ecosystem. It coordinates all actors within the ecosystem and drives the core utility of the network.



<figure><img src="../.gitbook/assets/spaces_HVZ3BQcmJhVmXh7fy6xP_uploads_qoRt8gKnYOtnXs06l6W4_The Growth Flywheel (1).webp" alt=""><figcaption></figcaption></figure>

## The role of POKT within the protocol

* Node runners currently need to stake at least 15,000 POKT to operate a POKT node. We expect this requirement to change once Shannon is deployed to mainnet later this year.
* Validators must stake enough POKT to become one of the 1,000 validators, a protocol-defined cap. The current “validator threshold” is 75,100 POKT [as per POKTscan](https://poktscan.com/). (Validators might be replaced by Sequencers in the Shannon protocol upgrade).
* Every gateway routing traffic to POKT Network’s decentralized network of nodes must pay a “Gateway Operator Fee” of $0.00000085 per relay, as per the [protocol burn proposal](https://forum.pokt.network/t/pip-29-burn-gateway-burn/4401) passed on 16 May 2023. Paid in POKT, these fees are burned. Approximately 6.5m POKT were burned over the 12 months since burning began in May 2023, an average of 540,000 per month. (For live metrics, refer to [https://pokt.money](https://pokt.money/).)

{% hint style="info" %}
There is a flywheel effect in place for POKT's economics as more gateways drive more relays to the network, requiring gateways to buy more POKT, which is then burned. More relays incentivize more node runners to join the network to earn rewards, and with more node runners with better QoS, more gateways, in turn, are incentivized to bring more of their business to POKT Network, which keeps the flywheel turning.
{% endhint %}

## Supply and minting of POKT

The original genesis distribution of POKT was 649,984,998 POKT distributed as follows:

<figure><img src="../.gitbook/assets/spaces_HVZ3BQcmJhVmXh7fy6xP_uploads_git-blob-6eeecf874a2a2d67ee7180acc072f0eae8cf63d1_Screenshot 2024-01-03 at 16 (1).webp" alt=""><figcaption></figcaption></figure>

## Most POKT now circulating

The vast majority of POKT's supply is now liquid and circulating, with most tokens - almost 1b (and counting) of the current supply - distributed permissionlessly since POKT Network’s mainnet launch on 28 July 2020. The distribution mechanism - POKT Network’s version of a fair launch à la Bitcoin - was to issue POKT rewards to those staking POKT as node runners to serve RPC requests and as validators to secure the network.

POKT's latest supply schedule is dictated by [ARR (Accelerating the Road to Revenue)](https://forum.pokt.network/t/pup-32-accelerating-the-road-to-revenue-arr/4494), a proposal that passed on 5 July 2023. This schedule targets an average mint rate of 220,000 POKT per day**,** which varies based on the 7-day trailing average of relay requests to the network as per [ACCURATE](https://forum.pokt.network/t/pup-29-a-cadence-change-to-updates-of-rttm-adjustment-for-target-emissions-accurate/3777), a proposal adopted on 25 January 2023, which includes the calculator used to update the mint rate weekly.

All POKT minted in each block is distributed as follows:

* 85% to the node runners for serving the relays
* 5% to the validators for securing the network
* 10% to the DAO treasury

## Total and Circulating supply of POKT

See [**here**](https://pokt-api.liquify.com/pokt/api/v1/supply/total) for the **total supply of POKT.**&#x20;

You can calculate the total supply of POKT by adding the monetary base figure on [POKTscan's supply tab](https://poktscan.com/explore?tab=supply) to the [DAO Treasury](https://poktscan.com/explore?tab=governance). For supply change figures, see [POKT.Money](https://pokt.money/).

Some exchanges and investors include the [DAO Treasury](https://poktscan.com/explore?tab=governance) and the [main PNF Treasury wallet](https://poktscan.com/node/186afc505903e7c7aa97d5f7f1c555111e2ae2ce) as part of **the circulating supply of POKT**, as neither sum is subject to any legal vesting provisions (apart from the small amount of POKT granted to PNF staff). For those that follow this line of reasoning, the total supply of POKT is the same as the circulating supply.

Other data providers, such as POKTscan, calculate the circulating supply of POKT by deducting the [DAO Treasury](https://poktscan.com/explore?tab=governance) from the total supply, as all DAO Treasury spending is subject to prior approval from the DAO. See [here](https://poktscan.com/explore?tab=supply) for POKTscan's calculation of the circulating supply, which they refer to as POKT’s “monetary base.” Or see [**here**](https://pokt-api.liquify.com/pokt/api/v1/supply/circulating) for a public endpoint showing the same.

For community reference, all of the DAO- and PNF-controlled wallets are listed below:

* the [DAO Treasury](https://poktscan.com/explore?tab=governance)
* the [DAO ERA Budget wallet](https://poktscan.com/account/4e67bdb7d099c8a754b22c852a9fe140b7d47849) (containing all POKT to fund upcoming [ERA expenses](https://forum.pokt.network/t/pep-60-enabling-responsible-allocation-of-budget-era-budget/4443))&#x20;
* the [DAO's wPOKT SAFE on Ethereum](eth:0x2f16615234827eE4dF14d02d40C24E6a258dD360) (used to launch the wPOKT pool)
* the [DAO's Gnosis SAFE on Ethereum](https://app.safe.global/transactions/history?safe=eth:0x7bAAf6cAEE858929a68a98a70a428b8BEB4d4093) (used to pay DAO contributors)
* the [main PNF POKT Treasury wallet](https://poktscan.com/node/186afc505903e7c7aa97d5f7f1c555111e2ae2ce)
* [PNF's Gnosis SAFE on Ethereum](https://app.safe.global/transactions/history?safe=eth:0x963810F5D0FB29286156C833FcF30ab760D5Bad8) (used to pay contractors and agencies).

## Supply projections for POKT

The main drivers of the supply of POKT are:

1. The amount of POKT paid to node runners, which is projected to drop in POKT terms as the price of POKT increases (to target an approximate USD profit margin for node runners, though any update requires a DAO vote).
2. The number of relays and the price charged to gateways for each relay served since every relay results in the burning of POKT.

The graphs below illustrate the potential supply growth for POKT over time and how that impacts the total supply of POKT. Please note that these projections are based on a USD/POKT price of $0.15 and 60b relays by day in 2028.



<figure><img src="../.gitbook/assets/spaces_HVZ3BQcmJhVmXh7fy6xP_uploads_git-blob-132a5f527c0f9fe00e572549efa5124bfc1ee3f4_image (1) (1).webp" alt=""><figcaption><p>Total supply for POKT over time based on such assumptions</p></figcaption></figure>

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F9frYjAjtKqZHrIgdCbj2%2Fuploads%2FVkvKrQjmErUCRX7VHcwS%2Fspaces_HVZ3BQcmJhVmXh7fy6xP_uploads_git-blob-a9cd805eb5ed6137e2cc873b760a9083736deda9_image%20(2).webp?alt=media&#x26;token=841fd9d7-20eb-46af-a8ad-9b3335f03bfa" alt=""><figcaption><p>Supply growth for POKT based on an indicative number of relays and price per POKT</p></figcaption></figure>

Others may be more optimistic or conservative in their approach to the variables underlying these graphs. We invite the community to fork the numbers in [this spreadsheet](https://docs.google.com/spreadsheets/d/1y4ZpBBR\_ytbp5EGqYc6Hsg5vw6CSeXn\_KEuKOMRHIbM/edit?usp=sharing) to create their own projections based on their assumptions for the price of POKT, the number of POKT needed to reward node runners, the number of relays, and the Gateway Operator Fee.
