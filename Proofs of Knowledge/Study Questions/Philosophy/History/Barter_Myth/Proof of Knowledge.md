# DeSciWorld Protocol Specification Update: Proof-of-Knowledge Mechanism

The DeSciWorld protocol introduces a revolutionary system of attributing value to knowledge by leveraging blockchain technology. We call this system Proof-of-Knowledge (PoK). This mechanism incentivizes knowledge contributions within the DeSciWorld ecosystem, making it a self-sustaining environment for free and open research.

Here is a more technical specification of the PoK mechanism:

## 1 Proof-of-Knowledge Mechanism
In the DeSciWorld protocol, knowledge worth is evaluated in a two-step process: knowledge submission, and knowledge validation & appreciation.

### 1.1 Knowledge (Engram) Submission
The first step is the submission of a Study Question by a user (Nerd). Each Study Question (SQ) is an atomic, indivisible unit of knowledge. The properties of a SQ include:

1. Question text/data: The core content of the question being posed.
2. Metadata: Data that provides information about the SQ, including subject, authorship, complexity level, amongst others.
3. Unique SQ ID: A unique identifier for the Study Question.

SQs are registered in the DeSciWorld Blockchain, securing the timestamp and authorship details. When a SQ is first submitted, it is stamped with a freshly minted Non-Fungible Token (NFT) that represents ownership and the unique identity of the Question. 

### 1.2 Knowledge (Engram) Validation & Value Attribution
After the Study Question has been submitted and saved on-chain, it undergoes a validation process. Validators on the DeSciWorld network independently review the new SQ for its correctness, clarity, relevance, and novelty. Their validation scores impact the initial value assigned to the question. 

The value of a SQ is not static, though. It increases organically based on usage metrics obtained through the advanced AI-based search system. Popular SQs that gain a lot of attention (judged by the number of views, shares, upvotes etc.) or are referenced in major new discoveries accumulate more value over time.

An SQ's value is intrinsically linked to its usage in the network. Usage triggers a royalty mechanism that rewards the author/owner of the SQ with DST tokens, fostering an environment conducive to continuous learning and knowledge sharing.

## 2 Search and Usage Metrics
The AI-based search system plays a critical role in the DeSciWorld network. Users use it to search for specific Engrams, Study Questions, or topics. Each relevant interaction with an Engram or SQ acquires and sends usage data to the Proof-of-Knowledge mechanism.

User interactions can include activities like:
- How many times an SQ is retrieved in search results.
- The frequency with which it is selected from the results.
- The number of direct or indirect references made to it in new SQs.
- Assessments of how helpful the SQ was in a user’s research or learning process.

As users interact with the Engrams or Study Questions, the system measures these interactions and uses them as a basis for adjusting the value of each Engram or SQ. The more an Engram is recognized as useful or critical to ongoing research or learning, the more value it gains in the system, and the more rewards are distributed to the Nerd who contributed it.

This process ensures relevant, high-quality SQs are rewarded over time, and their contributors stay incentivized to add more to the DeSciWorld network.

## 3. Conclusion
The Proof-of-Knowledge (PoK) mechanism in the DeSciWorld network leverages blockchain technology to incentivize contributions and validate the accuracy and relevance of the knowledge within the ecosystem. It is a dynamic system that adapts to the changing needs and areas of interest of users, continually promoting a higher standard of shared knowledge.