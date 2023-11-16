
## Technical Overview

The PoK system is a method of linking data points to their original research question. This is achieved through the creation and usage of kEngrams, which are JSON objects that contain various pieces of structured information. 

## Engram Creation

kEngrams are JSON objects that serve as a bridge between individual data points and the original research question. They are designed to be flexible and adaptable, capable of containing any type of information as long as they reference each other. 

The structure of a kEngram includes:
- The Study question: This is the base note of the kEngram. It is the original research question that the data points are linked to.
- The position of each data point on the X and Y axis: This helps in visualizing the data and understanding its relation to the research question.
- Individual notes within an engram: These notes can contain any type of information, as long as they are referencing each other.

## The Attestation Record[​](https://docs.attest.sh/docs/tutorials/make-an-attestation#the-attestation-record "Direct link to heading")

A unique `attestation record` is created each time an attestation is made using EAS and can be verified on the [EAS explorer](https://easscan.com/). The attestation record contains important information about the attestation, including the schema used, the attestor, the recipient (if specified), the expiration time (if specified), and more.

## Understanding the Attestation Record[​](https://docs.attest.sh/docs/tutorials/make-an-attestation#understanding-the-attestation-record "Direct link to heading")

Each attestation record has the following fields:

- `UID` - this is a universal unique identification number for the attestation.
- `Schema` - the UID of the schema used to make the attestation.
- `Attestor` - the address that made the attestation.
- `Recipient` - an **optional** recipient of the attestation that was made.
- `Expiration Time` - an **optional** date that the attestation will expire if provided by the attestor.
- `Revocation Time` - the time at which the attestation was revoked (if any).
- `refUID` - An attestation that this attestation is referencing (if any).
- `data`- The ABI encoded data for the attestation.
## Engram Attestation

The PoK system allows for questions to be submitted onchain through the Ethereum Attestation Service (EAS). This service enables the attestation schema to be attached to a smart contract, guaranteeing ownership over further attestations of a particular question. 

Attestations can be produced offchain for no gas cost, and can be submitted in bulk through merkle trees for the entire contents of the engram. The submission of attestations is facilitated through the DSW obsidian plugin.

### Attester Resolver[​](https://docs.attest.sh/docs/tutorials/resolver-contracts#attester-resolver "Direct link to heading")

The `AttesterResolver.sol` resolvers purpose is to check if an attestation is created by a specific attester, which has previously registered into the contract. When a new attestation is submitted using this resolver, the contract verifies that the attestation comes from the same attester before allowing it to proceed.


```solidity
// SPDX-License-Identifier: MIT

pragma solidity 0.8.19;

import { SchemaResolver } from "../SchemaResolver.sol";
import { IEAS, Attestation } from "../../IEAS.sol";

/**
 * @title A sample schema resolver that checks whether the attestation is from a registered attester.
 */
contract AttesterResolver is SchemaResolver {
    mapping(address => bool) private _registeredAttesters;

    constructor(IEAS eas) SchemaResolver(eas) {}

    function registerAttester(address attester) public {
        _registeredAttesters[attester] = true;
    }

    function onAttest(Attestation calldata attestation, uint256 /*value*/) internal view override returns (bool) {
        return _registeredAttesters[attestation.attester];
    }

    function onRevoke(Attestation calldata /*attestation*/, uint256 /*value*/) internal pure override returns (bool) {
        return true;
    }
}
```

# Referenced Attestations

`refUID` is one of the most powerful features of an EAS attestation that unlocks its composability by allowing one attestation to reference another.

This functionality enables the creation of a hierarchy or a chain of attestations that depend on one another. In doing so, attestations can be organized in a more structured manner and their relationships can be easily understood.

## Concept[​](https://docs.attest.sh/docs/tutorials/referenced-attestations#concept "Direct link to heading")

An attestation can reference another attestation by including its unique identifier (UID) as the refUID field in the new attestation. The referenced attestation serves as a basis or prerequisite for the new attestation. This relationship can be used to represent dependencies between attestations, where one attestation's validity or relevance is improved upon by the existence and validity of another.

## Engram Usage

The PoK system utilizes a chat interface framework known as Khoj. This framework allows for a vector search of existing kEngrams to find relevant context. Once a research question is found, the related notes are also produced in order to regenerate the context for the LLM to use

Once the response is created. The user will see which notes were selected to create the response after which, the system will create an offchain attestation  and propagation using the Ceramic Network. This allows for efficient indexing of attestations, kEngram scoring, and royalty payout to creators.

## Ceramic Network[​](https://docs.attest.sh/docs/tutorials/ceramic-storage#ceramic-network "Direct link to heading")

 [Ceramic](https://ceramic.network/), a decentralized data network that leverages the provenance-related qualities you can expect from a blockchain, with the cost efficiency and querying capabilities you'd experience with a traditional database. Ceramic also empowers developers to leverage the interoperable data formats stored within the Network, enabling product teams to circumvent the "cold-start" data problem, while allowing individuals to take ownership of their digital presence.

### How does it Work?[​](https://docs.attest.sh/docs/tutorials/ceramic-storage#how-does-it-work "Direct link to heading")

The Ceramic Protocol is built on decentralized event streams, where user accounts (enabled by decentralized identifiers, or [DIDs](https://developers.ceramic.network/protocol/accounts/decentralized-identifiers/)) cryptographically sign data events and submit them to the network. The events themselves are stored in the Interplanetary File System (IPFS) using the IPLD protocol, which are organized into readable streams. As such, streams are flexible enough to store many types of content such as user profiles, posts, relations to other entities, and (you guessed it) attestations.

### Ceramic as a Data Ledger[​](https://docs.attest.sh/docs/tutorials/ceramic-storage#ceramic-as-a-data-ledger "Direct link to heading")

Finally, it's important to note that Ceramic can be viewed as a "Data Ledger" middleground-of-sorts between on-chain activity and the off-chain realm. All Ceramic events are periodically rolled into a merkle tree and the root is published to the Ethereum blockchain, preserving consensus on the global ordering of Ceramic transactions.

For more information on how Ceramic works, visit [How it Works](https://ceramic.network/how-it-works).

### ComposeDB[​](https://docs.attest.sh/docs/tutorials/ceramic-storage#composedb "Direct link to heading")

ComposeDB is a graph database built on Ceramic that offers further composability and ease-of-querying to developers. ComposeDB comes with native support for GraphQL, and also automatically splits read/write load for additional performance. When running a Ceramic node with ComposeDB, developers can define their own [data models](https://composedb.js.org/docs/0.5.x/create-your-composite) using GraphQL, or choose to begin indexing on existing data models already defined by the community, or both!

For the purpose of this tutorial, we will be using Ceramic with ComposeDB to illustrate how developers can generate, store, and query off-chain attestations.

## Proof of Knowledge DSW Issuance

The Proof of Knowledge (PoK) protocol utilizes the DSW token as a utility token within its system. The DSW token plays a crucial role in incentivizing the creation of kEngrams.

The issuance of DSW tokens is directly tied to the usage of kEngrams. Creators of kEngrams are rewarded with DSW tokens based on the number of attestations of usage their kEngram has been responsible for in a given period. This means that the more a kEngram is used and referenced within the PoK system, the more DSW tokens the creator of that kEngram will receive.

This system of issuance serves two main purposes. Firstly, it incentivizes the creation of high-quality kEngrams, as creators are rewarded based on the usage of their kEngrams. Secondly, it ensures a fair distribution of DSW tokens, as those who contribute the most to the PoK system are rewarded the most.

The PoK system also allows for questions to be submitted onchain through the Ethereum Attestation Service (EAS). This service enables the attestation schema to be attached to a smart contract, guaranteeing ownership over further attestations of a particular question. Attestations can be produced offchain for no gas cost, and can be submitted in bulk through merkle trees for the entire contents of the engram.

Once an attestation is created, it is propagated with the Ceramic Network, which allows for efficient indexing of attestations, kEngram scoring, and royalty payout to creators. This integration with the Ceramic Network further enhances the utility of the DSW token, as it allows for a decentralized and efficient method of tracking and rewarding the usage of kEngrams.

## Tokenomic Overview

The DSW token is a utility token within the PoK system, designed to incentivize the creation and usage of kEngrams. The token is issued based on the number of attestations of usage a kEngram has generated.

## Token Issuance

1. **Initial Distribution**: A fixed amount of DSW tokens will be minted at the launch of the PoK system. This initial supply will be allocated to the development team, early backers, and a reserve for future development and partnerships.
    
2. **Reward for kEngram Creators**: A portion of the DSW tokens will be allocated as rewards for kEngram creators. The number of tokens issued to each creator will be proportional to the number of attestations their kEngrams generate. This incentivizes the creation of high-quality kEngrams.
    
3. **Community Rewards**: A portion of DSW tokens will be set aside for community rewards. These can be earned by users who contribute to the PoK system, such as by participating in community events, providing feedback, or helping to improve the system.
    

## Token Utility

DSW tokens are used within the PoK system to incentivize and reward the creation and usage of kEngrams. The tokens have several utilities:

1. **Reward for kEngram Usage**: Users who create kEngrams that are frequently used and referenced within the PoK system will receive DSW tokens as a reward.
    
2. **Governance**: DSW token holders may have the right to participate in the governance of the PoK system, voting on various proposals such as changes to the system, token issuance rate, and more.
    
3. **Access to Premium Features**: In the future, DSW tokens could potentially be used to access premium features within the PoK system.