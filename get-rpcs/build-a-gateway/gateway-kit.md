# Gateway Kit

{% hint style="info" %}
The self-hosted Gateway Kit is currently in alpha development by [Nodies](../find-a-gateway/nodies.md), POKT's second gateway, and expected to launch in January 2024.
{% endhint %}

POKT Network's self-hosted Gateway Kit is a lightweight [gRPC](https://grpc.io) client that integrates with the POKT Network protocol and maintains a familiar HTTP JSON-RPC Server interface for your applications (and any customer applications) to send and receive RPC requests.

With a modular architecture packaged in a Docker-compose form, the Gateway Kit abstracts away the intricacies of the POKT Network protocol, making it as easy as possible to connect to the network while providing the flexibility to choose only the services you need and/or plug in other services.&#x20;

The objective is to enable a one-click deployment with less than one week of lead time to start sending relays to the network.&#x20;

The modules included in the Gateway Kit are:

* **App Stake Module:** Manage your private keys, stake your applications in the POKT Network protocol, generate Application Authentication Tokens (AATs) (which enable app clients to send RPC requests without exposing private keys), and retrieve the relay throughput for your applications.
* **QoS (Quality of Service) Module:** A variety of methods such as filtering, error handling, and predictive analysis to select the node operators that will maximize the availability, reliability, and data quality provided in a given RPC session. The modular architecture means it will be easy for you to optimize your own quality methods.
* **Observability Module**: A bundle of open-source dashboards and time series databases to store and visualize application stakes, throughput, and traffic.
* **HTTP Gateway Module:** A stateless web server bridging your application, the Kit's modules, and the POKT protocol. It retrieves available app stakes for a session using the App Stake Module, selects a suitable node for the session via the QoS Module, sends the request to the chosen node, logs the results into the Observability Module, and finally returns the response back to the app client. To learn more about the RPC relay process that the Gateway Kit will be handling for you, see Nodies Relay Specification [here](https://docs.nodies.app/pokt-integration-wip/relay-specification).

**To learn more about deploying the Gateway Kit and contributing to its open-source codebase, see the GitHub repo** [**here**](https://github.com/baaspoolsllc/os-gateway/tree/main)**.**

## Additional non-POKT Network Gateway modules

Self-hosted gateways, as sovereign entities, also need to build and maintain the following components to enable a full-stack RPC gateway solution for the respective users of their endpoints:

| Gateway component                                                                     | Detail                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Self-hosted Front-end** (onboarding, user accounts, team management, payments, etc) | <ul><li>Standard Web2 SaaS interface, using open-source libraries or B2B tooling (e.g. Vercel, Stripe)</li><li>Complexity depends a lot on the type of gateway service you want to offer - e.g. full enterprise-grade stack, public endpoint dashboard, members-only shared endpoints, etc.</li><li>Grants to support the building of an open source agnostic gateway front-end solution will be announced soon </li></ul> |
| **Back-end RPC endpoint infrastructure**                                              | Components such as webservers, DNS for distributing RPC endpoints, rate limiting, Grafana monitoring/alerting                                                                                                                                                                                                                                                                                                              |
