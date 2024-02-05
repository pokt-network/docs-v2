# Servicing

### Overview <a href="#overview" id="overview"></a>

POKT Network’s Servicing layer is comprised of 2 main actors: Applications and Servicers.&#x20;

An Application submits a Relay Request, or an API requests to be routed to any Relay Chain. A Servicer ‘services’ the Application, by routing the Relay Request to the Relay Chain and forwarding the response to the Application.&#x20;

This interaction between an Application and a Servicer is the fundamental utility of POKT Network.

### Basic Lifecycle <a href="#basic-lifecycle" id="basic-lifecycle"></a>

1. To _register_ for decentralized infrastructure, an Application must stake the native cryptocurrency POKT in the network.
2. The amount of the sanctioned throughput (per request) is determined by the amount the Application stakes in the network.
3. To _register_ to provide decentralized infrastructure, a Servicer must stake the native cryptocurrency POKT in the network.
4. After the subsequent staking, an Application is paired with Servicer(s), during which time the servicing interaction takes place.
5. For providing the decentralized infrastructure, Servicer receives an amount of the native cryptocurrency POKT proportional to the amount of throughput (in requests) served.
6. Once an Application or Servicer unstakes, they are _unregistered_ from POKT Network and the stake is returned to their account.

### Sessions <a href="#sessions" id="sessions"></a>

#### Distribution <a href="#distribution" id="distribution"></a>

The Servicer(s) that are paired to service an Application in a Session are _equally_ distributed among all of the Servicers in the network.

Meaning that every Servicer theoretically serves the same amount as their peers and every Application theoretically will be evenly serviced by each Servicer over time.

#### Generation <a href="#generation" id="generation"></a>

The generation of a Session is key to the equal distribution property.

Equally distributed sessions are generated with _pseudorandom_ seed data:

* **BlockHash**: Hash of the last Session Block
* **AppPubKey**: The Application’s public key
* **RelayChain**: The identifier of the Relay Chain

The result of using this seed data is unique sessions for every Relay Chain of Application at any given Session period.

The Servicers over time that will serve each Application at any given time are extrapolated using this data, meaning any actor with the following blockchain data is able to generate the proper serving Servicers.

A single **Dispatch** API call to any full node on POKT Network will provide an Application client with the ServiceURI of their Session period Servicers.

#### Tumbling <a href="#tumbling" id="tumbling"></a>

Tumbling is the act of regenerating a Session with new seed data.

Sessions are _tumbled_ periodically every predetermined (by governance) quantity of blocks.

The tumbling mechanism allows for much greater Application security, as the same Validator(s) will only service the Application for a certain amount of time.

#### Throughput <a href="#throughput" id="throughput"></a>

The max Application throughput (in number of requests) is proportional to the amount staked.

The maximum a Servicer in a Session can service for a certain Application is determined using the following formula:

`max_app_relays = base_throughput / (# of Servicers in Session * # of relay_chains staked for)`

### Relays <a href="#relays" id="relays"></a>

#### **Payload** <a href="#payload" id="payload"></a>

The request payload is the body of the RPC request

* **Data**: The actual request body to be forwarded to the Relay Chain
  * e.g. `{"jsonrpc":"2.0","method":"web3_clientVersion","params":[],"id":67}`
* **Method**: The HTTP CRUD method
  * e.g. `POST`
* **Path**: Path variable for REST support
  * e.g: `"/v1/query/block"`
* **Headers**: HTTP Headers
  * e.g. `Content-Type: application/json`

#### **Metadata** <a href="#metadata" id="metadata"></a>

The Relay Metadata is Protocol level descriptive information that is needed for servicing.

* **BlockHeight**: POKT Network block height when the request was made

The metadata mechanism allows for a configurable _client syncronization_ module, enabling the **Servicer** to reject out of sync clients.

Since the Metadata is grouped into the request hash, this mechanism is a protection against Client level synchronization attacks where the Client is able to challenge single **Servicers** by requesting chain data at a different time than the majority.

#### **Proof of Relay (Evidence)** <a href="#proof-of-relay-evidence" id="proof-of-relay-evidence"></a>

A **Proof of Relay** is the portion of a Relay Request that is used for verification of the atomic work completed.

For each Application of each Session, a Servicer collects Relay Evidence in the form of a **Proof of Relay**. The amount of Relay Evidence is completely proportional to the amount of Relays serviced, meaning for each Relay successfully completed, the Servicer stores one piece of **Relay Evidence**.

**Structure of the Proof of Relay**

* **RequestHash**: _The SHA3-256 hash of the request payload_
  * Connects the specific payload with the proof
  * Needed for the **Application Challenge Mechanism**
* **Entropy**: _A unique nonce (random number) that ensures uniqueness_
  * Unique Relays are a requirement of Pocket Network for Claim/Proof Submission
  * Collisions are rejected by the Servicers
* **SessionBlockHeight**: _The block height of the session when the Relay was serviced_
  * Needed to verify the participants of Session
* **ServicerPubKey**: _The ED25519 Public Key of the servicer_
  * Needed to identify the servicer
* **RelayChain**: _The identifier of the ‘relayed to’ blockchain_
  * Ex: 0021 (Eth mainnet)
* **AAT**: _The Application Authentication Token for the client serviced_
  * Includes both App Public Key and Client Public Key
  * Needed for protocol level verification (app node pairings, client permissions, etc.)
* **ClientSignature**: _The Elliptic Curve Digital Signature of the client_
  * Preserves the integrity of the Relay data
  * Needed at Proof/Claim verification level

#### Response <a href="#response" id="response"></a>

**Response Payload**

The response payload is the body of the RPC response:

* **Response**: String representation of the HTTP response

**Servicer Signature**

The servicer signature completes the signature exchange needed to verify all parties in the servicing protocol.

* **Signature**: preserves the integrity by signing the hash of the **Proof of Relay** and the response payload.

### Claim/Proof Lifecycle <a href="#claimproof-lifecycle" id="claimproof-lifecycle"></a>

In order to participate in the network economic incentive mechanism, the Servicer must first **Claim** and then **Prove** the completed work. For each Application of each Session, after servicing is complete and Relay Evidence is collected, the Servicer must send two subsequent transactions:

1. **Claim Transaction**
   * Merkle Root of Relay Evidence
   * Number of Relays serviced
   * Evidence Type (Relay or Challenge)
2. **Proof Transaction**
   * Selected Relay
   * Corresponding Merkle Proof for selected Relay
   * Evidence Type (Relay or Challenge)

Upon successful completion of BOTH transactions, the Servicer is minted reward directly to their address.

#### Merkle Tree <a href="#merkle-tree" id="merkle-tree"></a>

POKT Network requires a specific Merkle tree implementation that ensures no two leafs of the Merkle tree are identical (for Relay replay protection). [Plasma-Core’s](https://web.archive.org/web/20221007191932/https://plasma-core.readthedocs.io/en/latest/specs/sum-tree.html) Merkle sum tree satisfies this property.

By using the hash of the Relay data (integrity is validated by verifying the Application Client Signature) in conjunction with the replay protection from the Plasma tree, Pocket Network can probabilistically guarantee work completed without the Servicer actually transmitting the entirety of its Relay Evidence to the rest of the network.

A fancier name for this is a _Zero Knowledge Range Proof_.

#### Zero Knowledge Range Proof <a href="#zero-knowledge-range-proof" id="zero-knowledge-range-proof"></a>

In order to complete a successful ZKRP in POKT Network, the following steps must be executed by each Servicer for each Session:

1. Generate the Merkle Tree using the SHA3-256 hash of the Relay Evidence as the leafs
2. Submit a **Claim Transaction** to preserve the integrity of the local Merkle tree and corresponding Relay Evidence, as well as inform the protocol of the _range_ or number of leafs possible to select from
3. After a protocol wide waiting period (determined by governance), the Servicer generates the selected leaf (using the latest block hash as _pseudorandom entropy_ to prevent knowledge of the selection during claim generation) and subsequently creates a **Merkle Proof** (branch) for the _pseudorandomly selected_ leaf.
4. The Servicer submits a **Proof Transaction** containing the selected leaf (Relay Evidence) and the corresponding **Merkle Proof** (branch)
5. The protocol verifies the Merkle proof against the previously submitted Merkle root (in the **Claim Transaction**), verifies the session (proper app/node pair, not overserviced etc.), and then verifies the client signature against the **Proof of Relay** (integrity check)
6. All of the Validators confirm the validity of the **Proof Transaction**, completing the **Zero Knowledge Range Proof**
7. Tokens are minted to the address of the Servicer proportional to the amount of Relays served.

\
