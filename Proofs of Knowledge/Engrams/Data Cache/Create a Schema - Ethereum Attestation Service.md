[Skip to main content](#docusaurus_skipToContent_fallback)

[

![EAS Logo](https://docs.attest.sh/docs/tutorials/create-a-schema/img/eas-logo.png)

**Ethereum Attestation Service**](/)

[EAS Explorer](https://easscan.com/)[EAS Website](https://attest.sh/)[GitHub](https://github.com/ethereum-attestation-service)

Search...

- [Welcome to EAS](/docs/welcome)
- [Purpose](/docs/category/purpose)
    
- [Quick Start](/docs/category/quick-start)
    
- [Core Concepts](/docs/category/core-concepts)
    
- [Developer Tools](/docs/category/developer-tools)
    
- [Tutorials](/docs/category/tutorials)
    
    - [Create a Schema](/docs/tutorials/create-a-schema)
    - [Make an Attestation](/docs/tutorials/make-an-attestation)
    - [Fetching Data with EAS](/docs/tutorials/get-an-attestation)
    - [Referenced Attestations](/docs/tutorials/referenced-attestations)
    - [Revoking Attestations](/docs/tutorials/revoking-attestations)
    - [Delegated Attestations](/docs/tutorials/delegated-attestations)
    - [Storing Offchain Attestations](/docs/tutorials/storing-offchain-data)
    - [Timestamping Attestations](/docs/tutorials/timestamping-attestations)
    - [Using Resolver Contracts](/docs/tutorials/resolver-contracts)
    - [Making Gas Efficient Schemas](/docs/tutorials/gas-efficiency)
    - [Private Data Attestations](/docs/tutorials/private-data-attestations)
    - [Storing on Ceramic](/docs/tutorials/ceramic-storage)
    - [Naming Your Schema](/docs/tutorials/naming-your-schema)
    - [Schema Descriptions](/docs/tutorials/schema-description)
    - [Schema Context](/docs/tutorials/schema-context)
- [The Explorer](/docs/category/the-explorer)
    
- [Ideas to Build](/docs/category/ideas-to-build)
    

- [](/)
- [Tutorials](/docs/category/tutorials)
- Create a Schema

On this page

# Create a Schema

A schema defines the data structure for an attestation within the Ethereum Attestation Service (EAS). Schemas are customizable and can be created for any purpose, allowing users to leverage preexisting schemas or create new ones tailored to their specific needs.

Tip

Before creating a new schema, double-check the [Schemas](https://easscan.org/schemas) on the EAS Explorer to see if a suitable one already exists for your attestation requirements.

## Schema Fields[​](#schema-fields "Direct link to heading")

Schemas follow the **Solidity ABI** for acceptable types. Below is a list of current elementary types:

- `address` An address can be any ethereum address or contract address.
- `string` A string can be any text of arbitrary length
- `bool` A bool can either be true or false.
- `bytes32` A bytes32 is a 32 byte value. Useful for unique identifiers or small data.
- `bytes` A bytes value is an arbitrary byte value.
- `uints` uint values can be from uint8 -> uint256.
- `<type>[]` A variable-length array of elements of the given type (ex. address[]).

Have questions about acceptable types? Learn more about [Solidity ABI types](https://docs.soliditylang.org/en/v0.8.16/abi-spec.html).

# The Schema Record

EAS uses Ethereum smart contracts to register and verify attestations. Each schema registered on EAS has a record that can be viewed on EASSCAN for the chain you're building on. Here' are a few quick links:

## The Schema Record[​](#the-schema-record-1 "Direct link to heading")

EAS uses Ethereum smart contracts to register and verify attestations. Each schema registered on EAS has a record that can be viewed on EASSCAN for the chain you're building on.

|Chain|EASSCAN Link|
|---|---|
|**Mainnet**|[View Schemas](https://easscan.org/schemas)|
|**Optimism**|[View Schemas](https://optimism.easscan.org/schemas)|
|**Base**|[View Schemas](https://base.easscan.org/schemas)|
|**Arbitrum**|[View Schemas](https://arbitrum.easscan.org/schemas)|
|**Sepolia**|[View Schemas](https://sepolia.easscan.org/schemas)|
|**Optimism Goerli**|[View Schemas](https://optimism-goerli.easscan.org/schemas)|
|**Base Goerli**|[View Schemas](https://base-goerli.easscan.org/schemas)|

## Understanding the EAS schema record[​](#understanding-the-eas-schema-record "Direct link to heading")

Learn how to read a schema record and understand if it's the proper structure for your use case.

**Each schema record has the following fields:**

- `Schema #` - this is an incremental number automatically assigned to the Schema. It is not a unique identifier.
- `UID` - this is the unique universal identifier assigned to the schema.
- `Creator` - the wallet address that created the schema.
- `Transaction ID` - the Ethereum transaction registering the schema on EAS.
- `Resolver Contract` - An optional contract assigned to the Schema for more complex use cases.
- `Attestation Count` - The amount of attestations that have been made with attestations on/off chain.
- `Schema` - The ABI encoded schema field types.

**Example Schema Record** ![#33 - Make A Statement](https://docs.attest.sh/docs/tutorials/create-a-schema/assets/images/gm-schema-59f4bb2ebc4a0a9ea3e0f5ef68e827f3.png)

## Making Schemas 🧙[​](#making-schemas- "Direct link to heading")

### No-Code Schema Builder[​](#no-code-schema-builder "Direct link to heading")

Use the no-code schema builder on any easscan explorer site, such as [https://easscan.org/schema/create](https://easscan.org/schema/create) ![No Code Schema Builder](https://docs.attest.sh/docs/tutorials/create-a-schema/assets/images/no-code-schema-4e9daf8ad00c66ab387359ac792437cd.png)

### Use the SDK[​](#use-the-sdk "Direct link to heading")

To register a new schema, you can use the register function provided by the [**EAS SDK**](https://github.com/ethereum-attestation-service/eas-sdk#registering-a-schema). This function takes an object with the following properties:

- **schema:** The schema string that defines the structure of the data to be attested.
- **resolverAddress:** The Ethereum address of the resolver responsible for managing the schema.
- **revocable:** A boolean value indicating whether attestations created with this schema can be revoked.

Here's an example of how to register a new schema:

```
import { SchemaRegistry } from "@ethereum-attestation-service/eas-sdk";import { ethers } from 'ethers';const schemaRegistryContractAddress = "0xYourSchemaRegistryContractAddress";const schemaRegistry = new SchemaRegistry(schemaRegistryContractAddress);schemaRegistry.connect(signer);const schema = "uint256 eventId, uint8 voteIndex";const resolverAddress = "0x0a7E2Ff54e76B8E6659aedc9103FB21c038050D0"; // Sepolia 0.26const revocable = true;const transaction = await schemaRegistry.register({  schema,  resolverAddress,  revocable,});// Optional: Wait for transaction to be validatedawait transaction.wait();
```

## Learn about the Schema Contract 📄[​](#learn-about-the-schema-contract- "Direct link to heading")

Schemas are registered through the `SchemaRegistry.sol` contract. [Explore the entire contract on GitHub.](https://github.com/ethereum-attestation-service/eas-contracts/blob/master/contracts/SchemaRegistry.sol)

The contract enables users to register a schema that specifies the data format for a particular type of attestation. Additionally, a schema resolver contract can be employed to verify the attestation data.

[Edit this page](https://github.com/ethereum-attestation-service/eas-docs-site/blob/main/docs/tutorials/create-a-schema.md)

[

Previous

Tutorials

](/docs/category/tutorials)[

Next

Make an Attestation

](/docs/tutorials/make-an-attestation)

- [Schema Fields](#schema-fields)
- [The Schema Record](#the-schema-record-1)
- [Understanding the EAS schema record](#understanding-the-eas-schema-record)
- [Making Schemas 🧙](#making-schemas-)
    - [No-Code Schema Builder](#no-code-schema-builder)
    - [Use the SDK](#use-the-sdk)
- [Learn about the Schema Contract 📄](#learn-about-the-schema-contract-)

Docs

- [Welcome to EAS](/docs/welcome)
- [Learn](/docs/category/learn)
- [Getting Started](/docs/category/getting-started)
- [Tutorials](/docs/category/tutorials)
- [Technical Docs](/docs/category/technical-docs)

Community

- [Twitter](https://twitter.com/eas_eth)
- [Github](https://github.com/ethereum-attestation-service)

More

- [Mirror Articles](https://mirror.xyz/0xeee68aECeB4A9e9f328a46c39F50d83fA0239cDF)

Copyright © 2023 Ethereum Attestation Service. Built by the Ethereum Community.