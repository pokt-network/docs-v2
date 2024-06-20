# Suppliers

Suppliers host the data sources or backend service that Sovereign Applications and Gateways want access to. They bring the data infrastructure to POKT Network. With Shannon we want to enable Suppliers to dramatically reduce their costs, encourage growth, and improve decentralization.

### Proposed Improvements with the Shannon upgrade

The Shannon upgrade will redefine the economics around running Supplier nodes. It will unlock the ability for 1 Supplier node to generate network average rewards with a single PC.

|                                  | Morse    | Shannon      |
| -------------------------------- | -------- | ------------ |
| # of data sources (MaxChains)    | 15       | 1            |
| # regions (GeoMeshing)           | 3        | 1            |
| Estimated monthly hardware costs | $8k      | $0 (home PC) |
| Nodes required to profit         | 100      | 1            |
| POKT required to stake           | 6M ($1M) | 15k ($2.5k)  |

Allowing Suppliers to generate meaningful network rewards on 1 source, in 1 region, makes it possible for anyone to be a supplier. This dramatically diversifies who can participate in POKT Network, further encouraging more decentralization. With more parties acting as Suppliers, Gateways will have more choices, which is good for their QoS.

#### Relay Mining

Relay Mining is a new method of handling work verification that enables Shannon to scale to handle trillions of relays a day. This new system for Shannon employs probabilistic mechanisms, commit-and-reveal schemes, and Sparse Merkle Sum Tries (SMSTs) to estimate and prove the volume of RPCs handled without taxing the blockchain itself.

#### Core Features:

* <mark style="color:red;">`Scalability`</mark>: Dynamically adjusts how work from Suppliers is verified, allowing the network to scale to amount of relays, Sources, or Suppliers.
* <mark style="color:red;">`Commit-and-Reveal Schemes`</mark>: Ensures fair and permissionless distribution of work between Applications, Gateways, and Suppliers.
* <mark style="color:red;">`Sparse Merkle Sum Tries (SMSTs)`</mark>: Efficiently proves the amount of work done without excessive processing overhead.
* <mark style="color:red;">`ClosestMerkleProof`</mark>: A novel proof-of-inclusion scheme that validates the work done.
* <mark style="color:red;">`Rate Limiting Mechanism`</mark>: Implements token bucket algorithms and distributed rate-limiting penalty models to manage RPC request volume.
