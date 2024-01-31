# Manual Setup Tutorial

#### Background <a href="#background" id="background"></a>

The main utility of a Pocket node is to relay transactions to other blockchains. So, Pocket nodes need access to other nodes for the blockchains they’ll be relaying to. However, the focus of this guide is just on setting up a Pocket node that will relay to the Pocket network, essentially, through itself. **Setting up nodes for other blockchains such as Harmony, Ethereum, or any of the other** [**supported blockchains**](../../readme/supported-chains.md) **is beyond the scope of this guide.**

After completing the steps outlined here, you’ll have a fully functional Pocket node up and running. If you choose, you can also opt to stake your node and earn rewards. We’ll cover that here, but staking is not required unless you want to earn rewards.

#### Who is this guide for? <a href="#who-is-this-guide-for" id="who-is-this-guide-for"></a>

This guide is for anyone interested in running Pocket nodes. While the goal is to keep things simple, the assumption is that you have some general blockchain and computer networking knowledge, and some Linux terminal experience.

#### What you’ll need <a href="#what-youll-need" id="what-youll-need"></a>

In order to complete this guide, you’ll need:

1. A server connected to the internet
2. A domain name
3. The ability to add DNS records for your domain
4. 15,100 POKT (if you want to stake your node)
5. About 2-4 hours to complete and test everything
