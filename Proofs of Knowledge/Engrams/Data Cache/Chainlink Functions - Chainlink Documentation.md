[Skip to Content](#article)

[![Chainlink Documentation](https://docs.chain.link/chainlink-functions/chainlink-docs.svg)](/)

[Data Feeds](/data-feeds) [VRF](/vrf/v2/introduction) [Automation](/chainlink-automation/introduction) [CCIP](/ccip) [Functions](/chainlink-functions) [Nodes](/chainlink-nodes)

Search...![search](https://docs.chain.link/chainlink-functions/assets/search.svg)

[![](https://docs.chain.link/chainlink-functions/assets/github.svg)](https://github.com/smartcontractkit/documentation)

Menu

NEW

Join us at SmartCon 2023—where Web3 gets real. [Get your ticket.](https://smartcon.chain.link/?utm_medium=referral&utm_source=chainlink-docs&utm_campaign=smartcon-2023&agid=kgmdzq5cr7sn)

- ## NAVIGATION
    
    - [Data Feeds](/data-feeds)
    - [VRF](/vrf/v2/introduction)
    - [Automation](/chainlink-automation/introduction)
    - [CCIP](/ccip)
    - [Functions](/chainlink-functions)
    - [Nodes](/chainlink-nodes)
    

---

- Chainlink Functions
    
    - [Overview](/chainlink-functions)
    - [Getting Started](/chainlink-functions/getting-started)
    - [Supported Networks](/chainlink-functions/supported-networks)
    
- Guides
    
    - [Request Computation](/chainlink-functions/tutorials/simple-computation)
    - [Call an API](/chainlink-functions/tutorials/api-query-parameters)
    - [Return Custom Data Types](/chainlink-functions/tutorials/api-custom-response)
    - [POST Data to an API](/chainlink-functions/tutorials/api-post-data)
    - [Using Secrets in Requests](/chainlink-functions/tutorials/api-use-secrets)
    - [Call Multiple Data Sources](/chainlink-functions/tutorials/api-multiple-calls)
    - [Using Off-chain Secrets in Requests](/chainlink-functions/tutorials/api-use-secrets-offchain)
    - [Automate your Functions](/chainlink-functions/tutorials/automate-functions/)
    - [Add Functions to a Project](/chainlink-functions/resources/add-functions-to-projects)
    
- Concepts
    
    - [Concept Overview](/chainlink-functions/resources/concepts)
    - [Architecture](/chainlink-functions/resources/architecture)
    - [Managing Subscriptions](/chainlink-functions/resources/subscriptions)
    - [Billing](/chainlink-functions/resources/billing)
    - [Service Limits](/chainlink-functions/resources/service-limits)
    
- API Reference
    
    - [FunctionsClient](/chainlink-functions/api-reference/functions-client)
    - [Functions library](/chainlink-functions/api-reference/functions)
    
- Resources
    
    - [Learning Resources](/getting-started/other-tutorials?parent=chainlinkFunctions)
    - [Smart Contract Overview](/getting-started/conceptual-overview?parent=chainlinkFunctions)
    
    - [Deploy Your First Smart Contract](/getting-started/deploy-your-first-contract?parent=chainlinkFunctions)
    
    - [LINK Token Contracts](/resources/link-token-contracts?parent=chainlinkFunctions)
    
    - [Acquire testnet LINK](/resources/acquire-link?parent=chainlinkFunctions)
    - [Fund Your Contracts](/resources/fund-your-contract?parent=chainlinkFunctions)
    
    - [Starter Kits and Frameworks](/resources/create-a-chainlinked-project?parent=chainlinkFunctions)
    - [Bridges and Associated Risks](/resources/bridge-risks?parent=chainlinkFunctions)
    - [Chainlink Architecture](/architecture-overview/architecture-overview?parent=chainlinkFunctions)
    
    - [Basic Request Model](/architecture-overview/architecture-request-model?parent=chainlinkFunctions)
    - [Decentralized Data Model](/architecture-overview/architecture-decentralized-model?parent=chainlinkFunctions)
    - [Off-Chain Reporting](/architecture-overview/off-chain-reporting?parent=chainlinkFunctions)
    
    - [Developer Communications](/resources/developer-communications?parent=chainlinkFunctions)
    
    - [Getting Help](/resources/getting-help?parent=chainlinkFunctions)
    - [Hackathon Resources](/resources/hackathon-resources?parent=chainlinkFunctions)
    
    - [Contributing to Chainlink](/resources/contributing-to-chainlink?parent=chainlinkFunctions)
    

 

# Chainlink Functions

## On this page

- [Overview](#overview)
- [When to use Chainlink Functions](#when-to-use-chainlink-functions)
- [Supported networks](#supported-networks)

![note](https://docs.chain.link/chainlink-functions/_astro/info-icon.ca56bc94.svg)

Explore Chainlink Functions Playground

Start exploring Chainlink Functions in your browser using the [Chainlink Functions Playground](https://functions.chain.link/playground). You can use the playground to simulate Chainlink Functions, call APIs, and execute demo requests.

![note](https://docs.chain.link/chainlink-functions/_astro/info-icon.ca56bc94.svg)

Get Started

Chainlink Functions is available on testnet as a limited BETA preview. Apply [here](https://chainlinkcommunity.typeform.com/requestaccess) to request access and get started.

Chainlink Functions provides your smart contracts with access to a trust-minimized compute infrastructure. Your smart contract sends your code to a [Decentralized Oracle Network (DON)](/chainlink-functions/resources/concepts), and each DON's oracle runs the same code in a serverless environment. The DON aggregates all the independent runs and returns the final result to your smart contract. Your code can be anything from simple computation to fetching data from API providers.

Chainlink Functions provides access to off-chain computation without having to run and configure your own Chainlink Node. To pay for requests, you fund a subscription account with LINK. Your subscription is billed only when the DON fulfills your request.

To learn more about how _Chainlink Functions_ works, read the [concepts](/chainlink-functions/resources/concepts) and the [architecture](/chainlink-functions/resources/architecture) pages.

See the [Tutorials](/chainlink-functions/tutorials) page to find some simple tutorials that show you different GET and POST requests that run on _Chainlink Functions_. You can also gain hands-on experience with Chainlink Functions with the [Chainlink Functions Playground](https://functions.chain.link/playground).

## When to use Chainlink Functions[](#when-to-use-chainlink-functions)

![note](https://docs.chain.link/chainlink-functions/_astro/info-icon.ca56bc94.svg)

note

Chainlink Functions is a self-service solution. You are responsible for independently reviewing any JavaScript code that you write and submit in a request. This includes API dependencies that you send to be executed by Chainlink Functions. Community-created Javascript code examples might not be audited, so you must independently review this code before you use it.

Chainlink Functions is offered "as is" and "as available" without conditions or warranties of any kind. Neither Chainlink Labs, the Chainlink Foundation, nor Chainlink node operators are responsible for unintended outputs that are generated by Functions due to errors in Javascript code submitted by developers or downstream issues with API dependencies. Users must ensure that the data sources specified in requests are of sufficient quality and have the proper availability for your use case. Users are responsible for complying with the licensing agreements for all data providers that they connect with through Chainlink Functions.

_Chainlink Functions_ enables a variety of use cases. Use _Chainlink Functions_ to:

- Connect to any public data. For example, you can connect your smart contracts to weather statistics for parametric insurance or real-time sports results for Dynamic NFTs.
- Connect to public data and transform it before consumption. You could calculate Twitter sentiment after reading data from the Twitter API, or derive asset prices after reading price data from [Chainlink Price Feeds](/data-feeds/price-feeds).
- Connect to a password-protected data source; from IoT devices like smartwatches to enterprise resource planning systems.
- Connect to an external decentralized database, such as IPFS, to facilitate off-chain processes for a dApp or build a low-cost governance voting system.
- Connect to your Web2 application and build complex hybrid smart contracts.
- Fetch data from almost any Web2 system such as AWS S3, Firebase, or Google Cloud Storage.

You can find several community examples at [useChainlinkFunctions.com](https://www.usechainlinkfunctions.com/)

![note](https://docs.chain.link/chainlink-functions/_astro/info-icon.ca56bc94.svg)

Testnet BETA Preview

Chainlink Functions is available on testnet only as a limited BETA preview to ensure that this new platform is robust and secure for developers. While on testnet and in BETA, developers must follow best practices and not use the BETA for any production application or secure any value. Chainlink Functions is likely to evolve and improve. Breaking changes might occur while the service is in BETA. Monitor these docs to stay updated on feature improvements along with interface and contract changes. Apply [here](https://chainlinkcommunity.typeform.com/requestaccess) to request access and add your EVM account address to the allow list.

## Supported networks[](#supported-networks)

See the [Supported Networks](/chainlink-functions/supported-networks) page to find a list of supported networks and contract addresses.

## What's next

- [› Learn the basics in the Getting Started guide.](/chainlink-functions/getting-started)
- [› Learn how to use more advanced capabilities in one of the Tutorials.](/chainlink-functions/tutorials)
- [› Learn about core concepts, the Chainlink Functions architecture, and billing.](/chainlink-functions/resources)

## More

- [Edit this page](https://github.com/smartcontractkit/documentation/tree/main/src/content/chainlink-functions/index.mdx)
- [Join our community](https://discord.com/invite/aSK4zew)

## On this page

- [Overview](#overview)
- [When to use Chainlink Functions](#when-to-use-chainlink-functions)
- [Supported networks](#supported-networks)

## More

- [Edit this page](https://github.com/smartcontractkit/documentation/tree/main/src/content/chainlink-functions/index.mdx)
- [Join our community](https://discord.com/invite/aSK4zew)

## Feedback

## Stay updated on the latest Chainlink news

Email Address

### Developers

- [Developer resources](https://chain.link/developer-resources)
- [LINK Token Contracts](/resources/link-token-contracts)
- [Data Feeds](/data-feeds)
- [VRF](/vrf/v2/introduction)
- [Automation](/chainlink-automation/introduction)
- [Functions](/chainlink-functions)
- [CCIP](/ccip)

### Solutions

- [Overview](https://chain.link/solutions)
- [DeFi](https://chain.link/solutions/defi)
- [Chainlink VRF](https://chain.link/vrf)

### Community

- [Chainlink Hackathon](https://chain.link/hackathon/)
- [Community overview](https://chain.link/community)
- [Grant program](https://chain.link/community/grants)
- [Events](https://chain.link/community/events)
- [Become an advocate](https://chain.link/community/advocates)
- [Code of conduct](https://chain.link/code-of-conduct)

### Chainlink

- [Ecosystem](https://chain.link/ecosystem)
- [Press](https://chain.link/press)
- [Blog](https://blog.chain.link)
- [Team](https://chain.link/team)
- [Careers](https://chainlinklabs.com/careers)
    
    WE ARE HIRING!
    
- [Brand assets](https://chain.link/brand-assets)
- [FAQs](https://chain.link/faqs)

### Contact

- [Security](mailto:security@chain.link)
- [Support](mailto:support@chain.link)
- [Press inquiries](mailto:press@chain.link)

### Social

- ![](https://assets-global.website-files.com/5f6b7190899f41fb70882d08/5f760fcc8de393ea2bffa0ff_twitter.svg) [Twitter](https://twitter.com/chainlink)
- ![](https://assets-global.website-files.com/5f6b7190899f41fb70882d08/5f760fcc3830fc22d9bc18c8_youtube.svg) [YouTube](https://www.youtube.com/channel/UCnjkrlqaWEBSnKZQ71gdyFA)
- ![](https://assets-global.website-files.com/5f6b7190899f41fb70882d08/5f760fcff3840d5ec8300b30_discord.svg) [Discord](https://discord.gg/aSK4zew)
- ![](https://assets-global.website-files.com/5f6b7190899f41fb70882d08/5f760fcceaf22843cde97118_telegram.svg) [Telegram](https://t.me/chainlinkofficial)
- ![](https://assets-global.website-files.com/5f6b7190899f41fb70882d08/5f760fcc8e9ff41b546f039f_wechat.svg) [WeChat](https://blog.chain.link/chainlink-chinese-communities/)
- ![](https://assets-global.website-files.com/5f6b7190899f41fb70882d08/5f760fcc8f83d17d2d857106_reddit.svg) [Reddit](https://www.reddit.com/r/Chainlink/)

[![Chainlink logo](https://assets-global.website-files.com/5f6b7190899f41fb70882d08/5f7610da8f83d1e6028573c7_chainlink-logo-footer.svg)](/)

Chainlink®

© 2023 Chainlink Foundation

[Privacy Policy](https://chain.link/privacy-policy) [Terms of Use](https://chain.link/terms)