**Key Insights from Part 2**

1. Ethereum's transition from PoW to PoS necessitated a change in the MEV GETH system since PoS was designed to accommodate individual, low-resource validators or "solo stakers."

2. MEV Boost was introduced by Flashbots to address potential trust issues with solo stakers who might be motivated to exploit MEV. 

3. The main components of MEV Boost are: 
    - Relays: Anyone can serve as a relay, thereby broadening participation and security. 
    - Builders: A new role introduced that collects transactions and forms full block
    - Auction System: Bidding system for block inclusion and validation
    - Validator Interaction: Highest bid forwarded by relays to the validator
    - Block Commitment: Validators bound to their chosen block; attempting to switch construed as a malicious act
    - Final Proposal: Block proposal formalized and submitted to the network

4. Trust issues emerged due to Builder-Relay and Proposer-Relay relationships as the actors needed to trust each other not to manipulate MEV or blocks.

5. Ethereum block formation relied on collaboration between a validator's Execution Client (handling transactions) and Consensus Client (handling PoS consensus).

6. All validators can choose to use MEV Boost, but integration is not mandatory - however, it's worth noting that around 95% of validators utilize it.

7. This delegation of block building to third parties indicates a significant shift in Ethereum's core function.

8. Relays also hold the power to exercise censorship over blocks, potentially excluding transactions linked to sanctioned addresses.

**Emoji Summary**
💻 ⇄ 🔀🗳️⚖️🎰🔒📤🔎🔄🕵️‍♀️🤝🔐🔍