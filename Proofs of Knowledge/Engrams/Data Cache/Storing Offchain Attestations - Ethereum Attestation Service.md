[Skip to main content](#docusaurus_skipToContent_fallback)

[

![EAS Logo](https://docs.attest.sh/docs/tutorials/storing-offchain-data/img/eas-logo.png)

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
- Storing Offchain Attestations

On this page

# Storing Offchain Attestations

When making an offchain attestation, you have the choice to decide where that data is stored. EAS does not presuppose where that data should live or how it should be used. Thus, by default, all offchain attestations are made `private`. The EASSCAN server doesn't even know that it exists.

## Undestanding the Data You Get[​](#undestanding-the-data-you-get "Direct link to heading")

When an offchain attestation is made on EASSCAN, you have the option to store it's raw data. Here's an example offchain attestation made using the `Make a Statement` schema on `Mainnet`. Remember, offchain attestations don't cost any gas!

![Sample Offchain Attestation](https://docs.attest.sh/docs/tutorials/storing-offchain-data/assets/images/sample-offchain-private-attestation-1acd62aa38a693636f5e28840b5e20e9.png)

### Download the Raw Data[​](#download-the-raw-data "Direct link to heading")

It will create a simple `.txt` file with the raw attestation data. It'll look like an unformatted version of the JSON object below.

```
{   "sig":{      "domain":{         "name":"EAS Attestation",         "version":"0.26",         "chainId":1,         "verifyingContract":"0xA1207F3BBa224E2c9c3c6D5aF63D0eb1582Ce587"      },      "primaryType":"Attest",      "types":{         "Attest":[            {               "name":"version",               "type":"uint16"            },            {               "name":"schema",               "type":"bytes32"            },            {               "name":"recipient",               "type":"address"            },            {               "name":"time",               "type":"uint64"            },            {               "name":"expirationTime",               "type":"uint64"            },            {               "name":"revocable",               "type":"bool"            },            {               "name":"refUID",               "type":"bytes32"            },            {               "name":"data",               "type":"bytes"            }         ]      },      "signature":{         "r":"0x948e36add4753524c1ff0224427bc964e1262c5239d73d749d44aaead6ae6320",         "s":"0x59f7d812eb10323204f115aa18315b238dac4da609b0b5aec4d5892a23d55029",         "v":27      },      "uid":"0x9daf896fdad6ecb405f86d94395fecd4902461a2276180c6fa1d5c979bbf97d5",      "message":{         "version":1,         "schema":"0xf58b8b212ef75ee8cd7e8d803c37c03e0519890502d5e99ee2412aae1456cafe",         "recipient":"0x0000000000000000000000000000000000000000",         "time":1694227180,         "expirationTime":0,         "refUID":"0x0000000000000000000000000000000000000000000000000000000000000000",         "revocable":true,         "data":"0x000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000495468697320697320616e206f6666636861696e206174746573746174696f6e2120436f6d706c6574656c7920707269766174652e2050617373656420706565722d746f2d706565722e0000000000000000000000000000000000000000000000",         "nonce":0      }   },   "signer":"0xeee68aECeB4A9e9f328a46c39F50d83fA0239cDF"}
```

### Download the QR[​](#download-the-qr "Direct link to heading")

The entire attestation data is compressed into the QR code so you can print it and verify it whenever needed.

![Private Offchain Attestation QR Code](https://docs.attest.sh/docs/tutorials/storing-offchain-data/assets/images/private-offchain-qr-7ff1366a963db20c162744520360f6c7.png)

## Copy the URL[​](#copy-the-url "Direct link to heading")

The offchain attestation is stored locally in your browser when it is first made. The entire attestation data is encoded in the URI fragment of the URL, including the signature.

[https://easscan.org/offchain/url/#attestation=eNqlUkuOXDEIvMtbtyLM1yy7p6cvEc3CNvgAo0TK8cN7ibKPxgtsClyUMd8P%2BIZ63NrtgF%2F3hmAvejwGIr%2Fj8kVLnzJeSk%2FI2aTjW0q340x27kk6ItiEBHm1vaHuMdpcrpwNFZcgeRiFsQfzGDlCRyohXCTi26I3LHIgLJR3azJG69RkIvUYi2Mo%2BIQpI8uR7jiQQgTQjxvayZOZ2sf7Wz747umbsA%2FWRf4SiE77DqVjPV9%2FlMfY3XVHack1GWR3DWdy2bmCHZC1VQ9MW4ele7SQ5eZzbreQi2RLn31iSd8mmX2FZY8OtMgWUII07w4lMiTdM5Eb1vsbi66x8ySptqtz1akyN7iAH58%2F86SHLy382nVgF9aubvUjf23TLLv1XFSxUn4hzdhYxahsnQvdhdcgMdUpDHRVtDJ0mdd4gWEx6pUrWAxycpBRZfAZr10MsSZGN8Y%2FP%2F%2FvBUf1s338Bv9RrMI%3D](https://easscan.org/offchain/url/#attestation=eNqlUkuOXDEIvMtbtyLM1yy7p6cvEc3CNvgAo0TK8cN7ibKPxgtsClyUMd8P%2BIZ63NrtgF%2F3hmAvejwGIr%2Fj8kVLnzJeSk%2FI2aTjW0q340x27kk6ItiEBHm1vaHuMdpcrpwNFZcgeRiFsQfzGDlCRyohXCTi26I3LHIgLJR3azJG69RkIvUYi2Mo%2BIQpI8uR7jiQQgTQjxvayZOZ2sf7Wz747umbsA%2FWRf4SiE77DqVjPV9%2FlMfY3XVHack1GWR3DWdy2bmCHZC1VQ9MW4ele7SQ5eZzbreQi2RLn31iSd8mmX2FZY8OtMgWUII07w4lMiTdM5Eb1vsbi66x8ySptqtz1akyN7iAH58%2F86SHLy382nVgF9aubvUjf23TLLv1XFSxUn4hzdhYxahsnQvdhdcgMdUpDHRVtDJ0mdd4gWEx6pUrWAxycpBRZfAZr10MsSZGN8Y%2FP%2F%2FvBUf1s338Bv9RrMI%3D)

## Publishing to IPFS[​](#publishing-to-ipfs "Direct link to heading")

We do have an option for you to make your `private offchain attestation` public by publishing it to IPFS. If you click on `Publish to IPFS` we will pin the attestation to IPFS and then index it for the EASSCAN explorer.

[Edit this page](https://github.com/ethereum-attestation-service/eas-docs-site/blob/main/docs/tutorials/storing-offchain-data.md)

[

Previous

Delegated Attestations

](/docs/tutorials/delegated-attestations)[

Next

Timestamping Attestations

](/docs/tutorials/timestamping-attestations)

- [Undestanding the Data You Get](#undestanding-the-data-you-get)
    - [Download the Raw Data](#download-the-raw-data)
    - [Download the QR](#download-the-qr)
- [Copy the URL](#copy-the-url)
- [Publishing to IPFS](#publishing-to-ipfs)

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