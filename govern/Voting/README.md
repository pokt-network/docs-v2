## Voting

Our voting module is responsible for enfranchising each of the stakeholder classes in our governance, providing them with the agency to signal their preferences on specific decisions and implementing some of the rules defined in other modules.

##### Voting houses

Anyone who commits to and upholds our POKT DNA and understands the role of our DAO Governance system can become a citizen.

Citizenship is a requirement to have governance power in all governance voting houses. 
There are currently 3 voting houses :-

[Citizens House](Citizens_House.md)

[Builders House](Builders_House.md)

[Stakers House](Stakers_House.md)


##### How it works
To participate in pocket network governance through voting you follow the following steps:-

**_Registering Voting Power_**

Voters use Gateway to register all of the activities that will earn them voting power. 
This includes completing forms on the Gateway dashboard,connecting Ethereum wallets that they’re staking wPOKT with,and connecting POKT wallets that they’re staking nodes with.This will associate their various wallets and credentials to the same Gateway ID.

**_Tracking Voting Power_**

PNF will maintain a database of voting power which regularly mirrors the state of the Gateway protocol, ensuring we have an up-to-date map of Gateway IDs (voter identities) and all of their associated activities (voting power).

**_Locking-in Voting Power_**

When a proposal is created, a timestamp is locked in as a cut-off for voting power. 
Any credentials earned after the vote started will not contribute to voting power. 
This prevents gaming of votes.

**_Gating Voting with Passport_**

In order to vote, voters will need to provide Snapshot with a valid Gitcoin Passport that has a Humanity Score > 20. 
The Passport itself is tied to a specific Ethereum wallet. 
This enables us to maintain sybil protection and protect the limits in our governance. 
For example, with an individual Builder voting power limit of 10, even if a voter has multiple GatewayIDs with 10, they will only be able to vote once with the Passport.

**_Voting with Ethereum Wallet_**

 As is standard with Snapshot, voters will use an Ethereum wallet (e.g. Metamask) to cast their vote. 
 This Ethereum wallet must have a valid Gitcoin Passport attached. 
 If they have previously connected their Ethereum wallet to their Gateway ID, all of the voting power they registered with Gateway will be readable by Snapshot. 
 The Snapshot strategy will pull the associated Gateway ID then pull all associated credentials (voting power).

 **_Voting Weights Tallied at the End_**

 Once the vote concludes, Snapshot will tally up all votes and normalize them so that each of the houses (Citizen/Builder/Staker) has their predefined voting distribution. 
 Since weights won’t be normalized until the end, and we can’t predict voter turnout as it’s happening, it won’t be possible to maintain a running tally of voting weights.

##### Snapshot strategy

 Our snapshot follow the following general principles

 **_No quorum_** 
 Individual voter weights in each dimension are a function of how many in the dimension voted, not how many exist.

**_Inter-house limits_**
 Limits must be used to ensure that each house has a set proportion of voting power regardless of how many users vote.

**_No credential stacking_** 
 People can claim multiple instances of a credential, and this can be done to proactively prevent their voting power expiring, but they shouldn’t be able to stack them for more power.

**_Voting Weights_**
In pocket network the votes have the following weights.
- Citizens: 10% of Total
- Builders: 45% of Total
- Stakers: 45% of Total - which breaks down,as follows
    - Nodes: 40% of Stakers (18% of Total)
    - Gateways: 30% of Stakers (13.5% of Total)
    - LPs: 30% of Stakers (13.5% of Total)

Citizen Credential: If a voter doesn’t possess a Citizen credential, their voting weight will be 0%.

Voting one of the three pillars that form the DAO OS.
Others are : - 

[Citizenship](../Citizenship/README.md)

[ERAs](../ERAs/README.md)

[Governance](../README)