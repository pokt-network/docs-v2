# Host a Gateway

### Why Host a Gateway?

Decentralizing your node operations brings huge benefits but it is challenging.

Instead, you can unlock the same benefits by building your services on top of our decentralized network of c.15 k nodes, 66% on bare metal, in 22 countries, and with dozens of independent hardware operators.

{% hint style="info" %}
With the [Shannon Upgrade](../../pokt-protocol/shannon.md) (targeted to deploy to MainNet late Q2 2024), the ability to deploy a Gateway to POKT Network will be fully permissionless.&#x20;

In the meantime, POKT Network Foundation is working with a group of high potential [Early Access](broken-reference) partners. Partners are selected based on potential contribution to protocol revenue, innovation, and values alignment.

Alternatively, you can explore the Gateway-as-a-Service option offered by both [Grove](../../developers/use-a-gateway/grove.md) and [Nodies](../../developers/use-a-gateway/nodies.md). Using Gateway-as-a-Service, you can white-label their services while maintaining your own frontend.&#x20;
{% endhint %}

### Who should host a POKT Network Gateway?

Some situations in which it makes sense to host your own POKT Network gateway:

* You have an existing RPC business and want to tap into the cost, uptime, scalability, and wide range of chains that POKT Network offers.
* You are a developer tooling service and want to add RPC services to your existing offering.
* You are a developer community, blockchain foundation, or any other community or organization that wants to maintain RPC service as a public good for its members.
* You have a strong existing developer-focused brand or distribution channel that you can better monetize by selling RPC services.
* You care about decentralization and self-sovereignty and want to interact with POKT Network's decentralized network of nodes without an intermediary.

### What are you options for hosting a Gateway?

There are a few different options, depending on timing and your resources.

These include:

* **Gateway-as-a-Service:** white-label the services of one of our [existing Gateways](../../developers/use-a-gateway/). Maintain your own frontend and let the gateway provide familiar RPC endpoints on the backend, including QoS optimizations, monitoring, alerts, and other value-add features.&#x20;
* **Early Access Gateway Program:** use the open source [POKT Gateway Server](gateway-server.md) to easily deploy your own Gateway and connect directly to the protocol. Until the Shannon upgrade, access is available only via the Early Access program.
* **Permissionless Gateway:** register your interest to become a gateway once the Shannon upgrade is complete in 2024 and we'll keep you notified of developments.

Here are some considerations for you when choosing an option:

| Option                       | Pros                                                                                                                                                                                                                                                               | Cons                                                                                                               |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| Gateway-as-a-Service         | <ul><li>Quick and easy: minimal learning curve and minimal up-front resources required</li><li>No requirement to pay in POKT (gateways accept USD/crypto)</li><li>Outsource all backend infrastructure,  QoS optimizations, and other value-add features</li></ul> | <ul><li>Dependent on another gateway operator</li><li>Higher costs vs direct protocol access</li></ul>             |
| Early Access Gateway Program | <ul><li>Lowest cost to access: $0.85 per million relays</li><li>Fully customizable - integrate with your stack</li><li>Easy deployment of  open source POKT Gateway Server</li><li>Full support from Foundation and POKT Network Community</li></ul>               | <ul><li>Need to build and maintain your own stack</li></ul>                                                        |
| Permissionless Gateway       | <p>Everything in Full Stack Early Access plus:</p><ul><li>Frictionless onboarding</li><li>Self-sovereign - zero dependence on other organizations</li></ul>                                                                                                        | <p>Everything in Full Stack Early Access plus:</p><ul><li>Need to wait until the Shannon upgrade in 2024</li></ul> |

{% hint style="info" %}
There's nothing stopping you from starting with one option then evolving to another! For example, you could use Gateway-as-a-Service while you focus on your frontend, then swap out your backend for the self-hosted Gateway Kit.
{% endhint %}
