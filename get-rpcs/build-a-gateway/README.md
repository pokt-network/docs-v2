# Host a Gateway

In 2024, with the POKT Network protocol's Shannon upgrade, anyone will be able to self-host their access to POKT Network.&#x20;

Until then, the POKT Network Foundation is beginning to onboard [early access](early-access.md) gateways to the network, to bootstrap POKT Network's gateway ecosystem (lovingly referred to as our Gateway-verse).

### Who should host a POKT Network Gateway?

There are various situations in which it may make sense to host your own POKT Network gateway:

* You have an existing RPC business and want to tap into the cost, uptime, scalability, and wide range of chains that POKT Network offers.
* You are a developer tooling service and want to add RPC services to your existing offering.
* You are a developer community, blockchain foundation, or any other community or organization that wants to maintain RPC service as a public good for its members.
* You are none of the above but you have the experience and desire to integrate with POKT Network and start selling RPC services.

### What are you options for hosting a Gateway?

There are a few different options, depending on your timings and resources.

These include:

* **Gateway-as-a-Service:** white-label the services of one of our [existing Gateways](../find-a-gateway/). Maintain your own frontend and let the gateway provide familiar RPC endpoints on the backend, including QoS optimizations, monitoring, alerts, and other value-add features. You can get started on this right away and don't need to wait to be onboarded via our [early access program](early-access.md).
* **Full-stack Early Access Gateway:** use the [Gateway Kit](gateway-kit.md) to build your own full-stack from late December / early January you will be able to use the open source Gateway Kit that Nodies are currently building to work with POKT Network Foundation to build your own Gateway and connect directly to the protocol. The Kit is in alpha currently and expected to launch in January 2024. You will also need to wait to be onboarded via our [early access program](early-access.md).
* **Full-stack Permissionless Gateway:** If you don't want to have to be manually onboarded by the POKT Network Foundation through our [early access program](early-access.md), you can register your interest to become a gateway once the Shannon upgrade is complete in 2024 and we'll keep you notified of developments.

Here are some considerations for you when choosing an option:

| Option                    | Pros                                                                                                                                                                         | Cons                                                                                                 |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Gateway-as-a-Service      | <ul><li>Minimal learning curve</li><li>Don't need to pay in POKT, gateways accept USD/crypto</li><li>Outsource QoS optimizations and other value-add features</li></ul>      | <ul><li>Dependent on another gateway operator</li><li>Paying extra to the gateway operator</li></ul> |
| Full-stack Early Access   | <ul><li>Support from Foundation and existing gateways</li><li>Full customizability to integrate with your stack</li><li>Cheap POKT gateway fee ($0.85 per million)</li></ul> | <ul><li>More friction to onboard</li><li>Need to learn POKT</li></ul>                                |
| Full-stack Permissionless | <ul><li>Frictionless onboarding</li><li>Self-sovereign - zero dependence on other organizations</li></ul>                                                                    | <ul><li>Need to wait until Shannon upgrade in 2024</li></ul>                                         |

{% hint style="info" %}
There's nothing stopping you starting with one option then evolving to another! For example, you could use Gateway-as-a-Service while you focus on your frontend, then swap out your backend for the self-hosted Gateway Kit.
{% endhint %}
