---
description: >-
  This is the overview for Creds - an update to our governance system that is
  out for DAO consideration. It is under discussion and has not been approved at
  this time!
---

# Creds Overview

### TL;DR

POKT Network’s proposed governance system was built on three principles:

* Governance power cannot be bought, it must be earned.
* You earn governance power by driving impact, and it should grow with your impact.
* This requires a lot of thought “under the hood” but should be automated as much as possible to be frictionless for participants - you work to earn your governance, but you shouldn’t have to work hard to claim what you’ve earned.

### Why do we need this upgrade?

There are four main challenges with the current system (more info [here](https://forum.pokt.network/t/pgov1-evolving-pocket-s-governance-introducing-3d-governance/4698)):

* **Gaps in representation:** current paths are not appropriate for many stakeholders (investors, grantees etc) and outright exclude others (i.e. anons who cannot verify via discord selfies).
* **Inertia in representation: e**arning a vote takes a long time and once it is earned it persists even after you stop participating. In the last 12 months we only had \~5 new DAO voters.
* **Imbalances in representation:** it’s much easier to earn a vote for some types of stakeholders compared to others, so we get imbalances.
* **Manual processes:** the manual nature of the current system has left some feeling frustrated, having gone through the process of earning the vote.

### How do we define impact?

There are many different ways you can positively impact the project.

We look at impact in 3 areas, or “houses”:

* [**Builders**](https://forum.pokt.network/t/pgov5-builder-specification/4867)**:** drive impact by building the ecosystem and protocol. These people are shipping code, building products, winning RFPs, running experiments, and much more. They earn governance for these types of impact and hold significant weight (40% of total).
* [**Stakers**](https://forum.pokt.network/t/pgov6-staker-specification/4886)**:** drive impact by productively using the POKT token to support or secure the network. These people burn tokens as Gateways, stake POKT as Services or Validators, provide liquidity to our wPOKT pool, and much more. The network cannot operate without stake, so they too have significant weight (40% of total).
* [**Citizens**](https://forum.pokt.network/t/pgov4-citizenship-specification/4804)**:** drive impact by understanding and proliferating our mission, values, and vision. Every voter must show this base level of understanding. So every voter (Builder or Staker) must also be a Citizen. But barriers are low so it carries a low amount of governance power (20% of total).

Because any member of the community can earn power across any / all of these houses, we called the system ‘3D Governance’.

### How is that simple?

There are a couple of things you need to do at the start but, after that point, it is (mostly) dynamic and automated. No more manual actions, bottlenecks, or follow up.

Your governance power accrues automatically as you ship code, stake in LP pools, win an RFP or any of the many ways you can positively impact the project.

It will also fade gradually if you become inactive.

Here is the process:

1. **Create a Gitcoin Passport.** Retain your anonymity while we make sure that nobody can game the system with multiple identities.
2. **Create a digital ID on** [**mygateway.xyz**](http://mygateway.xyz) . Connect your wallet(s) and any other sites you wish to the Gateway protocol, they provide the infra for cred issuance and automations.
3. **Earn your Citizenship.** Complete 2 automated ‘quests’ and receive your Citizenship Cred to vote in the DAO.
4. **Automatically receive Builder Creds.** When you pass a proposal, complete a Socket, have a PR merged.. all of this will automatically be captured and issued to your ID or wallet.
5. **Automatically receive Staker Creds.** When you act as a custodial staker or liquidity provider your credentials are also automatically issued to you.
6. **Vote in Snapshot.** Exactly the same as today - to vote you simply use your ethereum wallet and vote. Your voting power is automatically calculated based on your Creds.

### Into the detail

As anyone knows who has ever built anything knows, simple is HARD and it has to be supported by a LOT of deep thought, detailed design, and careful execution.

This section is for those who want to dig in to that.

Perhaps the biggest challenge we wanted to tackle is to ensure that the system is capture resistant and that power is balanced correctly across individuals and groups.

This balance is achieved in part through the two elements of:

* Individual Voting Weight
* Collective Voting Weight

**Individual Voting Weight** recognises that all impact is not equal and creates the granularity needed for power to grow with your reputation.

For example, you might have:

* Weighting of 5 points for shipping a PR to one of the main POKT Network repos (because of the importance of this to the performance of the protocol).
* Weight of 1 point for being approved to open a Socket (plus another 1 point for keeping it open and self-reporting for two months).

While there are many more examples of this individual weighting, and many more ways to get reputation “Points”, each is just a representation of this same “impact = what?” question.

**Collective Voting Weight** sets constraints on how much voting power a collective group can have in the DAO. For example:

* We plan to give weight of 20% Citizens, 40% Builders and 40% Stakers at launch. As such, each group needs each other to reach a majority.
* Stakers represents all of demand, supply and liquidity. We plan to set the collective weights at 30% Gateways, 30% Liquidity providers and 40% Servicers & Validators at launch.

This is the full and complete set of collective voting weight constraints.

We also shared more information on the concept of [citizenship](https://www.pokt.network/blog/permissionless-does-not-equal-unrestricted-citizenship-and-the-boundaries-of-entry), [personhood](https://www.pokt.network/blog/the-personhood-module-in-pokt-dao), and this idea of [productive capital](https://www.pokt.network/blog/the-problem-isnt-capital-its-impact) in our blog posts.

### Final Thought on the Future

You may have seen us talking about Modularity in Governance.

We’ve used that approach to design this system in a way that will allow us to iterate as we learn, in a modular fashion, without breaking the system. We don’t know as much today as we will tomorrow, and we need to retain flexibility while not undermining our legitimacy.

More on that [here](https://www.pokt.network/blog/intro-to-modular-governance-at-pokt-dao).

#### Notes:

It is worth noting that the governance power in the Staker house does not include all token holders, it is only linked to productive capital (staked capital). Holding a token is not enough, it needs to be deployed / staked to support the network.

It is also worth noting that for token weighted governance within the Staker house, we apply a method that is similar to quadratic voting in order to flatten the curve and retain a balance of power.
