# INFURA Documentation

## Getting Started

Getting started with Infura takes just a few minutes once you’ve [signed up](https://infura.io/signup).

When you signup you'll receive your API token to use within your app. We use this token to track usage, route your data where it needs to go, and give you access to the most powerful infrastructure for Ethereum.

## Which API should I use?

We have built services and APIs around JSON-RPC, REST and Websockets that you can use with your favorite libraries and frameworks, on four Ethereum networks.  Infura exposes multiple separate APIs with different use cases.

- Ethereum:
  - **REST API**
    - [Documentation](https://infura-staging.now.sh/docs/api/rest/get/symbolFull)
    - Globally cached responses on our CDN for the best end-user latency
    - Value added features like exchange rates and contract black lists.
    - Requires some customizing your code to work with Infura
  - **JSON-RPC Endpoints**
    - [Documentation](https://infura-staging.now.sh/docs/api/jsonrpc/gettingStarted/chooseaNetwork)
    - Seamlessly access Ethereum via the Infura load-balanced nodes and smart architecture the same way you would via your own nodes.
  - **JSON-RPC over Websockets**
    - [Documentation](https://infura-staging.now.sh/docs/api/websockets/beta)
    - Supports subscriptions and filters in addition to stateless RPC methods.
    - Currently in BETA
- IPFS:
  - [Documentation](https://infura-staging.now.sh/docs/api/ipfs)
  - For storage and retrieval of decentralized data in the global IPFS network
