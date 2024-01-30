## Staker House

> The guiding principle we hold is that governance must be earned, not bought.

This way the governance system becomes more representative of our ecosystem and perhaps counterintuitively makes the system more resistant to governance capture than before.

The stakers house had 4 credentials :- 

**Supply Path**
This credential provides voting power to node runners or a validator staking POKT to serve relays or secure the network.
They represent __40% of the power__ in the Staker House.
This credentials is made up of :-
**_Valid Stake_** -  Defined as POKT Staked > 60 Days and NOT Jailed, Paused or Unstaking.
**_Credential weight_** - A weighting (impact score) of the the square root of Token-weighted voting power for POKT tokens staked in the network
The credentails are automated.(Credentials are issued or weights adjusted daily to reflect the Valid Stake and Weight of each node/address/wallet)

**Demand-side Path**
This credentials provide the Gateway operators the voting power.
It is given to the gateways that send pokt to the DAO address for burning.
They represent __30% of the power__ in the Staker House.
The requirements for the Demand-Side Stakers are :-
**__Valid Address:__** We will whitelist a POKT Address from which POKT is sent to the DAO for burning pokt for gateway operators.
**__Credentials weight:__** A weighting (impact score) of the square root of aggregate fees (POKT tokens) sent to the DAO for burning in the last 30 Days
This credentials is automated.(POKT only needs to be sent from the valid address for burning)

**__Liquidity Provider Path__**

This credential provides token-weighted voting power to Uniswap LP tokens representing liquidity staked in the Uniswap [wPOKT/ETH](https://app.uniswap.org/add/v2/ETH/0x67F4C72a50f8Df6487720261E188F2abE83F57D7) liquidity pool.
They represent __30% of the power__ in the Staker House.

The requirements for the Liquidity-Side Stakers are:

**__Valid Stake:__** Holding wPOKT/ETH LP tokens from Uniswap

**__Credential weight:__** A weighting (impact score) of the the square root of Token-weighted voting power of the Uniswap LP tokens
Ths credential is automated(we can verify the number of Uniswap LP tokens staked in the wPOKT staking contract from the voter’s wallet address).

> The total voting power of all Stakers can never be more or less than 45% of the total voting power of the DAO. 
**__To be explicit, this 45% power is distributed across Supply Stakers (40% of 45%), Demand Stakers (30% of 45%) and Liquidity Stakers (30% of 45%)__**

The other two houses that complete the voting mechanisms are :- 

[Citizens House](Citizens_House.md)

[Builders House](Builders_House.md)

All houses together form the voting base that move the protocol forward.

[Voting Mechanism](README.md)

[Governance Mechanism](../README.md)
