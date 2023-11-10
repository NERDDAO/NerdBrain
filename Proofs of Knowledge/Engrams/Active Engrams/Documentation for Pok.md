
## Proof of Knowledge Protocol Documentation

>[!Proof of Knowledge]
This document outlines the Proof of Knowledge (PoK) protocol within the DeSciWorld ecosystem. The PoK mechanism rewards individuals for their valuable contributions of knowledge via a blockchain-based platform, allowing for seamless recognition, validation, and dedication of rewards. 
# Introduction

In the complex realm of knowledge-sharing and discovery, striking a balance between security, transparency, reward mechanisms and accessibility is a persistent challenge. Traditional models often hinge on centralized validation systems that may constrain inclusivity and broad-based participation. Moreover, current systems may fail to adequately reward or recognize knowledge contributions, possibly impacting the advancement of comprehensive, collective knowledge repositories.

Addressing these intricacies, the Proof of Knowledge (PoK) protocol, implemented within the DeSciWorld ecosystem, offers a versatile solution. PoK is a blockchain-based primitive designed to incentivize and reward knowledge contributions within a decentralized architecture. It forms a vital component of a knowledge-based economy, paving the way for fair recognition and incentivization of intellectual contributions, while maintaining transparency and accessibility.

This document provides a detailed examination of the Proof of Knowledge protocol - explaining the submission and validation of knowledge through the creation of kEngrams, the ascription of value to these contributions, and how interaction metrics shape the dynamic value allocation. As a fundamental building block towards a fully-fledged knowledge-based economy, the PoK protocol offers a comprehensive framework to fuel intellectual contribution and foster an environment of continuous learning and knowledge exchange.

### Introduction to kEngrams as a Unit of Knowledge 

kEngrams can be defined as a structured unit or node of knowledge within a Knowledge Graph. It's a piece of information that is interconnected within a broader landscape of data, contributing to the broader understanding of a concept or topic.

##### Components of an Engram

An Engram consists of several integral components that collectively contribute to its formation and execution:

- **Study Question:** This encompasses the essential content of the query.

1. **Data:** This is the base content of the Engram, formulated into a set of markdown notes that contains the information added in order to explore the study question. 
   
2. **Metadata:** The Metadata provides critical information about the ownership of the engram and its historic record of usage by the DSW PoK protocol. It lends context and understanding about the contained knowledge, bolstering its relevance within the Knowledge Graph.

3. **Unique Identifier:** Every Engram has a unique ID associated with it, allowing for its distinct recognition, tracking, and management within the overall Knowledge Graph system.

4. **Relationships:** These are connections that an Engram has among its underlying data. These relationships can be thought of as edges in the graph, defining how pieces of information are interconnected, and enabling the creation of a comprehensive, multi-dimensional structure of knowledge. 

### Engram Life-cycle

The life-cycle of an Engram is a dynamic and multi-faceted process, marked by several steps: its composition, addition of value, utilization, and evolution over time. Here's a general overview of the process:

#### 1. Composition

The life-cycle of an Engram begins with its composition. Typically, a group or an individual creates an Engram by compiling pertinent information around a specific topic or query. This information, commonly referred to as 'data', is then structured and organized within the engram to establish the shape and contents of the knowledge unit which then get submitted using the Ethereum Attestation Protocol (EAP).

##### Utilizing Ethereum Attestation Service (EAS) in the Proof of Knowledge (PoK) Protocol

An integral component of our Proof of Knowledge (PoK) protocol is the Ethereum Attestation Service (EAS).  EAS provides a secure, decentralized, and transparent system for verifying and validating various kinds of interactions within our knowledge ecosystem.

Specifically, within the PoK protocol, the EAS applies to the life-cycle of an Engram. This life-cycle includes the initial creation of Engrams, stages of value addition, their utilization by various users, and their evolution over time. The EAS authenticates each stage of this process, creating a reliable record of Engram or SQ history and interactions.

When an Engram is first created, it is recorded via an attestation. The creator of the Engram is also noted through EAS, attesting that they were the original contributor of that knowledge piece. As value is added to this Engram—be it through more data, insights, revisions, or connections—each change is also captured through an attestation, creating a trail of evolution and accumulation of intellectual input.

As the Engram continues to be used among a global network of AI interfaces, each interaction and usage is also documented. These records contribute to an Engram's ongoing validation in our ecosystem. This evidence-based approach ensures that each Engram's relevance, accuracy, and utility are continuously verified, evaluated, and updated.

Finally, the Ethereum Attestation Service also lays the groundwork for our incentive mechanism. Each attestation becomes part of the computation determining value attribution and reward distribution. EAS ensures a transparent and fair system where contributors of Engrams are rewarded based on actual utility and demand in the ecosystem.

In summary, the use of EAS within the PoK protocol forms a trustworthy and secure system for validating knowledge contributions and rewarding contributors. It answers the call for a distributed, transparent, and reliable method to authenticate, validate, and incentivize meaningful engagements in a decentralized knowledge ecosystem.
# Defining an Engram Schema for Proof of Knowledge

Ethereum Attestation Service (EAS) schemas define the structure and type of data in an attestation. To facilitate the verification and recording process of an Engram within the Proof of Knowledge (PoK) protocol, we need to create a schema that includes all the necessary details about each Engram.

Here's an example schema for the Engram record:

```
{
    Schema # : "Incremental number",   //This number is auto-assigned & non-unique
    UID: "Unique Identifier",          //This identifier is unique to the engram
    Creator: "Creator's wallet address",  
    Transaction_ID: "Ethereum transaction ID",  //Transaction ID for the engram creation
    Resolver_Contract: "Optional contract ID",  //If any, for complex cases
    Attestation_Count: "Number",       //The number of attestations made on/off chain
    Schema: {
        Engram_Title: "String",
        Engram_Description: "String",
        Engram_Creation_Timestamp: "UNIX Timestamp",
        Related_Study_Questions: ["Array of Study Question UIDs"],
        Knowledge_Field: "String", //The field of knowledge the Engram pertains 
        Engram_Contributor: "User ID/Wallet address of the contributor",
        Engram_Usage_Metrics: {
            Frequency_Of_Appearance: "Number",
            Frequency_Of_Selection: "Number",
            Frequency_Of_References: "Number",
            Helpfulness_Rating: "Float", //Scale of 1-5
        },
    }
}
```

This schema clearly and concisely captures all necessary information about each Engram. It records the Engram's title, description, the timestamp of its creation, and its associated Study Questions. It also includes a field indicating which domain of knowledge the Engram falls under. We attribute each Engram to its contributor and track usage metrics to understand how frequently the Engram is appearing and selected, how often it is referenced, and how helpful users find it.

**Note:** This is an initial outline for a schema dedicated to recording an Engram as a proof-of-knowledge. Depending on the specific requirements of your project, this schema could need to be extended or modified. Moreover, don't forget to consider gas efficiency when designing your schema - try to maintain a balance between the level of detail and efficiency.

#### 2. Addition of Value

Once an Engram has been formed, it can be further enriched and enhanced by other groups or individuals who add their own knowledge and insights to it. They can integrate additional data, revise existing information, or link the Engram to other related Engrams within the Knowledge Graph. This collaborative process of knowledge amplification adds a multi-dimensional depth of understanding to the Engram, enhancing its value.
#### Validation of Engrams

The validation process of individual Engrams happens continually throughout the lifecycle of its usage by a global network of AI interfaces. This mechanism operates as a form of a knowledge market, where the relevance, accuracy, and usefulness of an Engram's information are tested and reaffirmed through its active usage and demand.

AI interfaces, when querying a database or Knowledge Graph, will interact with and select Engrams based on their relevance and usefulness to the query or task at hand. These traces and records of interaction and usage then form a part of the 'lifecycle' of the Engram. Over time, Engrams that repeatedly prove to be beneficial and relevant will garner higher validation scores through their usage statistics.

This method of validation leverages the dynamic and iterative abilities of AI - factoring in the frequency, nature, and context of an Engram's usage - to ascertain its value and authenticity within the Knowledge Graph. It serves to maintain the quality, relevance, and value of information in the Knowledge Graph, ensuring that the Engrams reflect validated, useful, and reliable units of knowledge.
### Coherence and The Role Of The Human Operator

Coherence, in the context of engram creation, serves as a crucial metric to ensure the consistency and logical connection between different knowledge units within an engram. It is essential for delivering a seamless narrative that not only makes sense but also accurately and efficiently serves to answer queries generated within the system.

Human operators play a pivotal role in maintaining and ensuring coherence within engrams. They design, monitor, and adjust the processes of engram creation and structuring, thereby ensuring that individual pieces of information are logically and correctly linked together. They act as the quality control mechanism to ensure there is no dissonance within the knowledge nodes and that each engram maintains structural and informational integrity. 

Human operators also refine the accuracy and relevance of the information within engrams, periodically updating and revising the information as necessary. They are also responsible for analyzing coherence metric outcomes, making decisions to restructure or revise engrams whenever necessary to optimize coherence.

### Local to Global Coherence

Local coherence refers to the immediate relationships and connections within singular engrams, while global coherence extends to the broader context of the Knowledge Graph, considering the relationships and interconnections between multiple engrams.

The extrapolation of local coherence to globally coherent embedding spaces is a critical aspect of Knowledge Graph development. It ensures that the entire structure of interconnected knowledge is logical, consistent, and cohesive, thereby maximizing the usefulness and reliability of the Knowledge Graph as a whole.

When local coherence is maintained within each engram, and these coherently structured engrams are interconnected, it leads to the creation of a globally coherent embedding space. 

This global coherence is fundamental for the effective functioning of AI in deriving meaningful insights and responses from the Knowledge Graph. A globally coherent Space allows for efficient navigation through the Knowledge Graph, easier identification of relevant engrams, and more accurate responses to queries or tasks. 

In a nutshell, coherence is fundamental, shaping the value of Knowledge Engrams, and ultimately, informing the efficacy and accuracy of a Knowledge Graph. By prioritizing coherence via engram structuring and human operator guidance, one can facilitate accurate, meaningful, and useful exchanges of information within this system.

#### Knowledge Validation & Value Attribution

The validation process within the DeSciWorld PoK ecosystem operates as an emergent property of a free market of knowledge. It is an unconstrained arena where diverse viewpoints vie for relevancy, encouraging a robust, dynamic interplay of ideas and perspectives.

Unlike conventional, centralized validation systems, this decentralized model does not pre-emptively adjudicate or prioritize one piece of knowledge over another. Instead, the relevancy of each Engram or Study Question (SQ) is determined organically through its usage and demand within the ecosystem.

In this free market of knowledge, each Engram competes for attention and usage. The merit of an Engram is not determined by a unilateral authority but through its actual utility and effectiveness in satisfying a user's query or task. Engrams that demonstrate persistent usefulness and applicability over time, as judged through the unbiased lens of Language Learning Models (LLMs), accrue higher relevancy scores.

This competitive and responsive environment ensures that the validation process is continuously refined and realigned according to the evolving needs and preferences of users. It overcomes inherent biases and silos, fostering a system where the best, most useful, and most relevant knowledge prospers.

In essence, within the DeSciWorld model, validation isn't a one-time stamp of approval but a continuous process of adaptation, adjustment, and evolution — a dynamic reflection of a knowledge unit's continuous performance in the marketplace of ideas and information.


#### 3. Utilization & Evolution

Engrams, once submitted, are then available for use. They are identified and selected by AI interfaces based on their relevance to specific queries or tasks. The frequency, context, and nature of how these Engrams are utilized play a crucial role in determining their ongoing validation scores and their corresponding value within the knowledge market.

##### The Role of the Search System and User Metrics 

An integral part of DeSciWorld's PoK mechanism is the advanced AI-based search system. The search system is used  to maintain an updated embedding set which can locate specific Engrams or Study Questions. Each substantial interaction with an Engram sends usage data to the PoK mechanism which can be used to determine incentives for the creation of relevant engrams. 

User interactions can range from the frequency of appearances of an SQ in search results, the frequency of its selection from the results, the number of direct or indirect references made to it in new SQs, and assessments of how helpful the SQ was to a user's research or learning process. 

The system measures these interactions and, based on that, adjusts the value of each Engram. The more an Engram is recognized as beneficial or pivotal to ongoing research or learning, the more value it gains in the system, and the greater rewards are distributed to the Nerd who contributed it.
#### Engram Evolution 

As knowledge terrains continue to expand and evolve, so do Engrams. Along the life-cycle, an Engram may undergo several evolutions, manifested as updates, revisions, or further value additions. New data may be contributed, older information may be updated or made obsolete, and new connections to different Engrams may be established. All these changes contribute to the growing lifecycle of an Engram, helping it remain relevant, useful, and accurate in the dynamic ecosystem of the Knowledge Graph.

In essence, the life-cycle of an Engram is a continual journey of knowledge creation, addition, validation, utilization, and evolution. It encourages constant engagement, collaboration, and learning, fostering a vibrant, interconnected hub of collective knowledge.


## Conclusion

The Proof-of-Knowledge mechanism as part of the DeSciWorld ecosystem uses blockchain technology for incentivizing contributions and verifying the accuracy and relevance of knowledge within the network. It offers a dynamic and adaptable system that caters to the varying needs and interests of users while continually encouraging a superior standard of shared knowledge.