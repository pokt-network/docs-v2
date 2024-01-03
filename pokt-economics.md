---
description: >-
  POKT is the lifeblood of the POKT Network ecosystem. It coordinates all actors
  within the ecosystem and drives the core utility of the network.
---

# POKT Economics

## The role of POKT within the protocol

* Node runners must currently stake at least 15,000 POKT to run a POKT node. (This is expected to increase as part of the updates to the economics following the output of the [Economics R\&D work with BlockScience](https://forum.pokt.network/t/v1-economics-and-governance-r-d-keystone/4712)).&#x20;
* Validators must stake enough POKT to become one of the 1,000 validators, a protocol-defined cap. The current “validator threshold” is 75,100 POKT [as per POKTscan](https://poktscan.com/). (A Sequencer will replace validators in the new Shannon protocol upgrade).&#x20;
* Every Gateway routing traffic to POKT Network’s decentralised network of nodes must pay a “Gateway Operator Fee” of $0.00000085, as per the [protocol burn proposal](https://forum.pokt.network/t/pip-29-burn-gateway-burn/4401) passed on 16 May 2023. As per [POKTscan](https://poktscan.com/explore?tab=supply), the weekly burn has ranged from 108,000 (as projected for December 2023) to 1.2m  POKT per month. The main drivers of the weekly burn are the number of relays and the price of POKT.&#x20;

{% hint style="info" %}
There is a flywheel effect in place for POKT's economics as more gateways drive more relays to the network, requiring gateways to buy more POKT, which is then burned, and more relays incentivize more node runners to join the network to earn more rewards, and with more node runners with better QoS, more gateways are in turn incentivized to bring more of their business to POKT Network, which keeps the flywheel turning.
{% endhint %}

## Supply and minting of POKT

The original genesis distribution for POKT was 649,984,998 POKT distributed as follows:

<figure><img src=".gitbook/assets/Screenshot 2024-01-03 at 16.36.10.png" alt=""><figcaption><p>POKT Genesis distribution on 28/7/2020</p></figcaption></figure>

The vast majority of all of POKT's supply is now liquid and circulating, with most tokens - almost 1B (and counting) of the current supply - distributed permissionlessly since POKT Network’s main net launch on 28 July 2020. The mechanism to achieve this distribution - POKT Network’s version of a fair launch - occurred similarly to Bitcoin by distributing POKT rewards to those staking POKT as node runners to serve RPC requests and validators to secure the network. \


The **latest supply schedule** for POKT is dictated by [the ARR proposal](https://forum.pokt.network/t/pup-32-accelerating-the-road-to-revenue-arr/4494) that passed on 5 July 2023. This schedule targets an average mint rate of 220,000 POKT per day, which varies based on the 7-day trailing number of relay requests to the network as per the [Accurate proposal](https://forum.pokt.network/t/pup-29-a-cadence-change-to-updates-of-rttm-adjustment-for-target-emissions-accurate/3777) (which includes the calculator used to update the mint rate each week).&#x20;

\
**All POKT minted in each block is distributed as follows:**

* &#x20;85% to the node runners doing the work to serve each relay request sent to the network by the gateways,
* 5% to the validators securing the network, and&#x20;
* 10% to the DAO treasury.

The current figure for the **total supply of POKT** is calculated by adding the monetary base figure on POKTscan's supply tab - see [here](https://poktscan.com/explore?tab=supply) - to the current DAO Treasury as per [this link](https://poktscan.com/explore?tab=governance).

On the other hand, the **circulating supply of POKT** is calculated by deducting the following from the total supply:&#x20;

* the [DAO Treasury](https://poktscan.com/explore?tab=governance), and
* &#x20;the balances of the current PNF Treasury wallets:
  * `186afc505903e7c7aa97d5f7f1c555111e2ae2ce`,
  * `6c2e570489dd1362a450c0cdc0b658cc0c1fe1fa` and
  * `258f98b18dff36c58155caf6092f242760d40967`.

## Supply projections for POKT

The main drivers on the supply of POKT are:

1. The amount of POKT paid out to node runners, which will continue to reduce in POKT terms as the price of POKT increases (to target an approximate USD profit margin for node runners),
2. The number of relays and the price charged to gateways for each relay served as every relay results in the burning of POKT

You can see below for some graphs illustrating the potential supply growth for POKT over time and how that impacts the total supply for POKT.&#x20;

<div>

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption><p>Supply growth for POKT based on an indicative number of relays and price per POKT</p></figcaption></figure>

 

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption><p>Total supply for POKT over time based on such assumptions</p></figcaption></figure>

</div>

These are fairly high-level assumptions and we welcome the community to fork the numbers in [this spreadsheet](https://docs.google.com/spreadsheets/d/1y4ZpBBR\_ytbp5EGqYc6Hsg5vw6CSeXn\_KEuKOMRHIbM/edit?usp=sharing) to create their own assumptions based on their projections for the price of POKT, the number of POKT needed to mint to node runners, the number of relays, as well as the Gateway Operator Fee.&#x20;

