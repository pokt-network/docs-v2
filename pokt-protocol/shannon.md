---
description: Becoming the API to the Open Internet
---

# Shannon

### Contents&#x20;

1. [About Shannon ](shannon.md#about-shannon)
2. [Shannon Roadmap ](shannon.md#shannon-roadmap)

### About Shannon&#x20;

Shannon is the next generation of the POKT protocol and takes its utility to new heights with a modular design. PNF and the protocol team will be releasing developer tools, research, bounty programs, and community initiatives that correlate with Shannon's Testnet phases.\
\
Built with the [Cosmos SDK](https://docs.cosmos.network/), Shannon is backed by [CometBFT](https://cometbft.com/)'s PoS consensus engine and uses the[ Rollchains module](https://github.com/rollchains/tiablob#celestia-blob-cosmos-sdk-module) to leverage Celestia's data availability layer.

### What does it achieve?

Shannon accelerates key changes that are already taking place at POKT Network.

{% tabs %}
{% tab title="Permissionless Gateways" %}
Shannon takes our Gateway strategy for decentralized demand-side access and makes the creation of Gateways fully permissionless, enabling rapid volume growth by becoming a fully open and universal RPC infra layer.
{% endtab %}

{% tab title="Improved Scalability" %}
Shannon removes the remaining limitations on the protocol’s scalability and brings interoperability with key ecosystems in Web3, opening us up fully to the rest of our world.
{% endtab %}

{% tab title="New Usescases" %}
Shannon takes the Data Source expansion that we started in Morse and introduces tokenomics that enable monetization for the Data Sources themselves. This accelerates our expansion into new use cases and provides a new sustainable incentive model for open Data Sources of all kinds.
{% endtab %}
{% endtabs %}

{% hint style="info" %}
_Shannon transforms POKT Network from a leading DePIN (Decentralized Physical Infrastructure)_ _with full supply-side decentralization and an empowered community into the first true sharing economy for any open data-source._&#x20;
{% endhint %}

***

## Launch Roadmap&#x20;

You can access the latest version of Shannon's Roadmap [here](https://github.com/orgs/pokt-network/projects/144?query=is%3Aopen+sort%3Aupdated-desc).​

### Testnet Launch

The public Testnet is structured in phases, each providing specific areas of focus and unique milestones. The main goal of each phase is to break, learn, iterate and rebuild stronger with community involvement.&#x20;

A rewards system for contributors including new [bounties](../community/start-contributing/bounties.md) will be announced shortly. We encourage you to help identify areas for improvement. POKT has a proud tradition of community contributions that substantially improved the protocol, and we hope to draw on this throughout the Testnet phases.

<figure><img src="../.gitbook/assets/testnetphases.png" alt=""><figcaption></figcaption></figure>

#### Our Priorities for launch

<details>

<summary><strong>Limits of permissionless demand</strong></summary>

One of the core reasons we are moving from \`_Morse_\` to \`_Shannon_\` is to enable the scalability needed for permissionless demand.\
\
The team is working on tooling so we can load-test it and start finding potential bottlenecks. We are excited to share what we believe is one of the best E2E load-testing frameworks across the entire industry.

</details>

<details>

<summary><strong>Governance Parameters</strong></summary>

In order to migrate existing functionality and add new functionality, we need to add support for Governance parameters that are compliant with the new Cosmos SDK. We are hard at work on getting this done ASAP.

</details>

<details>

<summary><strong>Explorers &#x26; Faucets</strong> </summary>

In order for anyone to interact with or explore the new network, we need visibility tooling. Luckily, using the Cosmos SDK opens up access to existing tools and our community is actively working on co-opting those!

</details>

<details>

<summary><strong>Images &#x26; Binaries</strong> </summary>

No one wants to build from scratch every time. We'll integrate with the [Cosmos Operator ](https://github.com/strangelove-ventures/cosmos-operator)to provide binaries and images for every POKT Shannon actor so that it's seamless for existing operators to test the new network as well as for onboarding new ones.

</details>

A re-genesis will occur in the coming weeks to launch the official Public Testnet. However, early adopters who aren’t afraid of bugs can start getting familiar with deploying and running using this [docker-compose guide](https://github.com/pokt-network/poktroll-docker-compose-example) today! Bounties and incentives for improving tooling for Public Testnet will be announced soon.

## Mainnet Launch

Every design decision is focused on allowing POKT Network to optimize core utility, abstracting away anything that doesn’t directly benefit its DePIN business, while enabling Shannon to be modular by nature and to natively integrate and interoperate with other ecosystems in Web3.

We hoped to be able to abstract away the validation layer entirely and deploy fully as a rollup on Celestia’s emerging tech, but we built pragmatically in a way that gave us a fallback to a new Cosmos SDK that was a strong alternative (full analysis [here](https://www.pokt.network/blog/rolling-into-the-modular-future) released in September 2023).&#x20;

Celestia’s ecosystem is developing rapidly but, in this instance, not rapidly enough for us to launch as a full rollup. POKT Network will therefore launch with the Cosmos SDK backed by CometBFT's PoS consensus engine, which will enable it to use Rollchains and settle its blocks on other data availability layers such as Celestia for added security. These changes will set back our Mainnet timeline but will allow interoperability with both IBC and Celestia ecosystems. The Rollchains module will be added in later testnet phases.

Here is the updated timeline, with Mainnet launch now targeted for later this year.

<figure><img src="../.gitbook/assets/Frame 2.png" alt=""><figcaption></figcaption></figure>

## Jump into Shannon Today

To allow developers, hobbyists, and tinkerers to truly participate in Shannon on a protocol level, **the team has built a complete LocalNet environment, able to be deployed in 2 commands**. This LocalNet is complete with validators, gateways, suppliers, monitoring, and other tools, and is able to automatically reload on new changes in the code or configurations.

This is the first protocol deployment tooling to be this simple in the Web3 space, and we are excited to release it now to the community with this [Quickstart Guide](https://dev.poktroll.com/develop/developer\_guide/quickstart) and a [Complete Walkthrough](https://drive.google.com/file/d/1Tfrd32ubDCmWz2ztje-NJ2qGH9tsPfj8/view?usp=sharing) video.&#x20;

As always, you can follow our [Github Roadmap](https://github.com/orgs/pokt-network/projects/144?query=is%3Aopen+sort%3Aupdated-desc) and very soon (not yet) apply for tasks with the community label [here](https://github.com/orgs/pokt-network/projects/144?query=is%3Aopen+sort%3Aupdated-desc).&#x20;

POKT Network is an open-source project and you can find our active repo for Shannon [here](https://dev.poktroll.com/).

***

> ### A Note From PNF
>
> Shannon is not only the next era of the POKT Protocol, but also the next stage of growth for the POKT Network community. This evolution in technology will also see the evolution of our community, as it will enable more developers to engage directly with the protocol and contribute in meaningful ways. We are excited for what is next. Please be on the lookout for new materials and initiatives rolling out in the coming weeks.
