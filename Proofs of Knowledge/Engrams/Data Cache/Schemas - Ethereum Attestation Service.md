[Skip to main content](#docusaurus_skipToContent_fallback)

[

![EAS Logo](https://docs.attest.sh/docs/core--concepts/schemas/img/eas-logo.png)

**Ethereum Attestation Service**](/)

[EAS Explorer](https://easscan.com/)[EAS Website](https://attest.sh/)[GitHub](https://github.com/ethereum-attestation-service)

Search...

- [Welcome to EAS](/docs/welcome)
- [Purpose](/docs/category/purpose)
    
- [Quick Start](/docs/category/quick-start)
    
- [Core Concepts](/docs/category/core-concepts)
    
    - [How EAS Works](/docs/core--concepts/how-eas-works)
    - [Attestations](/docs/core--concepts/attestations)
    - [Schemas](/docs/core--concepts/schemas)
    - [Onchain vs Offchain](/docs/core--concepts/onchain-vs-offchain)
    - [Attestations vs X](/docs/core--concepts/attestations-vs-x)
    - [Privacy](/docs/core--concepts/privacy)
    - [Composability](/docs/core--concepts/composability)
    - [Resolver Contracts](/docs/core--concepts/resolver-contracts)
    - [Delegating](/docs/core--concepts/delegated-attestations)
    - [Revocation](/docs/core--concepts/revocation)
    - [Credible Neutrality](/docs/core--concepts/credible-neutrality)
- [Developer Tools](/docs/category/developer-tools)
    
- [Tutorials](/docs/category/tutorials)
    
- [The Explorer](/docs/category/the-explorer)
    
- [Ideas to Build](/docs/category/ideas-to-build)
    

- [](/)
- [Core Concepts](/docs/category/core-concepts)
- Schemas

On this page

# Schemas

What are schemas?

Schemas define the structure and type of data that can be included in an attestation. They act as a blueprint for the information being attested to, ensuring consistency and clarity.

## Understanding Schemas[​](#understanding-schemas "Direct link to heading")

At its core, a schema is a structured framework that outlines the format of the data. In the context of EAS, schemas are essential because they ensure that attestations are consistent, readable, and verifiable. They dictate what kind of information can be attested to and how that information should be presented.

*Example Schema for "Making a Statement". It's simply just a `message string` schema. Notice that each schema has a UID

![Make a Statement Schema](https://docs.attest.sh/docs/core--concepts/schemas/assets/images/make-a-statement-schema-ba810106a2bda5c6b819b39517ca5ffe.png)

**Each schema record has the following fields:**

- `Schema #` - this is an incremental number automatically assigned to the Schema. It is not a unique identifier.
- `UID` - this is the unique universal identifier assigned to the schema.
- `Creator` - the wallet address that created the schema.
- `Transaction ID` - the Ethereum transaction registering the schema on EAS.
- `Resolver Contract` - An optional contract assigned to the Schema for more complex use cases.
- `Attestation Count` - The amount of attestations that have been made with attestations on/off chain.
- `Schema` - The ABI encoded schema field types.

### How Schemas Are Made[​](#how-schemas-are-made "Direct link to heading")

The [SchemaRegistry.sol](https://github.com/ethereum-attestation-service/eas-contracts/blob/master/contracts/SchemaRegistry.sol) contract is how schemas are made and registered.

```
/// @notice A struct representing a record for a submitted schema.struct SchemaRecord {    bytes32 uid; // The unique identifier of the schema.    ISchemaResolver resolver; // Optional schema resolver.    bool revocable; // Whether the schema allows revocations explicitly.    string schema; // Custom specification of the schema (e.g., an ABI).}
```

**🎓 Tutorial:** [**Make a Schema**](/docs/tutorials/create-a-schema)

## Building Efficient Schemas[​](#building-efficient-schemas "Direct link to heading")

When designing a schema, it's crucial to strike a balance between specificity and flexibility. Here are some guidelines:

- **Keep it Simple:** A schema should be concise. Avoid unnecessary complexity.
- **Be Descriptive:** Each field should have a clear purpose and name.
- **Avoid Redundancy:** Ensure each piece of information is captured once.
- **Plan for the Future:** Design your schema to be extendable without breaking existing attestations.
- **Gas Efficiency:** Consider the Ethereum gas costs. Using the right data types and thinking modularly will help reduce costs.

**📘 Read More:** [**Gas Efficiency Tutorial**](/docs/tutorials/gas-efficiency)

## Composability and Modularity[​](#composability-and-modularity "Direct link to heading")

One of the strengths of EAS is its ability to create composable attestations. This principle can be applied to schemas as well:

- **Think Modular:** Instead of creating a monolithic schema that tries to capture everything, build smaller, modular schemas that can be combined as needed.
- **Reuse and Recombine:** Generalized schemas can be reused across different attestations. For instance, an `isTrue bool` schema can be applied in numerous contexts.

### Modular Schema Example: Event Attendance[​](#modular-schema-example-event-attendance "Direct link to heading")

Imagine you want to attest to someone attending an event:

- **Event Registration Schema:** This schema registers the event itself. It might include the event name, date, and venue.
- **Attendance Schema:** This schema attests to a person's attendance. Instead of repeating all the event details, it simply references the UID of the event from the Event Registration Schema.

This approach avoids data repetition and keeps the attestations lean and efficient.

## Collaborative Schema Development[​](#collaborative-schema-development "Direct link to heading")

While EAS provides the tools to create custom schemas tailored to specific needs, it also encourages collaboration. If you believe your schema has broader applicability beyond just your brand or project, it's beneficial to get input from the wider community. This collaborative approach ensures:

- **Standardization:** Common use cases can have standardized schemas, ensuring consistency across different projects.
- **Composability:** Schemas that are designed with input from various stakeholders are more likely to be composable, meaning they can be easily combined or used alongside other schemas.
- **Wider Adoption:** A schema that has been discussed and refined with community input is more likely to see wider adoption.

## Generalized vs. Complex Schemas[​](#generalized-vs-complex-schemas "Direct link to heading")

- **Generalized Schemas:** These are broad and can be applied in many situations. An example is the `isTrue` schema, which simply verifies the truth of a statement. Such schemas are versatile and can be used for a myriad of use cases.
    
- **Complex Schemas:** These are tailored for specific needs and are often built by communities or groups with shared interests. For instance, a schema for verifying art authenticity might include fields for the artist's name, artwork medium, creation date, and provenance.
    

Start a discussion

Coordination around schemas is crucial. If you have a more complex schema in mind for a particular use case, start a discussion on our forum.

## Naming and Contextualizing Schemas[​](#naming-and-contextualizing-schemas "Direct link to heading")

With EAS, you can use attestations to add more depth to your schemas:

- **Naming a Schema:** Instead of hardcoding a name within the schema, you can create an attestation that links a name to a schema's UID. This approach is more flexible and allows for names to evolve without altering the schema itself.
    
- **Add a Description:** Descriptions help others understand the purpose of your schema. You can easily set a description by making a referenced attestation to the schema `UID`. Simply use the "Schema Description" on any chain.
    
- **Providing Context:** Similarly, you can attest to the context or intended use of a schema. Simply reference the schema's UID, you can provide additional information or examples of how the schema should be used, without bloating the schema itself.
    

**🎓 Tutorial:** [**Naming a Schema**](/docs/tutorials/naming-your-schema)

**🎓 Tutorial:** [**Adding a Description**](/docs/tutorials/schema-description)

**🎓 Tutorial:** [**Adding Context to a Schema**](/docs/tutorials/naming-your-schema)

## Conclusion[​](#conclusion "Direct link to heading")

Schemas are foundational to the EAS ecosystem. They ensure that attestations are consistent, verifiable, and meaningful. Builders that think modularly, embrace composability, and leverage the power of attestations, can create powerful and flexible schemas that cater to a wide range of use cases.

[Edit this page](https://github.com/ethereum-attestation-service/eas-docs-site/blob/main/docs/core--concepts/schemas.md)

[

Previous

Attestations

](/docs/core--concepts/attestations)[

Next

Onchain vs Offchain

](/docs/core--concepts/onchain-vs-offchain)

- [Understanding Schemas](#understanding-schemas)
    - [How Schemas Are Made](#how-schemas-are-made)
- [Building Efficient Schemas](#building-efficient-schemas)
- [Composability and Modularity](#composability-and-modularity)
    - [Modular Schema Example: Event Attendance](#modular-schema-example-event-attendance)
- [Collaborative Schema Development](#collaborative-schema-development)
- [Generalized vs. Complex Schemas](#generalized-vs-complex-schemas)
- [Naming and Contextualizing Schemas](#naming-and-contextualizing-schemas)
- [Conclusion](#conclusion)

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