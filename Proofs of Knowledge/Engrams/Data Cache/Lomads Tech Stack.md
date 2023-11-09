 

![🔄](https://lomads.notion.site/Lomads-Tech-Stack-2ef36ef269124eb49cf80bb398d8a266data:image/gif;base64,R0lGODlhAQABAIAAAP///wAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==)

Lomads Tech Stack

Search

Try Notion

![🔄](https://lomads.notion.site/Lomads-Tech-Stack-2ef36ef269124eb49cf80bb398d8a266data:image/gif;base64,R0lGODlhAQABAIAAAP///wAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==)![🔄](https://notion-emojis.s3-us-west-2.amazonaws.com/prod/svg-twitter/1f504.svg)

# Lomads Tech Stack

## Tech Architecture

![](https://lomads.notion.site/Lomads-Tech-Stack-2ef36ef269124eb49cf80bb398d8a266/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fc81d34a8-45b1-439d-98f7-2fb30d8001e3%2FUntitled_(15).jpg?table=block&id=9d8b1cfd-4f5b-47ae-aef4-361354b688a6&spaceId=efd63b0b-01a2-4772-92ec-bf2e49c9a525&width=2000&userId=&cache=v2)

## Tech Stack

![](https://lomads.notion.site/Lomads-Tech-Stack-2ef36ef269124eb49cf80bb398d8a266/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fbacf76b2-da1f-4fb4-afa7-659b40560bda%2FUntitled_(16).jpg?table=block&id=72b78d40-0b54-4833-a8a0-ed87cd70f55a&spaceId=efd63b0b-01a2-4772-92ec-bf2e49c9a525&width=1200&userId=&cache=v2)

#### Web 3 Network Layer

Web3 applications are built on top of blockchain architectures for trustless and permissionless access. Some points to consider:

Fast Transactions

Low gas fees

Decentralized exchange ([DEX](https://coinmarketcap.com/alexandria/glossary/decentralized-exchange-dex)) and Stablecoins

Smart contracts

Community

Support

Lomads is currently live on

Polygon

Ethereum

#### Web3 Development Environments

Hardhat / Truffle

Anchor

#### File storage

IPFS

Arweave

#### Off chain data protocols

In addition to file storage and on-chain storage, you may also need to store data off-chain.

Ceramic Network

#### Node Provider

Node in a blockchain serves as a “mini-server” that allows its operator to read/write blocks of data

Alchemy

#### API (indexing & querying)

The Graph

#### Identity

In web3, identity revolves completely around the idea of wallets and [public key cryptography](https://blog.mycrypto.com/the-basics-of-public-key-cryptography)

Wallet connect

Social Login to create a Wallet (Web3Auth and Aikon)

#### Client (frameworks and libraries)

[web3.js](https://web3js.readthedocs.io/en/v1.5.2/)

[ethers.js](https://docs.ethers.io/v5/)

#### Oracles

Oracles allow developers access to read real-world data & external systems from within a smart contract

Chainlink

#### Frontend Libraries

Reactjs

[

![🛡️](https://lomads.notion.site/Lomads-Tech-Stack-2ef36ef269124eb49cf80bb398d8a266data:image/gif;base64,R0lGODlhAQABAIAAAP///wAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==)

Data Protection Setup



](/Data-Protection-Setup-942ab1f5ee0148949ec9b01557c3dc5f?pvs=25)

## Gnosis Safe and SBT Contracts

Gnosis Safe: We are using the Gnosis Safe Core SDK to access the smart contracts. The SDK picks up the smart contracts automatically based on the chain id.

[

github.com

https://github.com/safe-global/safe-deployments/tree/main/src/assets/v1.3.0





](https://github.com/safe-global/safe-deployments/tree/main/src/assets/v1.3.0)

Example: For Base Chain

> safeMasterCopyAddress: '0x69f4D1788e39c87893C980c06EdF4b7f686e2938', safeProxyFactoryAddress: '0xa6B71E26C5e0845f74c812102Ca7114b6a896AB2', multiSendAddress: '0x998739BFdAAdde7C933B942a68053933098f9EDa', multiSendCallOnlyAddress: '0xA1dabEF33b3B82c7814B6D82A79e50F4AC44102B', fallbackHandlerAddress: '0x017062a1dE2FE6b99BE3d9d37841FeD19F573804', signMessageLibAddress: '0x98FFBBF51bb33A056B08ddf711f289936AafF717', createCallAddress: '0xB19D6FFc2182150F8Eb585b79D4ABcd7C5640A9d',

Example: For Gnosis Chain

> safeMasterCopyAddress: '0x69f4D1788e39c87893C980c06EdF4b7f686e2938', safeProxyFactoryAddress: '0xC22834581EbC8527d974F8a1c97E1bEA4EF910BC', multiSendAddress: '0xA238CBeb142c10Ef7Ad8442C6D1f9E89e07e7761', multiSendCallOnlyAddress: 'x40A2aCCbd92BCA938b02010E17A5b8929b49130D', fallbackHandlerAddress: '0xf48f2B2d2a534e402487b3ee7C18c33Aec0Fe5e4, signMessageLibAddress: '0xA65387F16B013cf2Af4605Ad8aA5ec25a2cbA3a2', createCallAddress: '0x7cbB62EaA69F79e6873cD1ecB2392971036cFAa4',

SBT Contract address: 0x662822aDbE18f1d5Eb60fCcb5C8A40cBD42037bC

[https://polygonscan.com/address/0x662822aDbE18f1d5Eb60fCcb5C8A40cBD42037bC](https://polygonscan.com/address/0x662822aDbE18f1d5Eb60fCcb5C8A40cBD42037bC)

#### Biconomy Contract Address

Based on the chain

For example for Polygon

BICONOMY_FORWARDER_ADDRESS: '0xf0511f123164602042ab2bCF02111fA5D3Fe97CD'

BICONOMY_GAS_TANK_ADDRESSES: '0xeb808ba857a080d35554fe5830dc61df1ba53e0c'

For example for Gnosis

BICONOMY_FORWARDER_ADDRESS: '0x86C80a8aa58e0A4fa09A69624c31Ab2a6CAD56b8'

BICONOMY_GAS_TANK_ADDRESSES: '0x64CD353384109423a966dCd3Aa30D884C9b2E057'