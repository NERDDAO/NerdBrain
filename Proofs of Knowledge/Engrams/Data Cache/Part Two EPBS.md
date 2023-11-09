## Part Two: The Current Landscape

When Ethereum transitioned from Proof of Work (PoW) to Proof of Stake (PoS), the landscape of transaction validation and block proposal significantly changed. While PoW relied on miners and computational power (hash rate) to validate and add new blocks to the blockchain, PoS shifted this responsibility to validators who would _stake_ their ETH to become block proposers.

MEV GETH was being used by nearly all the mining pools, but with Ethereum transitioning to PoS, the system required modifications. PoS was designed to accommodate solo stakers: individual validators operating on low resource devices like a Raspberry Pi. PoS was designed with the goal of ensuring a balanced landscape: whether you're a solo staker or part of a substantial staking pool, there would be no inherent advantage in the validation process for any participant. Prior to the PoS transition, a few mining pools dominated the hash rate. This allowed for a trusted relationship between these pools and the Flashbots Relay. Any dishonest actions, such as a mining pool stealing MEV from a searcher, could jeopardize this relationship. Say a miner received a bundle with a sandwich attack from a searcher. If the miner further sandwiched the searcher with their own transactions, it would bring short term gain, but it would sever ties with Flashbots, costing them future MEV earnings because they would lose access to the Flashbots Relay.

### _Introducing MEV Boost_

Solo stakers, unlike large mining pools, might not have long term motivations to maintain trust. In certain scenarios, they could find it more profitable to exploit the MEV from a builder and subsequently disappear from the network. This action would result in them being fully slashed, losing all 32 ETH, but in some cases, the potential profit from stealing the MEV can outweigh this loss. This indeed occurred in April, when a rogue validator swiped $20M from a sandwich bot before shutting down their validator. [Further reading on this incident](https://eigenphi.substack.com/p/how-did-a-malicious-validator-steal).

In response to this new attack vector, Flashbots rolled out MEV Boost, a system designed for an environment with solo stakers.

The Mechanics of MEV Boost:

1. **Relays:** Unlike the previous system where only Flashbots acted as the relay, MEV Boost democratizes this. Now, anyone can serve as a relay, broadening participation and security. Flashbots has also open-sourced their relayer code.
    
2. **Builders:** A new role emerges - the Builder. These entities collect transaction bundles from searchers and combine them into complete blocks.
    
3. **Auction System:** Builders make bids to include their full block and submit them to the relays. The relays perform a crucial verification step to ensure block validity.
    
4. **Validator Interaction:** The relays forward the highest bid, along with the respective block header, they receive from the competing builders to the validator who’s turn it is to propose a block to the Ethereum network.
    
5. **Block Commitment:** The designated validator signs the block header, which is a commitment. Once signed, they are bound to that block. If they attempt to sign a another block that would be seen as a malicious act and they would be slashed.
    
6. **Final Proposal:** With a commitment in place, the relay sends the full block details to the validator, and it’s formally proposal to the network.
    

![The MEV Boost process](https://mirror.xyz/0x218932707a30bE62Ef8559d32d954863933b412f/MhJM9li409wxuOSYaw5EcLjUQoLSx5iYZXZNgMZU4uM/_next/image?url=https%3A%2F%2Fimages.mirror-media.xyz%2Fpublication-images%2FeZJWdPFPZrkgK4VhjphGW.png&w=3840&q=75)

The MEV Boost process

This setup introduces trust issues:

- **Builder-Relay Trust:** Builders need to trust that relays won't steal their MEV. Consider a scenario where a relay, after receiving a block from a builder, swaps out the builder's address in a sandwich transaction for its own. Then they pass manipulated header on to the proposer.
    
- **Proposer-Relay Trust:** Proposers, on the other hand, must trust that the block headers they sign are valid. Proposing an invalid block would result in the forfeiting the block rewards since the network would reject such a block.
    

PBS designs see a recurring challenge: while interactions between the proposer and transaction ordering actors are a given, there's a clear need for a mechanism where:

1. Proposers can commit to a builder's block without knowing its contents but remain assured of the block's validity.
    
2. Builders can safely send their block to the proposer, confident that their MEV won’t be stolen.
    

![MEV Boost trust assumptions](https://mirror.xyz/0x218932707a30bE62Ef8559d32d954863933b412f/MhJM9li409wxuOSYaw5EcLjUQoLSx5iYZXZNgMZU4uM/_next/image?url=https%3A%2F%2Fimages.mirror-media.xyz%2Fpublication-images%2FjaPExe7bReV7L-6Wo3r6R.png&w=3840&q=75)

MEV Boost trust assumptions

Before diving deeper into MEV Boost, it's essential to understand the default way Ethereum creates blocks without the use of MEV Boost. This setup hinges on the collaboration between a validators Execution Client and Consensus Client. When a transaction is received by the Execution Client, it checks the format, adds it to its mempool, but doesn't process it. Simultaneously, the Consensus Client handles the PoS consensus, picking a validator to create the next block. The selected validator's Execution Client then arranges transactions by gas price into a new block, which is then forwarded to the Consensus Client and put forth to the network. Other validators attest to the block's accuracy, and once verified, it becomes the chain's newest link.

This process changes if the validator opts to use MEV Boost. Validators integrating MEV Boost do so with their consensus client. When they're up to propose a block, they don't rely on their Execution Client anymore and instead connect to a network of relays. Validators can choose which relays to connect to.

MEV Boost is optional, but 95% of validators are utilizing it. Essentially almost every validator, except those run by Vitalik, are delegating block building to a third party. This delegation indicates that a core function of the Ethereum protocol, block building, is now primarily conducted outside of the Ethereum system itself. One key player in this setup is the relay and their role somewhat contrasts with Ethereum's foundational principles. Presently, there are around 9 active relays, but only 6 of them have >9% share of blocks relayed.

![Breakdown of Top Relays and Builders by Market Share in the past 7d. Source: https://www.relayscan.io/](https://mirror.xyz/0x218932707a30bE62Ef8559d32d954863933b412f/MhJM9li409wxuOSYaw5EcLjUQoLSx5iYZXZNgMZU4uM/_next/image?url=https%3A%2F%2Fimages.mirror-media.xyz%2Fpublication-images%2FHIos6fK1hNtLunH2T-C5f.png&w=3840&q=75)

Breakdown of Top Relays and Builders by Market Share in the past 7d. Source: https://www.relayscan.io/

Trust becomes an issue since the relationship between the relays and the builder and the relay and the validator isn't trustless. There's also a concern about censorship resistance. Relays, during their auctions, have the discretion to determine the validity of blocks. This discretion allows them to exclude blocks with transactions linked to sanctioned addresses. A case in point is when the OFAC Tornado Cash sanctions happened some relays exercised this power. Recent data shows that 38% of blocks in the past week adhered to OFAC guidelines due to such relay imposed censorship.

![](https://mirror.xyz/0x218932707a30bE62Ef8559d32d954863933b412f/MhJM9li409wxuOSYaw5EcLjUQoLSx5iYZXZNgMZU4uM/_next/image?url=https%3A%2F%2Fimages.mirror-media.xyz%2Fpublication-images%2F0lp3XkBCMfqKiAOH5MGqA.png&w=3840&q=75)
