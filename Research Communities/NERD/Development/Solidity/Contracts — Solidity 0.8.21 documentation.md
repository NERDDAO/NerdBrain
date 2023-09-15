[![Solidity logo](https://docs.soliditylang.org/en/v0.8.21/contracts.html_static/img/logo.svg)](https://soliditylang.org)[{ skip to content }](#content)

[Blog](https://soliditylang.org/blog)[Documentation](/)[Use cases](https://soliditylang.org/use-cases)[Contribute](/en/latest/contributing.html)[About](https://soliditylang.org/about)[Forum](https://forum.soliditylang.org/)

![Color mode toggle icon](https://docs.soliditylang.org/en/v0.8.21/contracts.html_static/img/moon.svg)![Toggle menu](https://docs.soliditylang.org/en/v0.8.21/contracts.html_static/img/hamburger-light.svg)

v0.8.21

  

Basics

- [Introduction to Smart Contracts](introduction-to-smart-contracts.html)
- [Solidity by Example](solidity-by-example.html)
- [Installing the Solidity Compiler](installing-solidity.html)

Language Description

- [Layout of a Solidity Source File](layout-of-source-files.html)
- [Structure of a Contract](structure-of-a-contract.html)
- [Types](types.html)
- [Units and Globally Available Variables](units-and-global-variables.html)
- [Expressions and Control Structures](control-structures.html)
- [Contracts](#)
    - [Creating Contracts](#creating-contracts)
    - [Visibility and Getters](#visibility-and-getters)
        - [State Variable Visibility](#state-variable-visibility)
        - [Function Visibility](#function-visibility)
        - [Getter Functions](#getter-functions)
    - [Function Modifiers](#function-modifiers)
    - [Constant and Immutable State Variables](#constant-and-immutable-state-variables)
        - [Constant](#constant)
        - [Immutable](#immutable)
    - [Functions](#functions)
        - [Function Parameters and Return Variables](#function-parameters-and-return-variables)
            - [Function Parameters](#function-parameters)
            - [Return Variables](#return-variables)
            - [Returning Multiple Values](#returning-multiple-values)
        - [State Mutability](#state-mutability)
            - [View Functions](#view-functions)
            - [Pure Functions](#pure-functions)
        - [Special Functions](#special-functions)
            - [Receive Ether Function](#receive-ether-function)
            - [Fallback Function](#fallback-function)
        - [Function Overloading](#function-overloading)
            - [Overload resolution and Argument matching](#overload-resolution-and-argument-matching)
    - [Events](#events)
        - [Members of Events](#members-of-events)
        - [Example](#example)
        - [Additional Resources for Understanding Events](#additional-resources-for-understanding-events)
    - [Errors and the Revert Statement](#errors-and-the-revert-statement)
        - [Members of Errors](#members-of-errors)
    - [Inheritance](#inheritance)
        - [Function Overriding](#function-overriding)
        - [Modifier Overriding](#modifier-overriding)
        - [Constructors](#constructors)
        - [Arguments for Base Constructors](#arguments-for-base-constructors)
        - [Multiple Inheritance and Linearization](#multiple-inheritance-and-linearization)
        - [Inheriting Different Kinds of Members of the Same Name](#inheriting-different-kinds-of-members-of-the-same-name)
    - [Abstract Contracts](#abstract-contracts)
    - [Interfaces](#interfaces)
    - [Libraries](#libraries)
        - [Function Signatures and Selectors in Libraries](#function-signatures-and-selectors-in-libraries)
        - [Call Protection For Libraries](#call-protection-for-libraries)
    - [Using For](#using-for)
- [Inline Assembly](assembly.html)
- [Cheatsheet](cheatsheet.html)
- [Language Grammar](grammar.html)

Compiler

- [Using the Compiler](using-the-compiler.html)
- [Analysing the Compiler Output](analysing-compilation-output.html)
- [Solidity IR-based Codegen Changes](ir-breaking-changes.html)

Internals

- [Layout of State Variables in Storage](internals/layout_in_storage.html)
- [Layout in Memory](internals/layout_in_memory.html)
- [Layout of Call Data](internals/layout_in_calldata.html)
- [Cleaning Up Variables](internals/variable_cleanup.html)
- [Source Mappings](internals/source_mappings.html)
- [The Optimizer](internals/optimizer.html)
- [Contract Metadata](metadata.html)
- [Contract ABI Specification](abi-spec.html)

Advisory content

- [Security Considerations](security-considerations.html)
- [List of Known Bugs](bugs.html)
- [Solidity v0.5.0 Breaking Changes](050-breaking-changes.html)
- [Solidity v0.6.0 Breaking Changes](060-breaking-changes.html)
- [Solidity v0.7.0 Breaking Changes](070-breaking-changes.html)
- [Solidity v0.8.0 Breaking Changes](080-breaking-changes.html)

Additional Material

- [NatSpec Format](natspec-format.html)
- [SMTChecker and Formal Verification](smtchecker.html)
- [Yul](yul.html)
- [Import Path Resolution](path-resolution.html)

Resources

- [Style Guide](style-guide.html)
- [Common Patterns](common-patterns.html)
- [Resources](resources.html)
- [Contributing](contributing.html)
- [Language Influences](language-influences.html)
- [Solidity Brand Guide](brand-guide.html)

- [Keyword Index](genindex.html)

RTD v: v0.8.21

Languages

[en](https://docs.soliditylang.org/en/v0.8.21/contracts.html)

[zh](https://docs.soliditylang.org/zh/v0.8.19/contracts.html)

[fr](https://docs.soliditylang.org/fr/latest/contracts.html)

[tr](https://docs.soliditylang.org/tr/v0.8.16/contracts.html)

Versions

[latest](https://docs.soliditylang.org/en/latest/contracts.html)

[stable](https://docs.soliditylang.org/en/stable/contracts.html)

[v0.8.21](https://docs.soliditylang.org/en/v0.8.21/contracts.html)

[v0.8.20](https://docs.soliditylang.org/en/v0.8.20/contracts.html)

[v0.8.19](https://docs.soliditylang.org/en/v0.8.19/contracts.html)

[v0.8.18](https://docs.soliditylang.org/en/v0.8.18/contracts.html)

[v0.8.17](https://docs.soliditylang.org/en/v0.8.17/contracts.html)

[v0.8.16](https://docs.soliditylang.org/en/v0.8.16/contracts.html)

[v0.8.15](https://docs.soliditylang.org/en/v0.8.15/contracts.html)

[v0.8.14](https://docs.soliditylang.org/en/v0.8.14/contracts.html)

[v0.8.13](https://docs.soliditylang.org/en/v0.8.13/contracts.html)

[v0.8.12](https://docs.soliditylang.org/en/v0.8.12/contracts.html)

[v0.8.11](https://docs.soliditylang.org/en/v0.8.11/contracts.html)

[v0.8.10](https://docs.soliditylang.org/en/v0.8.10/contracts.html)

[v0.8.9](https://docs.soliditylang.org/en/v0.8.9/contracts.html)

[v0.8.8](https://docs.soliditylang.org/en/v0.8.8/contracts.html)

[v0.8.7](https://docs.soliditylang.org/en/v0.8.7/contracts.html)

[v0.8.6](https://docs.soliditylang.org/en/v0.8.6/contracts.html)

[v0.8.5](https://docs.soliditylang.org/en/v0.8.5/contracts.html)

[v0.8.4](https://docs.soliditylang.org/en/v0.8.4/contracts.html)

[v0.8.3](https://docs.soliditylang.org/en/v0.8.3/contracts.html)

[v0.8.2](https://docs.soliditylang.org/en/v0.8.2/contracts.html)

[v0.8.1](https://docs.soliditylang.org/en/v0.8.1/contracts.html)

[v0.8.0](https://docs.soliditylang.org/en/v0.8.0/contracts.html)

[v0.7.6](https://docs.soliditylang.org/en/v0.7.6/contracts.html)

[v0.7.5](https://docs.soliditylang.org/en/v0.7.5/contracts.html)

[v0.7.4](https://docs.soliditylang.org/en/v0.7.4/contracts.html)

[v0.7.3](https://docs.soliditylang.org/en/v0.7.3/contracts.html)

[v0.7.2](https://docs.soliditylang.org/en/v0.7.2/contracts.html)

[v0.7.1](https://docs.soliditylang.org/en/v0.7.1/contracts.html)

[v0.7.0](https://docs.soliditylang.org/en/v0.7.0/contracts.html)

[v0.6.12](https://docs.soliditylang.org/en/v0.6.12/contracts.html)

[v0.6.11](https://docs.soliditylang.org/en/v0.6.11/contracts.html)

[v0.6.10](https://docs.soliditylang.org/en/v0.6.10/contracts.html)

[v0.6.9](https://docs.soliditylang.org/en/v0.6.9/contracts.html)

[v0.6.8](https://docs.soliditylang.org/en/v0.6.8/contracts.html)

[v0.6.7](https://docs.soliditylang.org/en/v0.6.7/contracts.html)

[v0.6.6](https://docs.soliditylang.org/en/v0.6.6/contracts.html)

[v0.6.5](https://docs.soliditylang.org/en/v0.6.5/contracts.html)

[v0.6.4](https://docs.soliditylang.org/en/v0.6.4/contracts.html)

[v0.6.3](https://docs.soliditylang.org/en/v0.6.3/contracts.html)

[v0.6.2](https://docs.soliditylang.org/en/v0.6.2/contracts.html)

[v0.6.1](https://docs.soliditylang.org/en/v0.6.1/contracts.html)

[v0.6.0](https://docs.soliditylang.org/en/v0.6.0/contracts.html)

[v0.5.17](https://docs.soliditylang.org/en/v0.5.17/contracts.html)

[v0.5.16](https://docs.soliditylang.org/en/v0.5.16/contracts.html)

[v0.5.15](https://docs.soliditylang.org/en/v0.5.15/contracts.html)

[v0.5.14](https://docs.soliditylang.org/en/v0.5.14/contracts.html)

[v0.5.13](https://docs.soliditylang.org/en/v0.5.13/contracts.html)

[v0.5.12](https://docs.soliditylang.org/en/v0.5.12/contracts.html)

[v0.5.11](https://docs.soliditylang.org/en/v0.5.11/contracts.html)

[v0.5.10](https://docs.soliditylang.org/en/v0.5.10/contracts.html)

[v0.5.9](https://docs.soliditylang.org/en/v0.5.9/contracts.html)

[v0.5.8](https://docs.soliditylang.org/en/v0.5.8/contracts.html)

[v0.5.7](https://docs.soliditylang.org/en/v0.5.7/contracts.html)

[v0.5.6](https://docs.soliditylang.org/en/v0.5.6/contracts.html)

[v0.5.5](https://docs.soliditylang.org/en/v0.5.5/contracts.html)

[v0.5.4](https://docs.soliditylang.org/en/v0.5.4/contracts.html)

[v0.5.3](https://docs.soliditylang.org/en/v0.5.3/contracts.html)

[v0.5.2](https://docs.soliditylang.org/en/v0.5.2/contracts.html)

[v0.5.1](https://docs.soliditylang.org/en/v0.5.1/contracts.html)

[v0.5.0](https://docs.soliditylang.org/en/v0.5.0/contracts.html)

[v0.4.26](https://docs.soliditylang.org/en/v0.4.26/contracts.html)

[v0.4.25](https://docs.soliditylang.org/en/v0.4.25/contracts.html)

[v0.4.24](https://docs.soliditylang.org/en/v0.4.24/contracts.html)

[v0.4.23](https://docs.soliditylang.org/en/v0.4.23/contracts.html)

[v0.4.22](https://docs.soliditylang.org/en/v0.4.22/contracts.html)

[v0.4.21](https://docs.soliditylang.org/en/v0.4.21/contracts.html)

[v0.4.20](https://docs.soliditylang.org/en/v0.4.20/contracts.html)

[v0.4.19](https://docs.soliditylang.org/en/v0.4.19/contracts.html)

[v0.4.18](https://docs.soliditylang.org/en/v0.4.18/contracts.html)

[v0.4.17](https://docs.soliditylang.org/en/v0.4.17/contracts.html)

[v0.4.16](https://docs.soliditylang.org/en/v0.4.16/contracts.html)

[v0.4.15](https://docs.soliditylang.org/en/v0.4.15/contracts.html)

[v0.4.14](https://docs.soliditylang.org/en/v0.4.14/contracts.html)

[v0.4.13](https://docs.soliditylang.org/en/v0.4.13/contracts.html)

[v0.4.12](https://docs.soliditylang.org/en/v0.4.12/contracts.html)

[v0.4.11](https://docs.soliditylang.org/en/v0.4.11/contracts.html)

[v0.4.10](https://docs.soliditylang.org/en/v0.4.10/contracts.html)

[v0.4.9](https://docs.soliditylang.org/en/v0.4.9/contracts.html)

[v0.4.8](https://docs.soliditylang.org/en/v0.4.8/contracts.html)

[v0.4.7](https://docs.soliditylang.org/en/v0.4.7/contracts.html)

[v0.4.6](https://docs.soliditylang.org/en/v0.4.6/contracts.html)

[v0.4.5](https://docs.soliditylang.org/en/v0.4.5/contracts.html)

[v0.4.4](https://docs.soliditylang.org/en/v0.4.4/contracts.html)

[v0.4.3](https://docs.soliditylang.org/en/v0.4.3/contracts.html)

[v0.4.2](https://docs.soliditylang.org/en/v0.4.2/contracts.html)

[v0.4.1](https://docs.soliditylang.org/en/v0.4.1/contracts.html)

[v0.4.0](https://docs.soliditylang.org/en/v0.4.0/contracts.html)

[v0.3.6](https://docs.soliditylang.org/en/v0.3.6/contracts.html)

[v0.3.5](https://docs.soliditylang.org/en/v0.3.5/contracts.html)

[v0.3.4](https://docs.soliditylang.org/en/v0.3.4/contracts.html)

[v0.3.3](https://docs.soliditylang.org/en/v0.3.3/contracts.html)

[v0.3.2](https://docs.soliditylang.org/en/v0.3.2/contracts.html)

[v0.3.1](https://docs.soliditylang.org/en/v0.3.1/contracts.html)

[v0.3.0](https://docs.soliditylang.org/en/v0.3.0/contracts.html)

[v0.2.2](https://docs.soliditylang.org/en/v0.2.2/contracts.html)

[v0.2.1](https://docs.soliditylang.org/en/v0.2.1/contracts.html)

[v0.2.0](https://docs.soliditylang.org/en/v0.2.0/contracts.html)

[v0.1.7](https://docs.soliditylang.org/en/v0.1.7/contracts.html)

[v0.1.6](https://docs.soliditylang.org/en/v0.1.6/contracts.html)

[v0.1.5](https://docs.soliditylang.org/en/v0.1.5/contracts.html)

[v0.1.4](https://docs.soliditylang.org/en/v0.1.4/contracts.html)

[v0.1.3](https://docs.soliditylang.org/en/v0.1.3/contracts.html)

[v0.1.2](https://docs.soliditylang.org/en/v0.1.2/contracts.html)

[develop](https://docs.soliditylang.org/en/develop/contracts.html)

[breaking](https://docs.soliditylang.org/en/breaking/contracts.html)

Downloads

[PDF](//docs.soliditylang.org/_/downloads/en/v0.8.21/pdf/)

[Epub](//docs.soliditylang.org/_/downloads/en/v0.8.21/epub/)

On Read the Docs

[Project Home](//readthedocs.org/projects/solidity/)

[Builds](//readthedocs.org/projects/solidity/builds/)

[Downloads](//readthedocs.org/projects/solidity/downloads/)

On GitHub

[View](https://github.com/ethereum/solidity/blob/v0.8.21/docs/contracts.rst)

Search

---

Hosted by [Read the Docs](https://readthedocs.org) · [Privacy Policy](https://docs.readthedocs.io/page/privacy-policy.html)

- [](index.html)
- Contracts
- [Edit on GitHub](https://github.com/ethereum/solidity/blob/v0.8.21/docs/contracts.rst)

---

# Contracts[](#contracts "Permalink to this heading")

Contracts in Solidity are similar to classes in object-oriented languages. They contain persistent data in state variables, and functions that can modify these variables. Calling a function on a different contract (instance) will perform an EVM function call and thus switch the context such that state variables in the calling contract are inaccessible. A contract and its functions need to be called for anything to happen. There is no “cron” concept in Ethereum to call a function at a particular event automatically.

## Creating Contracts[](#creating-contracts "Permalink to this heading")

Contracts can be created “from outside” via Ethereum transactions or from within Solidity contracts.

IDEs, such as [Remix](https://remix.ethereum.org/), make the creation process seamless using UI elements.

One way to create contracts programmatically on Ethereum is via the JavaScript API [web3.js](https://github.com/web3/web3.js). It has a function called [web3.eth.Contract](https://web3js.readthedocs.io/en/1.0/web3-eth-contract.html#new-contract) to facilitate contract creation.

When a contract is created, its [constructor](#constructor) (a function declared with the `constructor` keyword) is executed once.

A constructor is optional. Only one constructor is allowed, which means overloading is not supported.

After the constructor has executed, the final code of the contract is stored on the blockchain. This code includes all public and external functions and all functions that are reachable from there through function calls. The deployed code does not include the constructor code or internal functions only called from the constructor.

Internally, constructor arguments are passed [ABI encoded](abi-spec.html#abi) after the code of the contract itself, but you do not have to care about this if you use `web3.js`.

If a contract wants to create another contract, the source code (and the binary) of the created contract has to be known to the creator. This means that cyclic creation dependencies are impossible.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjIyIDwwLjkuMDsKCgpjb250cmFjdCBPd25lZFRva2VuIHsKICAgIC8vIGBUb2tlbkNyZWF0b3JgIGlzIGEgY29udHJhY3QgdHlwZSB0aGF0IGlzIGRlZmluZWQgYmVsb3cuCiAgICAvLyBJdCBpcyBmaW5lIHRvIHJlZmVyZW5jZSBpdCBhcyBsb25nIGFzIGl0IGlzIG5vdCB1c2VkCiAgICAvLyB0byBjcmVhdGUgYSBuZXcgY29udHJhY3QuCiAgICBUb2tlbkNyZWF0b3IgY3JlYXRvcjsKICAgIGFkZHJlc3Mgb3duZXI7CiAgICBieXRlczMyIG5hbWU7CgogICAgLy8gVGhpcyBpcyB0aGUgY29uc3RydWN0b3Igd2hpY2ggcmVnaXN0ZXJzIHRoZQogICAgLy8gY3JlYXRvciBhbmQgdGhlIGFzc2lnbmVkIG5hbWUuCiAgICBjb25zdHJ1Y3RvcihieXRlczMyIG5hbWVfKSB7CiAgICAgICAgLy8gU3RhdGUgdmFyaWFibGVzIGFyZSBhY2Nlc3NlZCB2aWEgdGhlaXIgbmFtZQogICAgICAgIC8vIGFuZCBub3QgdmlhIGUuZy4gYHRoaXMub3duZXJgLiBGdW5jdGlvbnMgY2FuCiAgICAgICAgLy8gYmUgYWNjZXNzZWQgZGlyZWN0bHkgb3IgdGhyb3VnaCBgdGhpcy5mYCwKICAgICAgICAvLyBidXQgdGhlIGxhdHRlciBwcm92aWRlcyBhbiBleHRlcm5hbCB2aWV3CiAgICAgICAgLy8gdG8gdGhlIGZ1bmN0aW9uLiBFc3BlY2lhbGx5IGluIHRoZSBjb25zdHJ1Y3RvciwKICAgICAgICAvLyB5b3Ugc2hvdWxkIG5vdCBhY2Nlc3MgZnVuY3Rpb25zIGV4dGVybmFsbHksCiAgICAgICAgLy8gYmVjYXVzZSB0aGUgZnVuY3Rpb24gZG9lcyBub3QgZXhpc3QgeWV0LgogICAgICAgIC8vIFNlZSB0aGUgbmV4dCBzZWN0aW9uIGZvciBkZXRhaWxzLgogICAgICAgIG93bmVyID0gbXNnLnNlbmRlcjsKCiAgICAgICAgLy8gV2UgcGVyZm9ybSBhbiBleHBsaWNpdCB0eXBlIGNvbnZlcnNpb24gZnJvbSBgYWRkcmVzc2AKICAgICAgICAvLyB0byBgVG9rZW5DcmVhdG9yYCBhbmQgYXNzdW1lIHRoYXQgdGhlIHR5cGUgb2YKICAgICAgICAvLyB0aGUgY2FsbGluZyBjb250cmFjdCBpcyBgVG9rZW5DcmVhdG9yYCwgdGhlcmUgaXMKICAgICAgICAvLyBubyByZWFsIHdheSB0byB2ZXJpZnkgdGhhdC4KICAgICAgICAvLyBUaGlzIGRvZXMgbm90IGNyZWF0ZSBhIG5ldyBjb250cmFjdC4KICAgICAgICBjcmVhdG9yID0gVG9rZW5DcmVhdG9yKG1zZy5zZW5kZXIpOwogICAgICAgIG5hbWUgPSBuYW1lXzsKICAgIH0KCiAgICBmdW5jdGlvbiBjaGFuZ2VOYW1lKGJ5dGVzMzIgbmV3TmFtZSkgcHVibGljIHsKICAgICAgICAvLyBPbmx5IHRoZSBjcmVhdG9yIGNhbiBhbHRlciB0aGUgbmFtZS4KICAgICAgICAvLyBXZSBjb21wYXJlIHRoZSBjb250cmFjdCBiYXNlZCBvbiBpdHMKICAgICAgICAvLyBhZGRyZXNzIHdoaWNoIGNhbiBiZSByZXRyaWV2ZWQgYnkKICAgICAgICAvLyBleHBsaWNpdCBjb252ZXJzaW9uIHRvIGFkZHJlc3MuCiAgICAgICAgaWYgKG1zZy5zZW5kZXIgPT0gYWRkcmVzcyhjcmVhdG9yKSkKICAgICAgICAgICAgbmFtZSA9IG5ld05hbWU7CiAgICB9CgogICAgZnVuY3Rpb24gdHJhbnNmZXIoYWRkcmVzcyBuZXdPd25lcikgcHVibGljIHsKICAgICAgICAvLyBPbmx5IHRoZSBjdXJyZW50IG93bmVyIGNhbiB0cmFuc2ZlciB0aGUgdG9rZW4uCiAgICAgICAgaWYgKG1zZy5zZW5kZXIgIT0gb3duZXIpIHJldHVybjsKCiAgICAgICAgLy8gV2UgYXNrIHRoZSBjcmVhdG9yIGNvbnRyYWN0IGlmIHRoZSB0cmFuc2ZlcgogICAgICAgIC8vIHNob3VsZCBwcm9jZWVkIGJ5IHVzaW5nIGEgZnVuY3Rpb24gb2YgdGhlCiAgICAgICAgLy8gYFRva2VuQ3JlYXRvcmAgY29udHJhY3QgZGVmaW5lZCBiZWxvdy4gSWYKICAgICAgICAvLyB0aGUgY2FsbCBmYWlscyAoZS5nLiBkdWUgdG8gb3V0LW9mLWdhcyksCiAgICAgICAgLy8gdGhlIGV4ZWN1dGlvbiBhbHNvIGZhaWxzIGhlcmUuCiAgICAgICAgaWYgKGNyZWF0b3IuaXNUb2tlblRyYW5zZmVyT0sob3duZXIsIG5ld093bmVyKSkKICAgICAgICAgICAgb3duZXIgPSBuZXdPd25lcjsKICAgIH0KfQoKCmNvbnRyYWN0IFRva2VuQ3JlYXRvciB7CiAgICBmdW5jdGlvbiBjcmVhdGVUb2tlbihieXRlczMyIG5hbWUpCiAgICAgICAgcHVibGljCiAgICAgICAgcmV0dXJucyAoT3duZWRUb2tlbiB0b2tlbkFkZHJlc3MpCiAgICB7CiAgICAgICAgLy8gQ3JlYXRlIGEgbmV3IGBUb2tlbmAgY29udHJhY3QgYW5kIHJldHVybiBpdHMgYWRkcmVzcy4KICAgICAgICAvLyBGcm9tIHRoZSBKYXZhU2NyaXB0IHNpZGUsIHRoZSByZXR1cm4gdHlwZQogICAgICAgIC8vIG9mIHRoaXMgZnVuY3Rpb24gaXMgYGFkZHJlc3NgLCBhcyB0aGlzIGlzCiAgICAgICAgLy8gdGhlIGNsb3Nlc3QgdHlwZSBhdmFpbGFibGUgaW4gdGhlIEFCSS4KICAgICAgICByZXR1cm4gbmV3IE93bmVkVG9rZW4obmFtZSk7CiAgICB9CgogICAgZnVuY3Rpb24gY2hhbmdlTmFtZShPd25lZFRva2VuIHRva2VuQWRkcmVzcywgYnl0ZXMzMiBuYW1lKSBwdWJsaWMgewogICAgICAgIC8vIEFnYWluLCB0aGUgZXh0ZXJuYWwgdHlwZSBvZiBgdG9rZW5BZGRyZXNzYCBpcwogICAgICAgIC8vIHNpbXBseSBgYWRkcmVzc2AuCiAgICAgICAgdG9rZW5BZGRyZXNzLmNoYW5nZU5hbWUobmFtZSk7CiAgICB9CgogICAgLy8gUGVyZm9ybSBjaGVja3MgdG8gZGV0ZXJtaW5lIGlmIHRyYW5zZmVycmluZyBhIHRva2VuIHRvIHRoZQogICAgLy8gYE93bmVkVG9rZW5gIGNvbnRyYWN0IHNob3VsZCBwcm9jZWVkCiAgICBmdW5jdGlvbiBpc1Rva2VuVHJhbnNmZXJPSyhhZGRyZXNzIGN1cnJlbnRPd25lciwgYWRkcmVzcyBuZXdPd25lcikKICAgICAgICBwdWJsaWMKICAgICAgICBwdXJlCiAgICAgICAgcmV0dXJucyAoYm9vbCBvaykKICAgIHsKICAgICAgICAvLyBDaGVjayBhbiBhcmJpdHJhcnkgY29uZGl0aW9uIHRvIHNlZSBpZiB0cmFuc2ZlciBzaG91bGQgcHJvY2VlZAogICAgICAgIHJldHVybiBrZWNjYWsyNTYoYWJpLmVuY29kZVBhY2tlZChjdXJyZW50T3duZXIsIG5ld093bmVyKSlbMF0gPT0gMHg3ZjsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.22 <0.9.0;

contract OwnedToken {
    // `TokenCreator` is a contract type that is defined below.
    // It is fine to reference it as long as it is not used
    // to create a new contract.
    TokenCreator creator;
    address owner;
    bytes32 name;

    // This is the constructor which registers the
    // creator and the assigned name.
    constructor(bytes32 name_) {
        // State variables are accessed via their name
        // and not via e.g. `this.owner`. Functions can
        // be accessed directly or through `this.f`,
        // but the latter provides an external view
        // to the function. Especially in the constructor,
        // you should not access functions externally,
        // because the function does not exist yet.
        // See the next section for details.
        owner = msg.sender;

        // We perform an explicit type conversion from `address`
        // to `TokenCreator` and assume that the type of
        // the calling contract is `TokenCreator`, there is
        // no real way to verify that.
        // This does not create a new contract.
        creator = TokenCreator(msg.sender);
        name = name_;
    }

    function changeName(bytes32 newName) public {
        // Only the creator can alter the name.
        // We compare the contract based on its
        // address which can be retrieved by
        // explicit conversion to address.
        if (msg.sender == address(creator))
            name = newName;
    }

    function transfer(address newOwner) public {
        // Only the current owner can transfer the token.
        if (msg.sender != owner) return;

        // We ask the creator contract if the transfer
        // should proceed by using a function of the
        // `TokenCreator` contract defined below. If
        // the call fails (e.g. due to out-of-gas),
        // the execution also fails here.
        if (creator.isTokenTransferOK(owner, newOwner))
            owner = newOwner;
    }
}

contract TokenCreator {
    function createToken(bytes32 name)
        public
        returns (OwnedToken tokenAddress)
    {
        // Create a new `Token` contract and return its address.
        // From the JavaScript side, the return type
        // of this function is `address`, as this is
        // the closest type available in the ABI.
        return new OwnedToken(name);
    }

    function changeName(OwnedToken tokenAddress, bytes32 name) public {
        // Again, the external type of `tokenAddress` is
        // simply `address`.
        tokenAddress.changeName(name);
    }

    // Perform checks to determine if transferring a token to the
    // `OwnedToken` contract should proceed
    function isTokenTransferOK(address currentOwner, address newOwner)
        public
        pure
        returns (bool ok)
    {
        // Check an arbitrary condition to see if transfer should proceed
        return keccak256(abi.encodePacked(currentOwner, newOwner))[0] == 0x7f;
    }
}

## Visibility and Getters[](#visibility-and-getters "Permalink to this heading")

### State Variable Visibility[](#state-variable-visibility "Permalink to this heading")

`public`

Public state variables differ from internal ones only in that the compiler automatically generates [getter functions](#getter-functions) for them, which allows other contracts to read their values. When used within the same contract, the external access (e.g. `this.x`) invokes the getter while internal access (e.g. `x`) gets the variable value directly from storage. Setter functions are not generated so other contracts cannot directly modify their values.

`internal`

Internal state variables can only be accessed from within the contract they are defined in and in derived contracts. They cannot be accessed externally. This is the default visibility level for state variables.

`private`

Private state variables are like internal ones but they are not visible in derived contracts.

Warning

Making something `private` or `internal` only prevents other contracts from reading or modifying the information, but it will still be visible to the whole world outside of the blockchain.

### Function Visibility[](#function-visibility "Permalink to this heading")

Solidity knows two kinds of function calls: external ones that do create an actual EVM message call and internal ones that do not. Furthermore, internal functions can be made inaccessible to derived contracts. This gives rise to four types of visibility for functions.

`external`

External functions are part of the contract interface, which means they can be called from other contracts and via transactions. An external function `f` cannot be called internally (i.e. `f()` does not work, but `this.f()` works).

`public`

Public functions are part of the contract interface and can be either called internally or via message calls.

`internal`

Internal functions can only be accessed from within the current contract or contracts deriving from it. They cannot be accessed externally. Since they are not exposed to the outside through the contract’s ABI, they can take parameters of internal types like mappings or storage references.

`private`

Private functions are like internal ones but they are not visible in derived contracts.

Warning

Making something `private` or `internal` only prevents other contracts from reading or modifying the information, but it will still be visible to the whole world outside of the blockchain.

The visibility specifier is given after the type for state variables and between parameter list and return parameter list for functions.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IEMgewogICAgZnVuY3Rpb24gZih1aW50IGEpIHByaXZhdGUgcHVyZSByZXR1cm5zICh1aW50IGIpIHsgcmV0dXJuIGEgKyAxOyB9CiAgICBmdW5jdGlvbiBzZXREYXRhKHVpbnQgYSkgaW50ZXJuYWwgeyBkYXRhID0gYTsgfQogICAgdWludCBwdWJsaWMgZGF0YTsKfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract C {
    function f(uint a) private pure returns (uint b) { return a + 1; }
    function setData(uint a) internal { data = a; }
    uint public data;
}

In the following example, `D`, can call `c.getData()` to retrieve the value of `data` in state storage, but is not able to call `f`. Contract `E` is derived from `C` and, thus, can call `compute`.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IEMgewogICAgdWludCBwcml2YXRlIGRhdGE7CgogICAgZnVuY3Rpb24gZih1aW50IGEpIHByaXZhdGUgcHVyZSByZXR1cm5zKHVpbnQgYikgeyByZXR1cm4gYSArIDE7IH0KICAgIGZ1bmN0aW9uIHNldERhdGEodWludCBhKSBwdWJsaWMgeyBkYXRhID0gYTsgfQogICAgZnVuY3Rpb24gZ2V0RGF0YSgpIHB1YmxpYyB2aWV3IHJldHVybnModWludCkgeyByZXR1cm4gZGF0YTsgfQogICAgZnVuY3Rpb24gY29tcHV0ZSh1aW50IGEsIHVpbnQgYikgaW50ZXJuYWwgcHVyZSByZXR1cm5zICh1aW50KSB7IHJldHVybiBhICsgYjsgfQp9CgovLyBUaGlzIHdpbGwgbm90IGNvbXBpbGUKY29udHJhY3QgRCB7CiAgICBmdW5jdGlvbiByZWFkRGF0YSgpIHB1YmxpYyB7CiAgICAgICAgQyBjID0gbmV3IEMoKTsKICAgICAgICB1aW50IGxvY2FsID0gYy5mKDcpOyAvLyBlcnJvcjogbWVtYmVyIGBmYCBpcyBub3QgdmlzaWJsZQogICAgICAgIGMuc2V0RGF0YSgzKTsKICAgICAgICBsb2NhbCA9IGMuZ2V0RGF0YSgpOwogICAgICAgIGxvY2FsID0gYy5jb21wdXRlKDMsIDUpOyAvLyBlcnJvcjogbWVtYmVyIGBjb21wdXRlYCBpcyBub3QgdmlzaWJsZQogICAgfQp9Cgpjb250cmFjdCBFIGlzIEMgewogICAgZnVuY3Rpb24gZygpIHB1YmxpYyB7CiAgICAgICAgQyBjID0gbmV3IEMoKTsKICAgICAgICB1aW50IHZhbCA9IGNvbXB1dGUoMywgNSk7IC8vIGFjY2VzcyB0byBpbnRlcm5hbCBtZW1iZXIgKGZyb20gZGVyaXZlZCB0byBwYXJlbnQgY29udHJhY3QpCiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract C {
    uint private data;

    function f(uint a) private pure returns(uint b) { return a + 1; }
    function setData(uint a) public { data = a; }
    function getData() public view returns(uint) { return data; }
    function compute(uint a, uint b) internal pure returns (uint) { return a + b; }
}

// This will not compile
contract D {
    function readData() public {
        C c = new C();
        uint local = c.f(7); // error: member `f` is not visible
        c.setData(3);
        local = c.getData();
        local = c.compute(3, 5); // error: member `compute` is not visible
    }
}

contract E is C {
    function g() public {
        C c = new C();
        uint val = compute(3, 5); // access to internal member (from derived to parent contract)
    }
}

### Getter Functions[](#getter-functions "Permalink to this heading")

The compiler automatically creates getter functions for all **public** state variables. For the contract given below, the compiler will generate a function called `data` that does not take any arguments and returns a `uint`, the value of the state variable `data`. State variables can be initialized when they are declared.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IEMgewogICAgdWludCBwdWJsaWMgZGF0YSA9IDQyOwp9Cgpjb250cmFjdCBDYWxsZXIgewogICAgQyBjID0gbmV3IEMoKTsKICAgIGZ1bmN0aW9uIGYoKSBwdWJsaWMgdmlldyByZXR1cm5zICh1aW50KSB7CiAgICAgICAgcmV0dXJuIGMuZGF0YSgpOwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract C {
    uint public data = 42;
}

contract Caller {
    C c = new C();
    function f() public view returns (uint) {
        return c.data();
    }
}

The getter functions have external visibility. If the symbol is accessed internally (i.e. without `this.`), it evaluates to a state variable. If it is accessed externally (i.e. with `this.`), it evaluates to a function.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKY29udHJhY3QgQyB7CiAgICB1aW50IHB1YmxpYyBkYXRhOwogICAgZnVuY3Rpb24geCgpIHB1YmxpYyByZXR1cm5zICh1aW50KSB7CiAgICAgICAgZGF0YSA9IDM7IC8vIGludGVybmFsIGFjY2VzcwogICAgICAgIHJldHVybiB0aGlzLmRhdGEoKTsgLy8gZXh0ZXJuYWwgYWNjZXNzCiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract C {
    uint public data;
    function x() public returns (uint) {
        data = 3; // internal access
        return this.data(); // external access
    }
}

If you have a `public` state variable of array type, then you can only retrieve single elements of the array via the generated getter function. This mechanism exists to avoid high gas costs when returning an entire array. You can use arguments to specify which individual element to return, for example `myArray(0)`. If you want to return an entire array in one call, then you need to write a function, for example:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IGFycmF5RXhhbXBsZSB7CiAgICAvLyBwdWJsaWMgc3RhdGUgdmFyaWFibGUKICAgIHVpbnRbXSBwdWJsaWMgbXlBcnJheTsKCiAgICAvLyBHZXR0ZXIgZnVuY3Rpb24gZ2VuZXJhdGVkIGJ5IHRoZSBjb21waWxlcgogICAgLyoKICAgIGZ1bmN0aW9uIG15QXJyYXkodWludCBpKSBwdWJsaWMgdmlldyByZXR1cm5zICh1aW50KSB7CiAgICAgICAgcmV0dXJuIG15QXJyYXlbaV07CiAgICB9CiAgICAqLwoKICAgIC8vIGZ1bmN0aW9uIHRoYXQgcmV0dXJucyBlbnRpcmUgYXJyYXkKICAgIGZ1bmN0aW9uIGdldEFycmF5KCkgcHVibGljIHZpZXcgcmV0dXJucyAodWludFtdIG1lbW9yeSkgewogICAgICAgIHJldHVybiBteUFycmF5OwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract arrayExample {
    // public state variable
    uint[] public myArray;

    // Getter function generated by the compiler
    /*
    function myArray(uint i) public view returns (uint) {
        return myArray[i];
    }
    */

    // function that returns entire array
    function getArray() public view returns (uint[] memory) {
        return myArray;
    }
}

Now you can use `getArray()` to retrieve the entire array, instead of `myArray(i)`, which returns a single element per call.

The next example is more complex:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKY29udHJhY3QgQ29tcGxleCB7CiAgICBzdHJ1Y3QgRGF0YSB7CiAgICAgICAgdWludCBhOwogICAgICAgIGJ5dGVzMyBiOwogICAgICAgIG1hcHBpbmcodWludCA9PiB1aW50KSBtYXA7CiAgICAgICAgdWludFszXSBjOwogICAgICAgIHVpbnRbXSBkOwogICAgICAgIGJ5dGVzIGU7CiAgICB9CiAgICBtYXBwaW5nKHVpbnQgPT4gbWFwcGluZyhib29sID0+IERhdGFbXSkpIHB1YmxpYyBkYXRhOwp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract Complex {
    struct Data {
        uint a;
        bytes3 b;
        mapping(uint => uint) map;
        uint[3] c;
        uint[] d;
        bytes e;
    }
    mapping(uint => mapping(bool => Data[])) public data;
}

It generates a function of the following form. The mapping and arrays (with the exception of byte arrays) in the struct are omitted because there is no good way to select individual struct members or provide a key for the mapping:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=ZnVuY3Rpb24gZGF0YSh1aW50IGFyZzEsIGJvb2wgYXJnMiwgdWludCBhcmczKQogICAgcHVibGljCiAgICByZXR1cm5zICh1aW50IGEsIGJ5dGVzMyBiLCBieXRlcyBtZW1vcnkgZSkKewogICAgYSA9IGRhdGFbYXJnMV1bYXJnMl1bYXJnM10uYTsKICAgIGIgPSBkYXRhW2FyZzFdW2FyZzJdW2FyZzNdLmI7CiAgICBlID0gZGF0YVthcmcxXVthcmcyXVthcmczXS5lOwp9)

function data(uint arg1, bool arg2, uint arg3)
    public
    returns (uint a, bytes3 b, bytes memory e)
{
    a = data[arg1][arg2][arg3].a;
    b = data[arg1][arg2][arg3].b;
    e = data[arg1][arg2][arg3].e;
}

## Function Modifiers[](#function-modifiers "Permalink to this heading")

Modifiers can be used to change the behavior of functions in a declarative way. For example, you can use a modifier to automatically check a condition prior to executing the function.

Modifiers are inheritable properties of contracts and may be overridden by derived contracts, but only if they are marked `virtual`. For details, please see [Modifier Overriding](#modifier-overriding).

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjEgPDAuOS4wOwovLyBUaGlzIHdpbGwgcmVwb3J0IGEgd2FybmluZyBkdWUgdG8gZGVwcmVjYXRlZCBzZWxmZGVzdHJ1Y3QKCmNvbnRyYWN0IG93bmVkIHsKICAgIGNvbnN0cnVjdG9yKCkgeyBvd25lciA9IHBheWFibGUobXNnLnNlbmRlcik7IH0KICAgIGFkZHJlc3MgcGF5YWJsZSBvd25lcjsKCiAgICAvLyBUaGlzIGNvbnRyYWN0IG9ubHkgZGVmaW5lcyBhIG1vZGlmaWVyIGJ1dCBkb2VzIG5vdCB1c2UKICAgIC8vIGl0OiBpdCB3aWxsIGJlIHVzZWQgaW4gZGVyaXZlZCBjb250cmFjdHMuCiAgICAvLyBUaGUgZnVuY3Rpb24gYm9keSBpcyBpbnNlcnRlZCB3aGVyZSB0aGUgc3BlY2lhbCBzeW1ib2wKICAgIC8vIGBfO2AgaW4gdGhlIGRlZmluaXRpb24gb2YgYSBtb2RpZmllciBhcHBlYXJzLgogICAgLy8gVGhpcyBtZWFucyB0aGF0IGlmIHRoZSBvd25lciBjYWxscyB0aGlzIGZ1bmN0aW9uLCB0aGUKICAgIC8vIGZ1bmN0aW9uIGlzIGV4ZWN1dGVkIGFuZCBvdGhlcndpc2UsIGFuIGV4Y2VwdGlvbiBpcwogICAgLy8gdGhyb3duLgogICAgbW9kaWZpZXIgb25seU93bmVyIHsKICAgICAgICByZXF1aXJlKAogICAgICAgICAgICBtc2cuc2VuZGVyID09IG93bmVyLAogICAgICAgICAgICAiT25seSBvd25lciBjYW4gY2FsbCB0aGlzIGZ1bmN0aW9uLiIKICAgICAgICApOwogICAgICAgIF87CiAgICB9Cn0KCmNvbnRyYWN0IGRlc3RydWN0aWJsZSBpcyBvd25lZCB7CiAgICAvLyBUaGlzIGNvbnRyYWN0IGluaGVyaXRzIHRoZSBgb25seU93bmVyYCBtb2RpZmllciBmcm9tCiAgICAvLyBgb3duZWRgIGFuZCBhcHBsaWVzIGl0IHRvIHRoZSBgZGVzdHJveWAgZnVuY3Rpb24sIHdoaWNoCiAgICAvLyBjYXVzZXMgdGhhdCBjYWxscyB0byBgZGVzdHJveWAgb25seSBoYXZlIGFuIGVmZmVjdCBpZgogICAgLy8gdGhleSBhcmUgbWFkZSBieSB0aGUgc3RvcmVkIG93bmVyLgogICAgZnVuY3Rpb24gZGVzdHJveSgpIHB1YmxpYyBvbmx5T3duZXIgewogICAgICAgIHNlbGZkZXN0cnVjdChvd25lcik7CiAgICB9Cn0KCmNvbnRyYWN0IHByaWNlZCB7CiAgICAvLyBNb2RpZmllcnMgY2FuIHJlY2VpdmUgYXJndW1lbnRzOgogICAgbW9kaWZpZXIgY29zdHModWludCBwcmljZSkgewogICAgICAgIGlmIChtc2cudmFsdWUgPj0gcHJpY2UpIHsKICAgICAgICAgICAgXzsKICAgICAgICB9CiAgICB9Cn0KCmNvbnRyYWN0IFJlZ2lzdGVyIGlzIHByaWNlZCwgZGVzdHJ1Y3RpYmxlIHsKICAgIG1hcHBpbmcoYWRkcmVzcyA9PiBib29sKSByZWdpc3RlcmVkQWRkcmVzc2VzOwogICAgdWludCBwcmljZTsKCiAgICBjb25zdHJ1Y3Rvcih1aW50IGluaXRpYWxQcmljZSkgeyBwcmljZSA9IGluaXRpYWxQcmljZTsgfQoKICAgIC8vIEl0IGlzIGltcG9ydGFudCB0byBhbHNvIHByb3ZpZGUgdGhlCiAgICAvLyBgcGF5YWJsZWAga2V5d29yZCBoZXJlLCBvdGhlcndpc2UgdGhlIGZ1bmN0aW9uIHdpbGwKICAgIC8vIGF1dG9tYXRpY2FsbHkgcmVqZWN0IGFsbCBFdGhlciBzZW50IHRvIGl0LgogICAgZnVuY3Rpb24gcmVnaXN0ZXIoKSBwdWJsaWMgcGF5YWJsZSBjb3N0cyhwcmljZSkgewogICAgICAgIHJlZ2lzdGVyZWRBZGRyZXNzZXNbbXNnLnNlbmRlcl0gPSB0cnVlOwogICAgfQoKICAgIGZ1bmN0aW9uIGNoYW5nZVByaWNlKHVpbnQgcHJpY2VfKSBwdWJsaWMgb25seU93bmVyIHsKICAgICAgICBwcmljZSA9IHByaWNlXzsKICAgIH0KfQoKY29udHJhY3QgTXV0ZXggewogICAgYm9vbCBsb2NrZWQ7CiAgICBtb2RpZmllciBub1JlZW50cmFuY3koKSB7CiAgICAgICAgcmVxdWlyZSgKICAgICAgICAgICAgIWxvY2tlZCwKICAgICAgICAgICAgIlJlZW50cmFudCBjYWxsLiIKICAgICAgICApOwogICAgICAgIGxvY2tlZCA9IHRydWU7CiAgICAgICAgXzsKICAgICAgICBsb2NrZWQgPSBmYWxzZTsKICAgIH0KCiAgICAvLy8gVGhpcyBmdW5jdGlvbiBpcyBwcm90ZWN0ZWQgYnkgYSBtdXRleCwgd2hpY2ggbWVhbnMgdGhhdAogICAgLy8vIHJlZW50cmFudCBjYWxscyBmcm9tIHdpdGhpbiBgbXNnLnNlbmRlci5jYWxsYCBjYW5ub3QgY2FsbCBgZmAgYWdhaW4uCiAgICAvLy8gVGhlIGByZXR1cm4gN2Agc3RhdGVtZW50IGFzc2lnbnMgNyB0byB0aGUgcmV0dXJuIHZhbHVlIGJ1dCBzdGlsbAogICAgLy8vIGV4ZWN1dGVzIHRoZSBzdGF0ZW1lbnQgYGxvY2tlZCA9IGZhbHNlYCBpbiB0aGUgbW9kaWZpZXIuCiAgICBmdW5jdGlvbiBmKCkgcHVibGljIG5vUmVlbnRyYW5jeSByZXR1cm5zICh1aW50KSB7CiAgICAgICAgKGJvb2wgc3VjY2VzcywpID0gbXNnLnNlbmRlci5jYWxsKCIiKTsKICAgICAgICByZXF1aXJlKHN1Y2Nlc3MpOwogICAgICAgIHJldHVybiA3OwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.1 <0.9.0;
// This will report a warning due to deprecated selfdestruct

contract owned {
    constructor() { owner = payable(msg.sender); }
    address payable owner;

    // This contract only defines a modifier but does not use
    // it: it will be used in derived contracts.
    // The function body is inserted where the special symbol
    // `_;` in the definition of a modifier appears.
    // This means that if the owner calls this function, the
    // function is executed and otherwise, an exception is
    // thrown.
    modifier onlyOwner {
        require(
            msg.sender == owner,
            "Only owner can call this function."
        );
        _;
    }
}

contract destructible is owned {
    // This contract inherits the `onlyOwner` modifier from
    // `owned` and applies it to the `destroy` function, which
    // causes that calls to `destroy` only have an effect if
    // they are made by the stored owner.
    function destroy() public onlyOwner {
        selfdestruct(owner);
    }
}

contract priced {
    // Modifiers can receive arguments:
    modifier costs(uint price) {
        if (msg.value >= price) {
            _;
        }
    }
}

contract Register is priced, destructible {
    mapping(address => bool) registeredAddresses;
    uint price;

    constructor(uint initialPrice) { price = initialPrice; }

    // It is important to also provide the
    // `payable` keyword here, otherwise the function will
    // automatically reject all Ether sent to it.
    function register() public payable costs(price) {
        registeredAddresses[msg.sender] = true;
    }

    function changePrice(uint price_) public onlyOwner {
        price = price_;
    }
}

contract Mutex {
    bool locked;
    modifier noReentrancy() {
        require(
            !locked,
            "Reentrant call."
        );
        locked = true;
        _;
        locked = false;
    }

    /// This function is protected by a mutex, which means that
    /// reentrant calls from within `msg.sender.call` cannot call `f` again.
    /// The `return 7` statement assigns 7 to the return value but still
    /// executes the statement `locked = false` in the modifier.
    function f() public noReentrancy returns (uint) {
        (bool success,) = msg.sender.call("");
        require(success);
        return 7;
    }
}

If you want to access a modifier `m` defined in a contract `C`, you can use `C.m` to reference it without virtual lookup. It is only possible to use modifiers defined in the current contract or its base contracts. Modifiers can also be defined in libraries but their use is limited to functions of the same library.

Multiple modifiers are applied to a function by specifying them in a whitespace-separated list and are evaluated in the order presented.

Modifiers cannot implicitly access or change the arguments and return values of functions they modify. Their values can only be passed to them explicitly at the point of invocation.

In function modifiers, it is necessary to specify when you want the function to which the modifier is applied to be run. The placeholder statement (denoted by a single underscore character `_`) is used to denote where the body of the function being modified should be inserted. Note that the placeholder operator is different from using underscores as leading or trailing characters in variable names, which is a stylistic choice.

Explicit returns from a modifier or function body only leave the current modifier or function body. Return variables are assigned and control flow continues after the `_` in the preceding modifier.

Warning

In an earlier version of Solidity, `return` statements in functions having modifiers behaved differently.

An explicit return from a modifier with `return;` does not affect the values returned by the function. The modifier can, however, choose not to execute the function body at all and in that case the return variables are set to their [default values](control-structures.html#default-value) just as if the function had an empty body.

The `_` symbol can appear in the modifier multiple times. Each occurrence is replaced with the function body.

Arbitrary expressions are allowed for modifier arguments and in this context, all symbols visible from the function are visible in the modifier. Symbols introduced in the modifier are not visible in the function (as they might change by overriding).

## Constant and Immutable State Variables[](#constant-and-immutable-state-variables "Permalink to this heading")

State variables can be declared as `constant` or `immutable`. In both cases, the variables cannot be modified after the contract has been constructed. For `constant` variables, the value has to be fixed at compile-time, while for `immutable`, it can still be assigned at construction time.

It is also possible to define `constant` variables at the file level.

The compiler does not reserve a storage slot for these variables, and every occurrence is replaced by the respective value.

Compared to regular state variables, the gas costs of constant and immutable variables are much lower. For a constant variable, the expression assigned to it is copied to all the places where it is accessed and also re-evaluated each time. This allows for local optimizations. Immutable variables are evaluated once at construction time and their value is copied to all the places in the code where they are accessed. For these values, 32 bytes are reserved, even if they would fit in fewer bytes. Due to this, constant values can sometimes be cheaper than immutable values.

Not all types for constants and immutables are implemented at this time. The only supported types are [strings](types.html#strings) (only for constants) and [value types](types.html#value-types).

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguMjE7Cgp1aW50IGNvbnN0YW50IFggPSAzMioqMjIgKyA4OwoKY29udHJhY3QgQyB7CiAgICBzdHJpbmcgY29uc3RhbnQgVEVYVCA9ICJhYmMiOwogICAgYnl0ZXMzMiBjb25zdGFudCBNWV9IQVNIID0ga2VjY2FrMjU2KCJhYmMiKTsKICAgIHVpbnQgaW1tdXRhYmxlIGRlY2ltYWxzID0gMTg7CiAgICB1aW50IGltbXV0YWJsZSBtYXhCYWxhbmNlOwogICAgYWRkcmVzcyBpbW11dGFibGUgb3duZXIgPSBtc2cuc2VuZGVyOwoKICAgIGNvbnN0cnVjdG9yKHVpbnQgZGVjaW1hbHNfLCBhZGRyZXNzIHJlZikgewogICAgICAgIGlmIChkZWNpbWFsc18gIT0gMCkKICAgICAgICAgICAgLy8gSW1tdXRhYmxlcyBhcmUgb25seSBpbW11dGFibGUgd2hlbiBkZXBsb3llZC4KICAgICAgICAgICAgLy8gQXQgY29uc3RydWN0aW9uIHRpbWUgdGhleSBjYW4gYmUgYXNzaWduZWQgdG8gYW55IG51bWJlciBvZiB0aW1lcy4KICAgICAgICAgICAgZGVjaW1hbHMgPSBkZWNpbWFsc187CgogICAgICAgIC8vIEFzc2lnbm1lbnRzIHRvIGltbXV0YWJsZXMgY2FuIGV2ZW4gYWNjZXNzIHRoZSBlbnZpcm9ubWVudC4KICAgICAgICBtYXhCYWxhbmNlID0gcmVmLmJhbGFuY2U7CiAgICB9CgogICAgZnVuY3Rpb24gaXNCYWxhbmNlVG9vSGlnaChhZGRyZXNzIG90aGVyKSBwdWJsaWMgdmlldyByZXR1cm5zIChib29sKSB7CiAgICAgICAgcmV0dXJuIG90aGVyLmJhbGFuY2UgPiBtYXhCYWxhbmNlOwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.21;

uint constant X = 32**22 + 8;

contract C {
    string constant TEXT = "abc";
    bytes32 constant MY_HASH = keccak256("abc");
    uint immutable decimals = 18;
    uint immutable maxBalance;
    address immutable owner = msg.sender;

    constructor(uint decimals_, address ref) {
        if (decimals_ != 0)
            // Immutables are only immutable when deployed.
            // At construction time they can be assigned to any number of times.
            decimals = decimals_;

        // Assignments to immutables can even access the environment.
        maxBalance = ref.balance;
    }

    function isBalanceTooHigh(address other) public view returns (bool) {
        return other.balance > maxBalance;
    }
}

### Constant[](#constant "Permalink to this heading")

For `constant` variables, the value has to be a constant at compile time and it has to be assigned where the variable is declared. Any expression that accesses storage, blockchain data (e.g. `block.timestamp`, `address(this).balance` or `block.number`) or execution data (`msg.value` or `gasleft()`) or makes calls to external contracts is disallowed. Expressions that might have a side-effect on memory allocation are allowed, but those that might have a side-effect on other memory objects are not. The built-in functions `keccak256`, `sha256`, `ripemd160`, `ecrecover`, `addmod` and `mulmod` are allowed (even though, with the exception of `keccak256`, they do call external contracts).

The reason behind allowing side-effects on the memory allocator is that it should be possible to construct complex objects like e.g. lookup-tables. This feature is not yet fully usable.

### Immutable[](#immutable "Permalink to this heading")

Variables declared as `immutable` are a bit less restricted than those declared as `constant`: Immutable variables can be assigned a value at construction time. The value can be changed at any time before deployment and then it becomes permanent.

One additional restriction is that immutables can only be assigned to inside expressions for which there is no possibility of being executed after creation. This excludes all modifier definitions and functions other than constructors.

There are no restrictions on reading immutable variables. The read is even allowed to happen before the variable is written to for the first time because variables in Solidity always have a well-defined initial value. For this reason it is also allowed to never explicitly assign a value to an immutable.

Warning

When accessing immutables at construction time, please keep the [initialization order](ir-breaking-changes.html#state-variable-initialization-order) in mind. Even if you provide an explicit initializer, some expressions may end up being evaluated before that initializer, especially when they are at a different level in inheritance hierarchy.

Note

Before Solidity 0.8.21 initialization of immutable variables was more restrictive. Such variables had to be initialized exactly once at construction time and could not be read before then.

The contract creation code generated by the compiler will modify the contract’s runtime code before it is returned by replacing all references to immutables with the values assigned to them. This is important if you are comparing the runtime code generated by the compiler with the one actually stored in the blockchain. The compiler outputs where these immutables are located in the deployed bytecode in the `immutableReferences` field of the [compiler JSON standard output](using-the-compiler.html#compiler-api).

## Functions[](#functions "Permalink to this heading")

Functions can be defined inside and outside of contracts.

Functions outside of a contract, also called “free functions”, always have implicit `internal` [visibility](#visibility-and-getters). Their code is included in all contracts that call them, similar to internal library functions.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjEgPDAuOS4wOwoKZnVuY3Rpb24gc3VtKHVpbnRbXSBtZW1vcnkgYXJyKSBwdXJlIHJldHVybnMgKHVpbnQgcykgewogICAgZm9yICh1aW50IGkgPSAwOyBpIDwgYXJyLmxlbmd0aDsgaSsrKQogICAgICAgIHMgKz0gYXJyW2ldOwp9Cgpjb250cmFjdCBBcnJheUV4YW1wbGUgewogICAgYm9vbCBmb3VuZDsKICAgIGZ1bmN0aW9uIGYodWludFtdIG1lbW9yeSBhcnIpIHB1YmxpYyB7CiAgICAgICAgLy8gVGhpcyBjYWxscyB0aGUgZnJlZSBmdW5jdGlvbiBpbnRlcm5hbGx5LgogICAgICAgIC8vIFRoZSBjb21waWxlciB3aWxsIGFkZCBpdHMgY29kZSB0byB0aGUgY29udHJhY3QuCiAgICAgICAgdWludCBzID0gc3VtKGFycik7CiAgICAgICAgcmVxdWlyZShzID49IDEwKTsKICAgICAgICBmb3VuZCA9IHRydWU7CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.1 <0.9.0;

function sum(uint[] memory arr) pure returns (uint s) {
    for (uint i = 0; i < arr.length; i++)
        s += arr[i];
}

contract ArrayExample {
    bool found;
    function f(uint[] memory arr) public {
        // This calls the free function internally.
        // The compiler will add its code to the contract.
        uint s = sum(arr);
        require(s >= 10);
        found = true;
    }
}

Note

Functions defined outside a contract are still always executed in the context of a contract. They still can call other contracts, send them Ether and destroy the contract that called them, among other things. The main difference to functions defined inside a contract is that free functions do not have direct access to the variable `this`, storage variables and functions not in their scope.

### Function Parameters and Return Variables[](#function-parameters-and-return-variables "Permalink to this heading")

Functions take typed parameters as input and may, unlike in many other languages, also return an arbitrary number of values as output.

#### Function Parameters[](#function-parameters "Permalink to this heading")

Function parameters are declared the same way as variables, and the name of unused parameters can be omitted.

For example, if you want your contract to accept one kind of external call with two integers, you would use something like the following:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IFNpbXBsZSB7CiAgICB1aW50IHN1bTsKICAgIGZ1bmN0aW9uIHRha2VyKHVpbnQgYSwgdWludCBiKSBwdWJsaWMgewogICAgICAgIHN1bSA9IGEgKyBiOwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract Simple {
    uint sum;
    function taker(uint a, uint b) public {
        sum = a + b;
    }
}

Function parameters can be used as any other local variable and they can also be assigned to.

#### Return Variables[](#return-variables "Permalink to this heading")

Function return variables are declared with the same syntax after the `returns` keyword.

For example, suppose you want to return two results: the sum and the product of two integers passed as function parameters, then you use something like:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IFNpbXBsZSB7CiAgICBmdW5jdGlvbiBhcml0aG1ldGljKHVpbnQgYSwgdWludCBiKQogICAgICAgIHB1YmxpYwogICAgICAgIHB1cmUKICAgICAgICByZXR1cm5zICh1aW50IHN1bSwgdWludCBwcm9kdWN0KQogICAgewogICAgICAgIHN1bSA9IGEgKyBiOwogICAgICAgIHByb2R1Y3QgPSBhICogYjsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract Simple {
    function arithmetic(uint a, uint b)
        public
        pure
        returns (uint sum, uint product)
    {
        sum = a + b;
        product = a * b;
    }
}

The names of return variables can be omitted. Return variables can be used as any other local variable and they are initialized with their [default value](control-structures.html#default-value) and have that value until they are (re-)assigned.

You can either explicitly assign to return variables and then leave the function as above, or you can provide return values (either a single or [multiple ones](#multi-return)) directly with the `return` statement:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IFNpbXBsZSB7CiAgICBmdW5jdGlvbiBhcml0aG1ldGljKHVpbnQgYSwgdWludCBiKQogICAgICAgIHB1YmxpYwogICAgICAgIHB1cmUKICAgICAgICByZXR1cm5zICh1aW50IHN1bSwgdWludCBwcm9kdWN0KQogICAgewogICAgICAgIHJldHVybiAoYSArIGIsIGEgKiBiKTsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract Simple {
    function arithmetic(uint a, uint b)
        public
        pure
        returns (uint sum, uint product)
    {
        return (a + b, a * b);
    }
}

If you use an early `return` to leave a function that has return variables, you must provide return values together with the return statement.

Note

You cannot return some types from non-internal functions. This includes the types listed below and any composite types that recursively contain them:

- mappings,
    
- internal function types,
    
- reference types with location set to `storage`,
    
- multi-dimensional arrays (applies only to [ABI coder v1](layout-of-source-files.html#abi-coder)),
    
- structs (applies only to [ABI coder v1](layout-of-source-files.html#abi-coder)).
    

This restriction does not apply to library functions because of their different [internal ABI](#library-selectors).

#### Returning Multiple Values[](#returning-multiple-values "Permalink to this heading")

When a function has multiple return types, the statement `return (v0, v1, ..., vn)` can be used to return multiple values. The number of components must be the same as the number of return variables and their types have to match, potentially after an [implicit conversion](types.html#types-conversion-elementary-types).

### State Mutability[](#state-mutability "Permalink to this heading")

#### View Functions[](#view-functions "Permalink to this heading")

Functions can be declared `view` in which case they promise not to modify the state.

Note

If the compiler’s EVM target is Byzantium or newer (default) the opcode `STATICCALL` is used when `view` functions are called, which enforces the state to stay unmodified as part of the EVM execution. For library `view` functions `DELEGATECALL` is used, because there is no combined `DELEGATECALL` and `STATICCALL`. This means library `view` functions do not have run-time checks that prevent state modifications. This should not impact security negatively because library code is usually known at compile-time and the static checker performs compile-time checks.

The following statements are considered modifying the state:

1. Writing to state variables.
    
2. [Emitting events](#events).
    
3. [Creating other contracts](control-structures.html#creating-contracts).
    
4. Using `selfdestruct`.
    
5. Sending Ether via calls.
    
6. Calling any function not marked `view` or `pure`.
    
7. Using low-level calls.
    
8. Using inline assembly that contains certain opcodes.
    

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC41LjAgPDAuOS4wOwoKY29udHJhY3QgQyB7CiAgICBmdW5jdGlvbiBmKHVpbnQgYSwgdWludCBiKSBwdWJsaWMgdmlldyByZXR1cm5zICh1aW50KSB7CiAgICAgICAgcmV0dXJuIGEgKiAoYiArIDQyKSArIGJsb2NrLnRpbWVzdGFtcDsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.5.0 <0.9.0;

contract C {
    function f(uint a, uint b) public view returns (uint) {
        return a * (b + 42) + block.timestamp;
    }
}

Note

`constant` on functions used to be an alias to `view`, but this was dropped in version 0.5.0.

Note

Getter methods are automatically marked `view`.

Note

Prior to version 0.5.0, the compiler did not use the `STATICCALL` opcode for `view` functions. This enabled state modifications in `view` functions through the use of invalid explicit type conversions. By using `STATICCALL` for `view` functions, modifications to the state are prevented on the level of the EVM.

#### Pure Functions[](#pure-functions "Permalink to this heading")

Functions can be declared `pure` in which case they promise not to read from or modify the state. In particular, it should be possible to evaluate a `pure` function at compile-time given only its inputs and `msg.data`, but without any knowledge of the current blockchain state. This means that reading from `immutable` variables can be a non-pure operation.

Note

If the compiler’s EVM target is Byzantium or newer (default) the opcode `STATICCALL` is used, which does not guarantee that the state is not read, but at least that it is not modified.

In addition to the list of state modifying statements explained above, the following are considered reading from the state:

1. Reading from state variables.
    
2. Accessing `address(this).balance` or `<address>.balance`.
    
3. Accessing any of the members of `block`, `tx`, `msg` (with the exception of `msg.sig` and `msg.data`).
    
4. Calling any function not marked `pure`.
    
5. Using inline assembly that contains certain opcodes.
    

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC41LjAgPDAuOS4wOwoKY29udHJhY3QgQyB7CiAgICBmdW5jdGlvbiBmKHVpbnQgYSwgdWludCBiKSBwdWJsaWMgcHVyZSByZXR1cm5zICh1aW50KSB7CiAgICAgICAgcmV0dXJuIGEgKiAoYiArIDQyKTsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.5.0 <0.9.0;

contract C {
    function f(uint a, uint b) public pure returns (uint) {
        return a * (b + 42);
    }
}

Pure functions are able to use the `revert()` and `require()` functions to revert potential state changes when an [error occurs](control-structures.html#assert-and-require).

Reverting a state change is not considered a “state modification”, as only changes to the state made previously in code that did not have the `view` or `pure` restriction are reverted and that code has the option to catch the `revert` and not pass it on.

This behavior is also in line with the `STATICCALL` opcode.

Warning

It is not possible to prevent functions from reading the state at the level of the EVM, it is only possible to prevent them from writing to the state (i.e. only `view` can be enforced at the EVM level, `pure` can not).

Note

Prior to version 0.5.0, the compiler did not use the `STATICCALL` opcode for `pure` functions. This enabled state modifications in `pure` functions through the use of invalid explicit type conversions. By using `STATICCALL` for `pure` functions, modifications to the state are prevented on the level of the EVM.

Note

Prior to version 0.4.17 the compiler did not enforce that `pure` is not reading the state. It is a compile-time type check, which can be circumvented doing invalid explicit conversions between contract types, because the compiler can verify that the type of the contract does not do state-changing operations, but it cannot check that the contract that will be called at runtime is actually of that type.

### Special Functions[](#special-functions "Permalink to this heading")

#### Receive Ether Function[](#receive-ether-function "Permalink to this heading")

A contract can have at most one `receive` function, declared using `receive() external payable { ... }` (without the `function` keyword). This function cannot have arguments, cannot return anything and must have `external` visibility and `payable` state mutability. It can be virtual, can override and can have modifiers.

The receive function is executed on a call to the contract with empty calldata. This is the function that is executed on plain Ether transfers (e.g. via `.send()` or `.transfer()`). If no such function exists, but a payable [fallback function](#fallback-function) exists, the fallback function will be called on a plain Ether transfer. If neither a receive Ether nor a payable fallback function is present, the contract cannot receive Ether through a transaction that does not represent a payable function call and throws an exception.

In the worst case, the `receive` function can only rely on 2300 gas being available (for example when `send` or `transfer` is used), leaving little room to perform other operations except basic logging. The following operations will consume more gas than the 2300 gas stipend:

- Writing to storage
    
- Creating a contract
    
- Calling an external function which consumes a large amount of gas
    
- Sending Ether
    

Warning

When Ether is sent directly to a contract (without a function call, i.e. sender uses `send` or `transfer`) but the receiving contract does not define a receive Ether function or a payable fallback function, an exception will be thrown, sending back the Ether (this was different before Solidity v0.4.0). If you want your contract to receive Ether, you have to implement a receive Ether function (using payable fallback functions for receiving Ether is not recommended, since the fallback is invoked and would not fail for interface confusions on the part of the sender).

Warning

A contract without a receive Ether function can receive Ether as a recipient of a _coinbase transaction_ (aka _miner block reward_) or as a destination of a `selfdestruct`.

A contract cannot react to such Ether transfers and thus also cannot reject them. This is a design choice of the EVM and Solidity cannot work around it.

It also means that `address(this).balance` can be higher than the sum of some manual accounting implemented in a contract (i.e. having a counter updated in the receive Ether function).

Below you can see an example of a Sink contract that uses function `receive`.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKLy8gVGhpcyBjb250cmFjdCBrZWVwcyBhbGwgRXRoZXIgc2VudCB0byBpdCB3aXRoIG5vIHdheQovLyB0byBnZXQgaXQgYmFjay4KY29udHJhY3QgU2luayB7CiAgICBldmVudCBSZWNlaXZlZChhZGRyZXNzLCB1aW50KTsKICAgIHJlY2VpdmUoKSBleHRlcm5hbCBwYXlhYmxlIHsKICAgICAgICBlbWl0IFJlY2VpdmVkKG1zZy5zZW5kZXIsIG1zZy52YWx1ZSk7CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

// This contract keeps all Ether sent to it with no way
// to get it back.
contract Sink {
    event Received(address, uint);
    receive() external payable {
        emit Received(msg.sender, msg.value);
    }
}

#### Fallback Function[](#fallback-function "Permalink to this heading")

A contract can have at most one `fallback` function, declared using either `fallback () external [payable]` or `fallback (bytes calldata input) external [payable] returns (bytes memory output)` (both without the `function` keyword). This function must have `external` visibility. A fallback function can be virtual, can override and can have modifiers.

The fallback function is executed on a call to the contract if none of the other functions match the given function signature, or if no data was supplied at all and there is no [receive Ether function](#receive-ether-function). The fallback function always receives data, but in order to also receive Ether it must be marked `payable`.

If the version with parameters is used, `input` will contain the full data sent to the contract (equal to `msg.data`) and can return data in `output`. The returned data will not be ABI-encoded. Instead it will be returned without modifications (not even padding).

In the worst case, if a payable fallback function is also used in place of a receive function, it can only rely on 2300 gas being available (see [receive Ether function](#receive-ether-function) for a brief description of the implications of this).

Like any function, the fallback function can execute complex operations as long as there is enough gas passed on to it.

Warning

A `payable` fallback function is also executed for plain Ether transfers, if no [receive Ether function](#receive-ether-function) is present. It is recommended to always define a receive Ether function as well, if you define a payable fallback function to distinguish Ether transfers from interface confusions.

Note

If you want to decode the input data, you can check the first four bytes for the function selector and then you can use `abi.decode` together with the array slice syntax to decode ABI-encoded data: `(c, d) = abi.decode(input[4:], (uint256, uint256));` Note that this should only be used as a last resort and proper functions should be used instead.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjIgPDAuOS4wOwoKY29udHJhY3QgVGVzdCB7CiAgICB1aW50IHg7CiAgICAvLyBUaGlzIGZ1bmN0aW9uIGlzIGNhbGxlZCBmb3IgYWxsIG1lc3NhZ2VzIHNlbnQgdG8KICAgIC8vIHRoaXMgY29udHJhY3QgKHRoZXJlIGlzIG5vIG90aGVyIGZ1bmN0aW9uKS4KICAgIC8vIFNlbmRpbmcgRXRoZXIgdG8gdGhpcyBjb250cmFjdCB3aWxsIGNhdXNlIGFuIGV4Y2VwdGlvbiwKICAgIC8vIGJlY2F1c2UgdGhlIGZhbGxiYWNrIGZ1bmN0aW9uIGRvZXMgbm90IGhhdmUgdGhlIGBwYXlhYmxlYAogICAgLy8gbW9kaWZpZXIuCiAgICBmYWxsYmFjaygpIGV4dGVybmFsIHsgeCA9IDE7IH0KfQoKY29udHJhY3QgVGVzdFBheWFibGUgewogICAgdWludCB4OwogICAgdWludCB5OwogICAgLy8gVGhpcyBmdW5jdGlvbiBpcyBjYWxsZWQgZm9yIGFsbCBtZXNzYWdlcyBzZW50IHRvCiAgICAvLyB0aGlzIGNvbnRyYWN0LCBleGNlcHQgcGxhaW4gRXRoZXIgdHJhbnNmZXJzCiAgICAvLyAodGhlcmUgaXMgbm8gb3RoZXIgZnVuY3Rpb24gZXhjZXB0IHRoZSByZWNlaXZlIGZ1bmN0aW9uKS4KICAgIC8vIEFueSBjYWxsIHdpdGggbm9uLWVtcHR5IGNhbGxkYXRhIHRvIHRoaXMgY29udHJhY3Qgd2lsbCBleGVjdXRlCiAgICAvLyB0aGUgZmFsbGJhY2sgZnVuY3Rpb24gKGV2ZW4gaWYgRXRoZXIgaXMgc2VudCBhbG9uZyB3aXRoIHRoZSBjYWxsKS4KICAgIGZhbGxiYWNrKCkgZXh0ZXJuYWwgcGF5YWJsZSB7IHggPSAxOyB5ID0gbXNnLnZhbHVlOyB9CgogICAgLy8gVGhpcyBmdW5jdGlvbiBpcyBjYWxsZWQgZm9yIHBsYWluIEV0aGVyIHRyYW5zZmVycywgaS5lLgogICAgLy8gZm9yIGV2ZXJ5IGNhbGwgd2l0aCBlbXB0eSBjYWxsZGF0YS4KICAgIHJlY2VpdmUoKSBleHRlcm5hbCBwYXlhYmxlIHsgeCA9IDI7IHkgPSBtc2cudmFsdWU7IH0KfQoKY29udHJhY3QgQ2FsbGVyIHsKICAgIGZ1bmN0aW9uIGNhbGxUZXN0KFRlc3QgdGVzdCkgcHVibGljIHJldHVybnMgKGJvb2wpIHsKICAgICAgICAoYm9vbCBzdWNjZXNzLCkgPSBhZGRyZXNzKHRlc3QpLmNhbGwoYWJpLmVuY29kZVdpdGhTaWduYXR1cmUoIm5vbkV4aXN0aW5nRnVuY3Rpb24oKSIpKTsKICAgICAgICByZXF1aXJlKHN1Y2Nlc3MpOwogICAgICAgIC8vIHJlc3VsdHMgaW4gdGVzdC54IGJlY29taW5nID09IDEuCgogICAgICAgIC8vIGFkZHJlc3ModGVzdCkgd2lsbCBub3QgYWxsb3cgdG8gY2FsbCBgYHNlbmRgYCBkaXJlY3RseSwgc2luY2UgYGB0ZXN0YGAgaGFzIG5vIHBheWFibGUKICAgICAgICAvLyBmYWxsYmFjayBmdW5jdGlvbi4KICAgICAgICAvLyBJdCBoYXMgdG8gYmUgY29udmVydGVkIHRvIHRoZSBgYGFkZHJlc3MgcGF5YWJsZWBgIHR5cGUgdG8gZXZlbiBhbGxvdyBjYWxsaW5nIGBgc2VuZGBgIG9uIGl0LgogICAgICAgIGFkZHJlc3MgcGF5YWJsZSB0ZXN0UGF5YWJsZSA9IHBheWFibGUoYWRkcmVzcyh0ZXN0KSk7CgogICAgICAgIC8vIElmIHNvbWVvbmUgc2VuZHMgRXRoZXIgdG8gdGhhdCBjb250cmFjdCwKICAgICAgICAvLyB0aGUgdHJhbnNmZXIgd2lsbCBmYWlsLCBpLmUuIHRoaXMgcmV0dXJucyBmYWxzZSBoZXJlLgogICAgICAgIHJldHVybiB0ZXN0UGF5YWJsZS5zZW5kKDIgZXRoZXIpOwogICAgfQoKICAgIGZ1bmN0aW9uIGNhbGxUZXN0UGF5YWJsZShUZXN0UGF5YWJsZSB0ZXN0KSBwdWJsaWMgcmV0dXJucyAoYm9vbCkgewogICAgICAgIChib29sIHN1Y2Nlc3MsKSA9IGFkZHJlc3ModGVzdCkuY2FsbChhYmkuZW5jb2RlV2l0aFNpZ25hdHVyZSgibm9uRXhpc3RpbmdGdW5jdGlvbigpIikpOwogICAgICAgIHJlcXVpcmUoc3VjY2Vzcyk7CiAgICAgICAgLy8gcmVzdWx0cyBpbiB0ZXN0LnggYmVjb21pbmcgPT0gMSBhbmQgdGVzdC55IGJlY29taW5nIDAuCiAgICAgICAgKHN1Y2Nlc3MsKSA9IGFkZHJlc3ModGVzdCkuY2FsbHt2YWx1ZTogMX0oYWJpLmVuY29kZVdpdGhTaWduYXR1cmUoIm5vbkV4aXN0aW5nRnVuY3Rpb24oKSIpKTsKICAgICAgICByZXF1aXJlKHN1Y2Nlc3MpOwogICAgICAgIC8vIHJlc3VsdHMgaW4gdGVzdC54IGJlY29taW5nID09IDEgYW5kIHRlc3QueSBiZWNvbWluZyAxLgoKICAgICAgICAvLyBJZiBzb21lb25lIHNlbmRzIEV0aGVyIHRvIHRoYXQgY29udHJhY3QsIHRoZSByZWNlaXZlIGZ1bmN0aW9uIGluIFRlc3RQYXlhYmxlIHdpbGwgYmUgY2FsbGVkLgogICAgICAgIC8vIFNpbmNlIHRoYXQgZnVuY3Rpb24gd3JpdGVzIHRvIHN0b3JhZ2UsIGl0IHRha2VzIG1vcmUgZ2FzIHRoYW4gaXMgYXZhaWxhYmxlIHdpdGggYQogICAgICAgIC8vIHNpbXBsZSBgYHNlbmRgYCBvciBgYHRyYW5zZmVyYGAuIEJlY2F1c2Ugb2YgdGhhdCwgd2UgaGF2ZSB0byB1c2UgYSBsb3ctbGV2ZWwgY2FsbC4KICAgICAgICAoc3VjY2VzcywpID0gYWRkcmVzcyh0ZXN0KS5jYWxse3ZhbHVlOiAyIGV0aGVyfSgiIik7CiAgICAgICAgcmVxdWlyZShzdWNjZXNzKTsKICAgICAgICAvLyByZXN1bHRzIGluIHRlc3QueCBiZWNvbWluZyA9PSAyIGFuZCB0ZXN0LnkgYmVjb21pbmcgMiBldGhlci4KCiAgICAgICAgcmV0dXJuIHRydWU7CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.2 <0.9.0;

contract Test {
    uint x;
    // This function is called for all messages sent to
    // this contract (there is no other function).
    // Sending Ether to this contract will cause an exception,
    // because the fallback function does not have the `payable`
    // modifier.
    fallback() external { x = 1; }
}

contract TestPayable {
    uint x;
    uint y;
    // This function is called for all messages sent to
    // this contract, except plain Ether transfers
    // (there is no other function except the receive function).
    // Any call with non-empty calldata to this contract will execute
    // the fallback function (even if Ether is sent along with the call).
    fallback() external payable { x = 1; y = msg.value; }

    // This function is called for plain Ether transfers, i.e.
    // for every call with empty calldata.
    receive() external payable { x = 2; y = msg.value; }
}

contract Caller {
    function callTest(Test test) public returns (bool) {
        (bool success,) = address(test).call(abi.encodeWithSignature("nonExistingFunction()"));
        require(success);
        // results in test.x becoming == 1.

        // address(test) will not allow to call ``send`` directly, since ``test`` has no payable
        // fallback function.
        // It has to be converted to the ``address payable`` type to even allow calling ``send`` on it.
        address payable testPayable = payable(address(test));

        // If someone sends Ether to that contract,
        // the transfer will fail, i.e. this returns false here.
        return testPayable.send(2 ether);
    }

    function callTestPayable(TestPayable test) public returns (bool) {
        (bool success,) = address(test).call(abi.encodeWithSignature("nonExistingFunction()"));
        require(success);
        // results in test.x becoming == 1 and test.y becoming 0.
        (success,) = address(test).call{value: 1}(abi.encodeWithSignature("nonExistingFunction()"));
        require(success);
        // results in test.x becoming == 1 and test.y becoming 1.

        // If someone sends Ether to that contract, the receive function in TestPayable will be called.
        // Since that function writes to storage, it takes more gas than is available with a
        // simple ``send`` or ``transfer``. Because of that, we have to use a low-level call.
        (success,) = address(test).call{value: 2 ether}("");
        require(success);
        // results in test.x becoming == 2 and test.y becoming 2 ether.

        return true;
    }
}

### Function Overloading[](#function-overloading "Permalink to this heading")

A contract can have multiple functions of the same name but with different parameter types. This process is called “overloading” and also applies to inherited functions. The following example shows overloading of the function `f` in the scope of contract `A`.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IEEgewogICAgZnVuY3Rpb24gZih1aW50IHZhbHVlKSBwdWJsaWMgcHVyZSByZXR1cm5zICh1aW50IG91dCkgewogICAgICAgIG91dCA9IHZhbHVlOwogICAgfQoKICAgIGZ1bmN0aW9uIGYodWludCB2YWx1ZSwgYm9vbCByZWFsbHkpIHB1YmxpYyBwdXJlIHJldHVybnMgKHVpbnQgb3V0KSB7CiAgICAgICAgaWYgKHJlYWxseSkKICAgICAgICAgICAgb3V0ID0gdmFsdWU7CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract A {
    function f(uint value) public pure returns (uint out) {
        out = value;
    }

    function f(uint value, bool really) public pure returns (uint out) {
        if (really)
            out = value;
    }
}

Overloaded functions are also present in the external interface. It is an error if two externally visible functions differ by their Solidity types but not by their external types.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCi8vIFRoaXMgd2lsbCBub3QgY29tcGlsZQpjb250cmFjdCBBIHsKICAgIGZ1bmN0aW9uIGYoQiB2YWx1ZSkgcHVibGljIHB1cmUgcmV0dXJucyAoQiBvdXQpIHsKICAgICAgICBvdXQgPSB2YWx1ZTsKICAgIH0KCiAgICBmdW5jdGlvbiBmKGFkZHJlc3MgdmFsdWUpIHB1YmxpYyBwdXJlIHJldHVybnMgKGFkZHJlc3Mgb3V0KSB7CiAgICAgICAgb3V0ID0gdmFsdWU7CiAgICB9Cn0KCmNvbnRyYWN0IEIgewp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

// This will not compile
contract A {
    function f(B value) public pure returns (B out) {
        out = value;
    }

    function f(address value) public pure returns (address out) {
        out = value;
    }
}

contract B {
}

Both `f` function overloads above end up accepting the address type for the ABI although they are considered different inside Solidity.

#### Overload resolution and Argument matching[](#overload-resolution-and-argument-matching "Permalink to this heading")

Overloaded functions are selected by matching the function declarations in the current scope to the arguments supplied in the function call. Functions are selected as overload candidates if all arguments can be implicitly converted to the expected types. If there is not exactly one candidate, resolution fails.

Note

Return parameters are not taken into account for overload resolution.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IEEgewogICAgZnVuY3Rpb24gZih1aW50OCB2YWwpIHB1YmxpYyBwdXJlIHJldHVybnMgKHVpbnQ4IG91dCkgewogICAgICAgIG91dCA9IHZhbDsKICAgIH0KCiAgICBmdW5jdGlvbiBmKHVpbnQyNTYgdmFsKSBwdWJsaWMgcHVyZSByZXR1cm5zICh1aW50MjU2IG91dCkgewogICAgICAgIG91dCA9IHZhbDsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract A {
    function f(uint8 val) public pure returns (uint8 out) {
        out = val;
    }

    function f(uint256 val) public pure returns (uint256 out) {
        out = val;
    }
}

Calling `f(50)` would create a type error since `50` can be implicitly converted both to `uint8` and `uint256` types. On another hand `f(256)` would resolve to `f(uint256)` overload as `256` cannot be implicitly converted to `uint8`.

## Events[](#events "Permalink to this heading")

Solidity events give an abstraction on top of the EVM’s logging functionality. Applications can subscribe and listen to these events through the RPC interface of an Ethereum client.

Events are inheritable members of contracts. When you call them, they cause the arguments to be stored in the transaction’s log - a special data structure in the blockchain. These logs are associated with the address of the contract, are incorporated into the blockchain, and stay there as long as a block is accessible (forever as of now, but this might change with Serenity). The Log and its event data is not accessible from within contracts (not even from the contract that created them).

It is possible to request a Merkle proof for logs, so if an external entity supplies a contract with such a proof, it can check that the log actually exists inside the blockchain. You have to supply block headers because the contract can only see the last 256 block hashes.

You can add the attribute `indexed` to up to three parameters which adds them to a special data structure known as [“topics”](abi-spec.html#abi-events) instead of the data part of the log. A topic can only hold a single word (32 bytes) so if you use a [reference type](types.html#reference-types) for an indexed argument, the Keccak-256 hash of the value is stored as a topic instead.

All parameters without the `indexed` attribute are [ABI-encoded](abi-spec.html#abi) into the data part of the log.

Topics allow you to search for events, for example when filtering a sequence of blocks for certain events. You can also filter events by the address of the contract that emitted the event.

For example, the code below uses the web3.js `subscribe("logs")` [method](https://web3js.readthedocs.io/en/1.0/web3-eth-subscribe.html#subscribe-logs) to filter logs that match a topic with a certain address value:

var options = {
    fromBlock: 0,
    address: web3.eth.defaultAccount,
    topics: ["0x0000000000000000000000000000000000000000000000000000000000000000", null, null]
};
web3.eth.subscribe('logs', options, function (error, result) {
    if (!error)
        console.log(result);
})
    .on("data", function (log) {
        console.log(log);
    })
    .on("changed", function (log) {
});

The hash of the signature of the event is one of the topics, except if you declared the event with the `anonymous` specifier. This means that it is not possible to filter for specific anonymous events by name, you can only filter by the contract address. The advantage of anonymous events is that they are cheaper to deploy and call. It also allows you to declare four indexed arguments rather than three.

Note

Since the transaction log only stores the event data and not the type, you have to know the type of the event, including which parameter is indexed and if the event is anonymous in order to correctly interpret the data. In particular, it is possible to “fake” the signature of another event using an anonymous event.

### Members of Events[](#members-of-events "Permalink to this heading")

- `event.selector`: For non-anonymous events, this is a `bytes32` value containing the `keccak256` hash of the event signature, as used in the default topic.
    

### Example[](#example "Permalink to this heading")

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjIxIDwwLjkuMDsKCmNvbnRyYWN0IENsaWVudFJlY2VpcHQgewogICAgZXZlbnQgRGVwb3NpdCgKICAgICAgICBhZGRyZXNzIGluZGV4ZWQgZnJvbSwKICAgICAgICBieXRlczMyIGluZGV4ZWQgaWQsCiAgICAgICAgdWludCB2YWx1ZQogICAgKTsKCiAgICBmdW5jdGlvbiBkZXBvc2l0KGJ5dGVzMzIgaWQpIHB1YmxpYyBwYXlhYmxlIHsKICAgICAgICAvLyBFdmVudHMgYXJlIGVtaXR0ZWQgdXNpbmcgYGVtaXRgLCBmb2xsb3dlZCBieQogICAgICAgIC8vIHRoZSBuYW1lIG9mIHRoZSBldmVudCBhbmQgdGhlIGFyZ3VtZW50cwogICAgICAgIC8vIChpZiBhbnkpIGluIHBhcmVudGhlc2VzLiBBbnkgc3VjaCBpbnZvY2F0aW9uCiAgICAgICAgLy8gKGV2ZW4gZGVlcGx5IG5lc3RlZCkgY2FuIGJlIGRldGVjdGVkIGZyb20KICAgICAgICAvLyB0aGUgSmF2YVNjcmlwdCBBUEkgYnkgZmlsdGVyaW5nIGZvciBgRGVwb3NpdGAuCiAgICAgICAgZW1pdCBEZXBvc2l0KG1zZy5zZW5kZXIsIGlkLCBtc2cudmFsdWUpOwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.21 <0.9.0;

contract ClientReceipt {
    event Deposit(
        address indexed from,
        bytes32 indexed id,
        uint value
    );

    function deposit(bytes32 id) public payable {
        // Events are emitted using `emit`, followed by
        // the name of the event and the arguments
        // (if any) in parentheses. Any such invocation
        // (even deeply nested) can be detected from
        // the JavaScript API by filtering for `Deposit`.
        emit Deposit(msg.sender, id, msg.value);
    }
}

The use in the JavaScript API is as follows:

var abi = /* abi as generated by the compiler */;
var ClientReceipt = web3.eth.contract(abi);
var clientReceipt = ClientReceipt.at("0x1234...ab67" /* address */);

var depositEvent = clientReceipt.Deposit();

// watch for changes
depositEvent.watch(function(error, result){
    // result contains non-indexed arguments and topics
    // given to the `Deposit` call.
    if (!error)
        console.log(result);
});

// Or pass a callback to start watching immediately
var depositEvent = clientReceipt.Deposit(function(error, result) {
    if (!error)
        console.log(result);
});

The output of the above looks like the following (trimmed):

{
   "returnValues": {
       "from": "0x1111…FFFFCCCC",
       "id": "0x50…sd5adb20",
       "value": "0x420042"
   },
   "raw": {
       "data": "0x7f…91385",
       "topics": ["0xfd4…b4ead7", "0x7f…1a91385"]
   }
}

### Additional Resources for Understanding Events[](#additional-resources-for-understanding-events "Permalink to this heading")

- [JavaScript documentation](https://github.com/web3/web3.js/blob/1.x/docs/web3-eth-contract.rst#events)
    
- [Example usage of events](https://github.com/ethchange/smart-exchange/blob/master/lib/contracts/SmartExchange.sol)
    
- [How to access them in js](https://github.com/ethchange/smart-exchange/blob/master/lib/exchange_transactions.js)
    

## Errors and the Revert Statement[](#errors-and-the-revert-statement "Permalink to this heading")

Errors in Solidity provide a convenient and gas-efficient way to explain to the user why an operation failed. They can be defined inside and outside of contracts (including interfaces and libraries).

They have to be used together with the [revert statement](control-structures.html#revert-statement) which causes all changes in the current call to be reverted and passes the error data back to the caller.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguNDsKCi8vLyBJbnN1ZmZpY2llbnQgYmFsYW5jZSBmb3IgdHJhbnNmZXIuIE5lZWRlZCBgcmVxdWlyZWRgIGJ1dCBvbmx5Ci8vLyBgYXZhaWxhYmxlYCBhdmFpbGFibGUuCi8vLyBAcGFyYW0gYXZhaWxhYmxlIGJhbGFuY2UgYXZhaWxhYmxlLgovLy8gQHBhcmFtIHJlcXVpcmVkIHJlcXVlc3RlZCBhbW91bnQgdG8gdHJhbnNmZXIuCmVycm9yIEluc3VmZmljaWVudEJhbGFuY2UodWludDI1NiBhdmFpbGFibGUsIHVpbnQyNTYgcmVxdWlyZWQpOwoKY29udHJhY3QgVGVzdFRva2VuIHsKICAgIG1hcHBpbmcoYWRkcmVzcyA9PiB1aW50KSBiYWxhbmNlOwogICAgZnVuY3Rpb24gdHJhbnNmZXIoYWRkcmVzcyB0bywgdWludDI1NiBhbW91bnQpIHB1YmxpYyB7CiAgICAgICAgaWYgKGFtb3VudCA+IGJhbGFuY2VbbXNnLnNlbmRlcl0pCiAgICAgICAgICAgIHJldmVydCBJbnN1ZmZpY2llbnRCYWxhbmNlKHsKICAgICAgICAgICAgICAgIGF2YWlsYWJsZTogYmFsYW5jZVttc2cuc2VuZGVyXSwKICAgICAgICAgICAgICAgIHJlcXVpcmVkOiBhbW91bnQKICAgICAgICAgICAgfSk7CiAgICAgICAgYmFsYW5jZVttc2cuc2VuZGVyXSAtPSBhbW91bnQ7CiAgICAgICAgYmFsYW5jZVt0b10gKz0gYW1vdW50OwogICAgfQogICAgLy8gLi4uCn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.4;

/// Insufficient balance for transfer. Needed `required` but only
/// `available` available.
/// @param available balance available.
/// @param required requested amount to transfer.
error InsufficientBalance(uint256 available, uint256 required);

contract TestToken {
    mapping(address => uint) balance;
    function transfer(address to, uint256 amount) public {
        if (amount > balance[msg.sender])
            revert InsufficientBalance({
                available: balance[msg.sender],
                required: amount
            });
        balance[msg.sender] -= amount;
        balance[to] += amount;
    }
    // ...
}

Errors cannot be overloaded or overridden but are inherited. The same error can be defined in multiple places as long as the scopes are distinct. Instances of errors can only be created using `revert` statements.

The error creates data that is then passed to the caller with the revert operation to either return to the off-chain component or catch it in a [try/catch statement](control-structures.html#try-catch). Note that an error can only be caught when coming from an external call, reverts happening in internal calls or inside the same function cannot be caught.

If you do not provide any parameters, the error only needs four bytes of data and you can use [NatSpec](natspec-format.html#natspec) as above to further explain the reasons behind the error, which is not stored on chain. This makes this a very cheap and convenient error-reporting feature at the same time.

More specifically, an error instance is ABI-encoded in the same way as a function call to a function of the same name and types would be and then used as the return data in the `revert` opcode. This means that the data consists of a 4-byte selector followed by [ABI-encoded](abi-spec.html#abi) data. The selector consists of the first four bytes of the keccak256-hash of the signature of the error type.

Note

It is possible for a contract to revert with different errors of the same name or even with errors defined in different places that are indistinguishable by the caller. For the outside, i.e. the ABI, only the name of the error is relevant, not the contract or file where it is defined.

The statement `require(condition, "description");` would be equivalent to `if (!condition) revert Error("description")` if you could define `error Error(string)`. Note, however, that `Error` is a built-in type and cannot be defined in user-supplied code.

Similarly, a failing `assert` or similar conditions will revert with an error of the built-in type `Panic(uint256)`.

Note

Error data should only be used to give an indication of failure, but not as a means for control-flow. The reason is that the revert data of inner calls is propagated back through the chain of external calls by default. This means that an inner call can “forge” revert data that looks like it could have come from the contract that called it.

### Members of Errors[](#members-of-errors "Permalink to this heading")

- `error.selector`: A `bytes4` value containing the error selector.
    

## Inheritance[](#inheritance "Permalink to this heading")

Solidity supports multiple inheritance including polymorphism.

Polymorphism means that a function call (internal and external) always executes the function of the same name (and parameter types) in the most derived contract in the inheritance hierarchy. This has to be explicitly enabled on each function in the hierarchy using the `virtual` and `override` keywords. See [Function Overriding](#function-overriding) for more details.

It is possible to call functions further up in the inheritance hierarchy internally by explicitly specifying the contract using `ContractName.functionName()` or using `super.functionName()` if you want to call the function one level higher up in the flattened inheritance hierarchy (see below).

When a contract inherits from other contracts, only a single contract is created on the blockchain, and the code from all the base contracts is compiled into the created contract. This means that all internal calls to functions of base contracts also just use internal function calls (`super.f(..)` will use JUMP and not a message call).

State variable shadowing is considered as an error. A derived contract can only declare a state variable `x`, if there is no visible state variable with the same name in any of its bases.

The general inheritance system is very similar to [Python’s](https://docs.python.org/3/tutorial/classes.html#inheritance), especially concerning multiple inheritance, but there are also some [differences](#multi-inheritance).

Details are given in the following example.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwovLyBUaGlzIHdpbGwgcmVwb3J0IGEgd2FybmluZyBkdWUgdG8gZGVwcmVjYXRlZCBzZWxmZGVzdHJ1Y3QKCmNvbnRyYWN0IE93bmVkIHsKICAgIGNvbnN0cnVjdG9yKCkgeyBvd25lciA9IHBheWFibGUobXNnLnNlbmRlcik7IH0KICAgIGFkZHJlc3MgcGF5YWJsZSBvd25lcjsKfQoKCi8vIFVzZSBgaXNgIHRvIGRlcml2ZSBmcm9tIGFub3RoZXIgY29udHJhY3QuIERlcml2ZWQKLy8gY29udHJhY3RzIGNhbiBhY2Nlc3MgYWxsIG5vbi1wcml2YXRlIG1lbWJlcnMgaW5jbHVkaW5nCi8vIGludGVybmFsIGZ1bmN0aW9ucyBhbmQgc3RhdGUgdmFyaWFibGVzLiBUaGVzZSBjYW5ub3QgYmUKLy8gYWNjZXNzZWQgZXh0ZXJuYWxseSB2aWEgYHRoaXNgLCB0aG91Z2guCmNvbnRyYWN0IERlc3RydWN0aWJsZSBpcyBPd25lZCB7CiAgICAvLyBUaGUga2V5d29yZCBgdmlydHVhbGAgbWVhbnMgdGhhdCB0aGUgZnVuY3Rpb24gY2FuIGNoYW5nZQogICAgLy8gaXRzIGJlaGF2aW9yIGluIGRlcml2ZWQgY2xhc3NlcyAoIm92ZXJyaWRpbmciKS4KICAgIGZ1bmN0aW9uIGRlc3Ryb3koKSB2aXJ0dWFsIHB1YmxpYyB7CiAgICAgICAgaWYgKG1zZy5zZW5kZXIgPT0gb3duZXIpIHNlbGZkZXN0cnVjdChvd25lcik7CiAgICB9Cn0KCgovLyBUaGVzZSBhYnN0cmFjdCBjb250cmFjdHMgYXJlIG9ubHkgcHJvdmlkZWQgdG8gbWFrZSB0aGUKLy8gaW50ZXJmYWNlIGtub3duIHRvIHRoZSBjb21waWxlci4gTm90ZSB0aGUgZnVuY3Rpb24KLy8gd2l0aG91dCBib2R5LiBJZiBhIGNvbnRyYWN0IGRvZXMgbm90IGltcGxlbWVudCBhbGwKLy8gZnVuY3Rpb25zIGl0IGNhbiBvbmx5IGJlIHVzZWQgYXMgYW4gaW50ZXJmYWNlLgphYnN0cmFjdCBjb250cmFjdCBDb25maWcgewogICAgZnVuY3Rpb24gbG9va3VwKHVpbnQgaWQpIHB1YmxpYyB2aXJ0dWFsIHJldHVybnMgKGFkZHJlc3MgYWRyKTsKfQoKCmFic3RyYWN0IGNvbnRyYWN0IE5hbWVSZWcgewogICAgZnVuY3Rpb24gcmVnaXN0ZXIoYnl0ZXMzMiBuYW1lKSBwdWJsaWMgdmlydHVhbDsKICAgIGZ1bmN0aW9uIHVucmVnaXN0ZXIoKSBwdWJsaWMgdmlydHVhbDsKfQoKCi8vIE11bHRpcGxlIGluaGVyaXRhbmNlIGlzIHBvc3NpYmxlLiBOb3RlIHRoYXQgYE93bmVkYCBpcwovLyBhbHNvIGEgYmFzZSBjbGFzcyBvZiBgRGVzdHJ1Y3RpYmxlYCwgeWV0IHRoZXJlIGlzIG9ubHkgYSBzaW5nbGUKLy8gaW5zdGFuY2Ugb2YgYE93bmVkYCAoYXMgZm9yIHZpcnR1YWwgaW5oZXJpdGFuY2UgaW4gQysrKS4KY29udHJhY3QgTmFtZWQgaXMgT3duZWQsIERlc3RydWN0aWJsZSB7CiAgICBjb25zdHJ1Y3RvcihieXRlczMyIG5hbWUpIHsKICAgICAgICBDb25maWcgY29uZmlnID0gQ29uZmlnKDB4RDVmOUQ4RDk0ODg2RTcwYjA2RTQ3NGMzZkIxNEZkNDNFMmYyMzk3MCk7CiAgICAgICAgTmFtZVJlZyhjb25maWcubG9va3VwKDEpKS5yZWdpc3RlcihuYW1lKTsKICAgIH0KCiAgICAvLyBGdW5jdGlvbnMgY2FuIGJlIG92ZXJyaWRkZW4gYnkgYW5vdGhlciBmdW5jdGlvbiB3aXRoIHRoZSBzYW1lIG5hbWUgYW5kCiAgICAvLyB0aGUgc2FtZSBudW1iZXIvdHlwZXMgb2YgaW5wdXRzLiAgSWYgdGhlIG92ZXJyaWRpbmcgZnVuY3Rpb24gaGFzIGRpZmZlcmVudAogICAgLy8gdHlwZXMgb2Ygb3V0cHV0IHBhcmFtZXRlcnMsIHRoYXQgY2F1c2VzIGFuIGVycm9yLgogICAgLy8gQm90aCBsb2NhbCBhbmQgbWVzc2FnZS1iYXNlZCBmdW5jdGlvbiBjYWxscyB0YWtlIHRoZXNlIG92ZXJyaWRlcwogICAgLy8gaW50byBhY2NvdW50LgogICAgLy8gSWYgeW91IHdhbnQgdGhlIGZ1bmN0aW9uIHRvIG92ZXJyaWRlLCB5b3UgbmVlZCB0byB1c2UgdGhlCiAgICAvLyBgb3ZlcnJpZGVgIGtleXdvcmQuIFlvdSBuZWVkIHRvIHNwZWNpZnkgdGhlIGB2aXJ0dWFsYCBrZXl3b3JkIGFnYWluCiAgICAvLyBpZiB5b3Ugd2FudCB0aGlzIGZ1bmN0aW9uIHRvIGJlIG92ZXJyaWRkZW4gYWdhaW4uCiAgICBmdW5jdGlvbiBkZXN0cm95KCkgcHVibGljIHZpcnR1YWwgb3ZlcnJpZGUgewogICAgICAgIGlmIChtc2cuc2VuZGVyID09IG93bmVyKSB7CiAgICAgICAgICAgIENvbmZpZyBjb25maWcgPSBDb25maWcoMHhENWY5RDhEOTQ4ODZFNzBiMDZFNDc0YzNmQjE0RmQ0M0UyZjIzOTcwKTsKICAgICAgICAgICAgTmFtZVJlZyhjb25maWcubG9va3VwKDEpKS51bnJlZ2lzdGVyKCk7CiAgICAgICAgICAgIC8vIEl0IGlzIHN0aWxsIHBvc3NpYmxlIHRvIGNhbGwgYSBzcGVjaWZpYwogICAgICAgICAgICAvLyBvdmVycmlkZGVuIGZ1bmN0aW9uLgogICAgICAgICAgICBEZXN0cnVjdGlibGUuZGVzdHJveSgpOwogICAgICAgIH0KICAgIH0KfQoKCi8vIElmIGEgY29uc3RydWN0b3IgdGFrZXMgYW4gYXJndW1lbnQsIGl0IG5lZWRzIHRvIGJlCi8vIHByb3ZpZGVkIGluIHRoZSBoZWFkZXIgb3IgbW9kaWZpZXItaW52b2NhdGlvbi1zdHlsZSBhdAovLyB0aGUgY29uc3RydWN0b3Igb2YgdGhlIGRlcml2ZWQgY29udHJhY3QgKHNlZSBiZWxvdykuCmNvbnRyYWN0IFByaWNlRmVlZCBpcyBPd25lZCwgRGVzdHJ1Y3RpYmxlLCBOYW1lZCgiR29sZEZlZWQiKSB7CiAgICBmdW5jdGlvbiB1cGRhdGVJbmZvKHVpbnQgbmV3SW5mbykgcHVibGljIHsKICAgICAgICBpZiAobXNnLnNlbmRlciA9PSBvd25lcikgaW5mbyA9IG5ld0luZm87CiAgICB9CgogICAgLy8gSGVyZSwgd2Ugb25seSBzcGVjaWZ5IGBvdmVycmlkZWAgYW5kIG5vdCBgdmlydHVhbGAuCiAgICAvLyBUaGlzIG1lYW5zIHRoYXQgY29udHJhY3RzIGRlcml2aW5nIGZyb20gYFByaWNlRmVlZGAKICAgIC8vIGNhbm5vdCBjaGFuZ2UgdGhlIGJlaGF2aW9yIG9mIGBkZXN0cm95YCBhbnltb3JlLgogICAgZnVuY3Rpb24gZGVzdHJveSgpIHB1YmxpYyBvdmVycmlkZShEZXN0cnVjdGlibGUsIE5hbWVkKSB7IE5hbWVkLmRlc3Ryb3koKTsgfQogICAgZnVuY3Rpb24gZ2V0KCkgcHVibGljIHZpZXcgcmV0dXJucyh1aW50IHIpIHsgcmV0dXJuIGluZm87IH0KCiAgICB1aW50IGluZm87Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;
// This will report a warning due to deprecated selfdestruct

contract Owned {
    constructor() { owner = payable(msg.sender); }
    address payable owner;
}

// Use `is` to derive from another contract. Derived
// contracts can access all non-private members including
// internal functions and state variables. These cannot be
// accessed externally via `this`, though.
contract Destructible is Owned {
    // The keyword `virtual` means that the function can change
    // its behavior in derived classes ("overriding").
    function destroy() virtual public {
        if (msg.sender == owner) selfdestruct(owner);
    }
}

// These abstract contracts are only provided to make the
// interface known to the compiler. Note the function
// without body. If a contract does not implement all
// functions it can only be used as an interface.
abstract contract Config {
    function lookup(uint id) public virtual returns (address adr);
}

abstract contract NameReg {
    function register(bytes32 name) public virtual;
    function unregister() public virtual;
}

// Multiple inheritance is possible. Note that `Owned` is
// also a base class of `Destructible`, yet there is only a single
// instance of `Owned` (as for virtual inheritance in C++).
contract Named is Owned, Destructible {
    constructor(bytes32 name) {
        Config config = Config(0xD5f9D8D94886E70b06E474c3fB14Fd43E2f23970);
        NameReg(config.lookup(1)).register(name);
    }

    // Functions can be overridden by another function with the same name and
    // the same number/types of inputs.  If the overriding function has different
    // types of output parameters, that causes an error.
    // Both local and message-based function calls take these overrides
    // into account.
    // If you want the function to override, you need to use the
    // `override` keyword. You need to specify the `virtual` keyword again
    // if you want this function to be overridden again.
    function destroy() public virtual override {
        if (msg.sender == owner) {
            Config config = Config(0xD5f9D8D94886E70b06E474c3fB14Fd43E2f23970);
            NameReg(config.lookup(1)).unregister();
            // It is still possible to call a specific
            // overridden function.
            Destructible.destroy();
        }
    }
}

// If a constructor takes an argument, it needs to be
// provided in the header or modifier-invocation-style at
// the constructor of the derived contract (see below).
contract PriceFeed is Owned, Destructible, Named("GoldFeed") {
    function updateInfo(uint newInfo) public {
        if (msg.sender == owner) info = newInfo;
    }

    // Here, we only specify `override` and not `virtual`.
    // This means that contracts deriving from `PriceFeed`
    // cannot change the behavior of `destroy` anymore.
    function destroy() public override(Destructible, Named) { Named.destroy(); }
    function get() public view returns(uint r) { return info; }

    uint info;
}

Note that above, we call `Destructible.destroy()` to “forward” the destruction request. The way this is done is problematic, as seen in the following example:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwovLyBUaGlzIHdpbGwgcmVwb3J0IGEgd2FybmluZyBkdWUgdG8gZGVwcmVjYXRlZCBzZWxmZGVzdHJ1Y3QKCmNvbnRyYWN0IG93bmVkIHsKICAgIGNvbnN0cnVjdG9yKCkgeyBvd25lciA9IHBheWFibGUobXNnLnNlbmRlcik7IH0KICAgIGFkZHJlc3MgcGF5YWJsZSBvd25lcjsKfQoKY29udHJhY3QgRGVzdHJ1Y3RpYmxlIGlzIG93bmVkIHsKICAgIGZ1bmN0aW9uIGRlc3Ryb3koKSBwdWJsaWMgdmlydHVhbCB7CiAgICAgICAgaWYgKG1zZy5zZW5kZXIgPT0gb3duZXIpIHNlbGZkZXN0cnVjdChvd25lcik7CiAgICB9Cn0KCmNvbnRyYWN0IEJhc2UxIGlzIERlc3RydWN0aWJsZSB7CiAgICBmdW5jdGlvbiBkZXN0cm95KCkgcHVibGljIHZpcnR1YWwgb3ZlcnJpZGUgeyAvKiBkbyBjbGVhbnVwIDEgKi8gRGVzdHJ1Y3RpYmxlLmRlc3Ryb3koKTsgfQp9Cgpjb250cmFjdCBCYXNlMiBpcyBEZXN0cnVjdGlibGUgewogICAgZnVuY3Rpb24gZGVzdHJveSgpIHB1YmxpYyB2aXJ0dWFsIG92ZXJyaWRlIHsgLyogZG8gY2xlYW51cCAyICovIERlc3RydWN0aWJsZS5kZXN0cm95KCk7IH0KfQoKY29udHJhY3QgRmluYWwgaXMgQmFzZTEsIEJhc2UyIHsKICAgIGZ1bmN0aW9uIGRlc3Ryb3koKSBwdWJsaWMgb3ZlcnJpZGUoQmFzZTEsIEJhc2UyKSB7IEJhc2UyLmRlc3Ryb3koKTsgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;
// This will report a warning due to deprecated selfdestruct

contract owned {
    constructor() { owner = payable(msg.sender); }
    address payable owner;
}

contract Destructible is owned {
    function destroy() public virtual {
        if (msg.sender == owner) selfdestruct(owner);
    }
}

contract Base1 is Destructible {
    function destroy() public virtual override { /* do cleanup 1 */ Destructible.destroy(); }
}

contract Base2 is Destructible {
    function destroy() public virtual override { /* do cleanup 2 */ Destructible.destroy(); }
}

contract Final is Base1, Base2 {
    function destroy() public override(Base1, Base2) { Base2.destroy(); }
}

A call to `Final.destroy()` will call `Base2.destroy` because we specify it explicitly in the final override, but this function will bypass `Base1.destroy`. The way around this is to use `super`:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwovLyBUaGlzIHdpbGwgcmVwb3J0IGEgd2FybmluZyBkdWUgdG8gZGVwcmVjYXRlZCBzZWxmZGVzdHJ1Y3QKCmNvbnRyYWN0IG93bmVkIHsKICAgIGNvbnN0cnVjdG9yKCkgeyBvd25lciA9IHBheWFibGUobXNnLnNlbmRlcik7IH0KICAgIGFkZHJlc3MgcGF5YWJsZSBvd25lcjsKfQoKY29udHJhY3QgRGVzdHJ1Y3RpYmxlIGlzIG93bmVkIHsKICAgIGZ1bmN0aW9uIGRlc3Ryb3koKSB2aXJ0dWFsIHB1YmxpYyB7CiAgICAgICAgaWYgKG1zZy5zZW5kZXIgPT0gb3duZXIpIHNlbGZkZXN0cnVjdChvd25lcik7CiAgICB9Cn0KCmNvbnRyYWN0IEJhc2UxIGlzIERlc3RydWN0aWJsZSB7CiAgICBmdW5jdGlvbiBkZXN0cm95KCkgcHVibGljIHZpcnR1YWwgb3ZlcnJpZGUgeyAvKiBkbyBjbGVhbnVwIDEgKi8gc3VwZXIuZGVzdHJveSgpOyB9Cn0KCgpjb250cmFjdCBCYXNlMiBpcyBEZXN0cnVjdGlibGUgewogICAgZnVuY3Rpb24gZGVzdHJveSgpIHB1YmxpYyB2aXJ0dWFsIG92ZXJyaWRlIHsgLyogZG8gY2xlYW51cCAyICovIHN1cGVyLmRlc3Ryb3koKTsgfQp9Cgpjb250cmFjdCBGaW5hbCBpcyBCYXNlMSwgQmFzZTIgewogICAgZnVuY3Rpb24gZGVzdHJveSgpIHB1YmxpYyBvdmVycmlkZShCYXNlMSwgQmFzZTIpIHsgc3VwZXIuZGVzdHJveSgpOyB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;
// This will report a warning due to deprecated selfdestruct

contract owned {
    constructor() { owner = payable(msg.sender); }
    address payable owner;
}

contract Destructible is owned {
    function destroy() virtual public {
        if (msg.sender == owner) selfdestruct(owner);
    }
}

contract Base1 is Destructible {
    function destroy() public virtual override { /* do cleanup 1 */ super.destroy(); }
}

contract Base2 is Destructible {
    function destroy() public virtual override { /* do cleanup 2 */ super.destroy(); }
}

contract Final is Base1, Base2 {
    function destroy() public override(Base1, Base2) { super.destroy(); }
}

If `Base2` calls a function of `super`, it does not simply call this function on one of its base contracts. Rather, it calls this function on the next base contract in the final inheritance graph, so it will call `Base1.destroy()` (note that the final inheritance sequence is – starting with the most derived contract: Final, Base2, Base1, Destructible, owned). The actual function that is called when using super is not known in the context of the class where it is used, although its type is known. This is similar for ordinary virtual method lookup.

### Function Overriding[](#function-overriding "Permalink to this heading")

Base functions can be overridden by inheriting contracts to change their behavior if they are marked as `virtual`. The overriding function must then use the `override` keyword in the function header. The overriding function may only change the visibility of the overridden function from `external` to `public`. The mutability may be changed to a more strict one following the order: `nonpayable` can be overridden by `view` and `pure`. `view` can be overridden by `pure`. `payable` is an exception and cannot be changed to any other mutability.

The following example demonstrates changing mutability and visibility:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwoKY29udHJhY3QgQmFzZQp7CiAgICBmdW5jdGlvbiBmb28oKSB2aXJ0dWFsIGV4dGVybmFsIHZpZXcge30KfQoKY29udHJhY3QgTWlkZGxlIGlzIEJhc2Uge30KCmNvbnRyYWN0IEluaGVyaXRlZCBpcyBNaWRkbGUKewogICAgZnVuY3Rpb24gZm9vKCkgb3ZlcnJpZGUgcHVibGljIHB1cmUge30KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

contract Base
{
    function foo() virtual external view {}
}

contract Middle is Base {}

contract Inherited is Middle
{
    function foo() override public pure {}
}

For multiple inheritance, the most derived base contracts that define the same function must be specified explicitly after the `override` keyword. In other words, you have to specify all base contracts that define the same function and have not yet been overridden by another base contract (on some path through the inheritance graph). Additionally, if a contract inherits the same function from multiple (unrelated) bases, it has to explicitly override it:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKY29udHJhY3QgQmFzZTEKewogICAgZnVuY3Rpb24gZm9vKCkgdmlydHVhbCBwdWJsaWMge30KfQoKY29udHJhY3QgQmFzZTIKewogICAgZnVuY3Rpb24gZm9vKCkgdmlydHVhbCBwdWJsaWMge30KfQoKY29udHJhY3QgSW5oZXJpdGVkIGlzIEJhc2UxLCBCYXNlMgp7CiAgICAvLyBEZXJpdmVzIGZyb20gbXVsdGlwbGUgYmFzZXMgZGVmaW5pbmcgZm9vKCksIHNvIHdlIG11c3QgZXhwbGljaXRseQogICAgLy8gb3ZlcnJpZGUgaXQKICAgIGZ1bmN0aW9uIGZvbygpIHB1YmxpYyBvdmVycmlkZShCYXNlMSwgQmFzZTIpIHt9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

contract Base1
{
    function foo() virtual public {}
}

contract Base2
{
    function foo() virtual public {}
}

contract Inherited is Base1, Base2
{
    // Derives from multiple bases defining foo(), so we must explicitly
    // override it
    function foo() public override(Base1, Base2) {}
}

An explicit override specifier is not required if the function is defined in a common base contract or if there is a unique function in a common base contract that already overrides all other functions.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKY29udHJhY3QgQSB7IGZ1bmN0aW9uIGYoKSBwdWJsaWMgcHVyZXt9IH0KY29udHJhY3QgQiBpcyBBIHt9CmNvbnRyYWN0IEMgaXMgQSB7fQovLyBObyBleHBsaWNpdCBvdmVycmlkZSByZXF1aXJlZApjb250cmFjdCBEIGlzIEIsIEMge30=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

contract A { function f() public pure{} }
contract B is A {}
contract C is A {}
// No explicit override required
contract D is B, C {}

More formally, it is not required to override a function (directly or indirectly) inherited from multiple bases if there is a base contract that is part of all override paths for the signature, and (1) that base implements the function and no paths from the current contract to the base mentions a function with that signature or (2) that base does not implement the function and there is at most one mention of the function in all paths from the current contract to that base.

In this sense, an override path for a signature is a path through the inheritance graph that starts at the contract under consideration and ends at a contract mentioning a function with that signature that does not override.

If you do not mark a function that overrides as `virtual`, derived contracts can no longer change the behavior of that function.

Note

Functions with the `private` visibility cannot be `virtual`.

Note

Functions without implementation have to be marked `virtual` outside of interfaces. In interfaces, all functions are automatically considered `virtual`.

Note

Starting from Solidity 0.8.8, the `override` keyword is not required when overriding an interface function, except for the case where the function is defined in multiple bases.

Public state variables can override external functions if the parameter and return types of the function matches the getter function of the variable:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKY29udHJhY3QgQQp7CiAgICBmdW5jdGlvbiBmKCkgZXh0ZXJuYWwgdmlldyB2aXJ0dWFsIHJldHVybnModWludCkgeyByZXR1cm4gNTsgfQp9Cgpjb250cmFjdCBCIGlzIEEKewogICAgdWludCBwdWJsaWMgb3ZlcnJpZGUgZjsKfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

contract A
{
    function f() external view virtual returns(uint) { return 5; }
}

contract B is A
{
    uint public override f;
}

Note

While public state variables can override external functions, they themselves cannot be overridden.

### Modifier Overriding[](#modifier-overriding "Permalink to this heading")

Function modifiers can override each other. This works in the same way as [function overriding](#function-overriding) (except that there is no overloading for modifiers). The `virtual` keyword must be used on the overridden modifier and the `override` keyword must be used in the overriding modifier:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKY29udHJhY3QgQmFzZQp7CiAgICBtb2RpZmllciBmb28oKSB2aXJ0dWFsIHtfO30KfQoKY29udHJhY3QgSW5oZXJpdGVkIGlzIEJhc2UKewogICAgbW9kaWZpZXIgZm9vKCkgb3ZlcnJpZGUge187fQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

contract Base
{
    modifier foo() virtual {_;}
}

contract Inherited is Base
{
    modifier foo() override {_;}
}

In case of multiple inheritance, all direct base contracts must be specified explicitly:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKY29udHJhY3QgQmFzZTEKewogICAgbW9kaWZpZXIgZm9vKCkgdmlydHVhbCB7Xzt9Cn0KCmNvbnRyYWN0IEJhc2UyCnsKICAgIG1vZGlmaWVyIGZvbygpIHZpcnR1YWwge187fQp9Cgpjb250cmFjdCBJbmhlcml0ZWQgaXMgQmFzZTEsIEJhc2UyCnsKICAgIG1vZGlmaWVyIGZvbygpIG92ZXJyaWRlKEJhc2UxLCBCYXNlMikge187fQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

contract Base1
{
    modifier foo() virtual {_;}
}

contract Base2
{
    modifier foo() virtual {_;}
}

contract Inherited is Base1, Base2
{
    modifier foo() override(Base1, Base2) {_;}
}

### Constructors[](#constructors "Permalink to this heading")

A constructor is an optional function declared with the `constructor` keyword which is executed upon contract creation, and where you can run contract initialisation code.

Before the constructor code is executed, state variables are initialised to their specified value if you initialise them inline, or their [default value](control-structures.html#default-value) if you do not.

After the constructor has run, the final code of the contract is deployed to the blockchain. The deployment of the code costs additional gas linear to the length of the code. This code includes all functions that are part of the public interface and all functions that are reachable from there through function calls. It does not include the constructor code or internal functions that are only called from the constructor.

If there is no constructor, the contract will assume the default constructor, which is equivalent to `constructor() {}`. For example:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwoKYWJzdHJhY3QgY29udHJhY3QgQSB7CiAgICB1aW50IHB1YmxpYyBhOwoKICAgIGNvbnN0cnVjdG9yKHVpbnQgYV8pIHsKICAgICAgICBhID0gYV87CiAgICB9Cn0KCmNvbnRyYWN0IEIgaXMgQSgxKSB7CiAgICBjb25zdHJ1Y3RvcigpIHt9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

abstract contract A {
    uint public a;

    constructor(uint a_) {
        a = a_;
    }
}

contract B is A(1) {
    constructor() {}
}

You can use internal parameters in a constructor (for example storage pointers). In this case, the contract has to be marked [abstract](#abstract-contract), because these parameters cannot be assigned valid values from outside but only through the constructors of derived contracts.

Warning

Prior to version 0.4.22, constructors were defined as functions with the same name as the contract. This syntax was deprecated and is not allowed anymore in version 0.5.0.

Warning

Prior to version 0.7.0, you had to specify the visibility of constructors as either `internal` or `public`.

### Arguments for Base Constructors[](#arguments-for-base-constructors "Permalink to this heading")

The constructors of all the base contracts will be called following the linearization rules explained below. If the base constructors have arguments, derived contracts need to specify all of them. This can be done in two ways:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwoKY29udHJhY3QgQmFzZSB7CiAgICB1aW50IHg7CiAgICBjb25zdHJ1Y3Rvcih1aW50IHhfKSB7IHggPSB4XzsgfQp9CgovLyBFaXRoZXIgZGlyZWN0bHkgc3BlY2lmeSBpbiB0aGUgaW5oZXJpdGFuY2UgbGlzdC4uLgpjb250cmFjdCBEZXJpdmVkMSBpcyBCYXNlKDcpIHsKICAgIGNvbnN0cnVjdG9yKCkge30KfQoKLy8gb3IgdGhyb3VnaCBhICJtb2RpZmllciIgb2YgdGhlIGRlcml2ZWQgY29uc3RydWN0b3IuLi4KY29udHJhY3QgRGVyaXZlZDIgaXMgQmFzZSB7CiAgICBjb25zdHJ1Y3Rvcih1aW50IHkpIEJhc2UoeSAqIHkpIHt9Cn0KCi8vIG9yIGRlY2xhcmUgYWJzdHJhY3QuLi4KYWJzdHJhY3QgY29udHJhY3QgRGVyaXZlZDMgaXMgQmFzZSB7Cn0KCi8vIGFuZCBoYXZlIHRoZSBuZXh0IGNvbmNyZXRlIGRlcml2ZWQgY29udHJhY3QgaW5pdGlhbGl6ZSBpdC4KY29udHJhY3QgRGVyaXZlZEZyb21EZXJpdmVkIGlzIERlcml2ZWQzIHsKICAgIGNvbnN0cnVjdG9yKCkgQmFzZSgxMCArIDEwKSB7fQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

contract Base {
    uint x;
    constructor(uint x_) { x = x_; }
}

// Either directly specify in the inheritance list...
contract Derived1 is Base(7) {
    constructor() {}
}

// or through a "modifier" of the derived constructor...
contract Derived2 is Base {
    constructor(uint y) Base(y * y) {}
}

// or declare abstract...
abstract contract Derived3 is Base {
}

// and have the next concrete derived contract initialize it.
contract DerivedFromDerived is Derived3 {
    constructor() Base(10 + 10) {}
}

One way is directly in the inheritance list (`is Base(7)`). The other is in the way a modifier is invoked as part of the derived constructor (`Base(y * y)`). The first way to do it is more convenient if the constructor argument is a constant and defines the behavior of the contract or describes it. The second way has to be used if the constructor arguments of the base depend on those of the derived contract. Arguments have to be given either in the inheritance list or in modifier-style in the derived constructor. Specifying arguments in both places is an error.

If a derived contract does not specify the arguments to all of its base contracts’ constructors, it must be declared abstract. In that case, when another contract derives from it, that other contract’s inheritance list or constructor must provide the necessary parameters for all base classes that haven’t had their parameters specified (otherwise, that other contract must be declared abstract as well). For example, in the above code snippet, see `Derived3` and `DerivedFromDerived`.

### Multiple Inheritance and Linearization[](#multiple-inheritance-and-linearization "Permalink to this heading")

Languages that allow multiple inheritance have to deal with several problems. One is the [Diamond Problem](https://en.wikipedia.org/wiki/Multiple_inheritance#The_diamond_problem). Solidity is similar to Python in that it uses “[C3 Linearization](https://en.wikipedia.org/wiki/C3_linearization)” to force a specific order in the directed acyclic graph (DAG) of base classes. This results in the desirable property of monotonicity but disallows some inheritance graphs. Especially, the order in which the base classes are given in the `is` directive is important: You have to list the direct base contracts in the order from “most base-like” to “most derived”. Note that this order is the reverse of the one used in Python.

Another simplifying way to explain this is that when a function is called that is defined multiple times in different contracts, the given bases are searched from right to left (left to right in Python) in a depth-first manner, stopping at the first match. If a base contract has already been searched, it is skipped.

In the following code, Solidity will give the error “Linearization of inheritance graph impossible”.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKY29udHJhY3QgWCB7fQpjb250cmFjdCBBIGlzIFgge30KLy8gVGhpcyB3aWxsIG5vdCBjb21waWxlCmNvbnRyYWN0IEMgaXMgQSwgWCB7fQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract X {}
contract A is X {}
// This will not compile
contract C is A, X {}

The reason for this is that `C` requests `X` to override `A` (by specifying `A, X` in this order), but `A` itself requests to override `X`, which is a contradiction that cannot be resolved.

Due to the fact that you have to explicitly override a function that is inherited from multiple bases without a unique override, C3 linearization is not too important in practice.

One area where inheritance linearization is especially important and perhaps not as clear is when there are multiple constructors in the inheritance hierarchy. The constructors will always be executed in the linearized order, regardless of the order in which their arguments are provided in the inheriting contract’s constructor. For example:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwoKY29udHJhY3QgQmFzZTEgewogICAgY29uc3RydWN0b3IoKSB7fQp9Cgpjb250cmFjdCBCYXNlMiB7CiAgICBjb25zdHJ1Y3RvcigpIHt9Cn0KCi8vIENvbnN0cnVjdG9ycyBhcmUgZXhlY3V0ZWQgaW4gdGhlIGZvbGxvd2luZyBvcmRlcjoKLy8gIDEgLSBCYXNlMQovLyAgMiAtIEJhc2UyCi8vICAzIC0gRGVyaXZlZDEKY29udHJhY3QgRGVyaXZlZDEgaXMgQmFzZTEsIEJhc2UyIHsKICAgIGNvbnN0cnVjdG9yKCkgQmFzZTEoKSBCYXNlMigpIHt9Cn0KCi8vIENvbnN0cnVjdG9ycyBhcmUgZXhlY3V0ZWQgaW4gdGhlIGZvbGxvd2luZyBvcmRlcjoKLy8gIDEgLSBCYXNlMgovLyAgMiAtIEJhc2UxCi8vICAzIC0gRGVyaXZlZDIKY29udHJhY3QgRGVyaXZlZDIgaXMgQmFzZTIsIEJhc2UxIHsKICAgIGNvbnN0cnVjdG9yKCkgQmFzZTIoKSBCYXNlMSgpIHt9Cn0KCi8vIENvbnN0cnVjdG9ycyBhcmUgc3RpbGwgZXhlY3V0ZWQgaW4gdGhlIGZvbGxvd2luZyBvcmRlcjoKLy8gIDEgLSBCYXNlMgovLyAgMiAtIEJhc2UxCi8vICAzIC0gRGVyaXZlZDMKY29udHJhY3QgRGVyaXZlZDMgaXMgQmFzZTIsIEJhc2UxIHsKICAgIGNvbnN0cnVjdG9yKCkgQmFzZTEoKSBCYXNlMigpIHt9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

contract Base1 {
    constructor() {}
}

contract Base2 {
    constructor() {}
}

// Constructors are executed in the following order:
//  1 - Base1
//  2 - Base2
//  3 - Derived1
contract Derived1 is Base1, Base2 {
    constructor() Base1() Base2() {}
}

// Constructors are executed in the following order:
//  1 - Base2
//  2 - Base1
//  3 - Derived2
contract Derived2 is Base2, Base1 {
    constructor() Base2() Base1() {}
}

// Constructors are still executed in the following order:
//  1 - Base2
//  2 - Base1
//  3 - Derived3
contract Derived3 is Base2, Base1 {
    constructor() Base1() Base2() {}
}

### Inheriting Different Kinds of Members of the Same Name[](#inheriting-different-kinds-of-members-of-the-same-name "Permalink to this heading")

It is an error when any of the following pairs in a contract have the same name due to inheritance:

- a function and a modifier
    
- a function and an event
    
- an event and a modifier
    

As an exception, a state variable getter can override an external function.

## Abstract Contracts[](#abstract-contracts "Permalink to this heading")

Contracts must be marked as abstract when at least one of their functions is not implemented or when they do not provide arguments for all of their base contract constructors. Even if this is not the case, a contract may still be marked abstract, such as when you do not intend for the contract to be created directly. Abstract contracts are similar to [Interfaces](#interfaces) but an interface is more limited in what it can declare.

An abstract contract is declared using the `abstract` keyword as shown in the following example. Note that this contract needs to be defined as abstract, because the function `utterance()` is declared, but no implementation was provided (no implementation body `{ }` was given).

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKYWJzdHJhY3QgY29udHJhY3QgRmVsaW5lIHsKICAgIGZ1bmN0aW9uIHV0dGVyYW5jZSgpIHB1YmxpYyB2aXJ0dWFsIHJldHVybnMgKGJ5dGVzMzIpOwp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

abstract contract Feline {
    function utterance() public virtual returns (bytes32);
}

Such abstract contracts can not be instantiated directly. This is also true, if an abstract contract itself does implement all defined functions. The usage of an abstract contract as a base class is shown in the following example:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKYWJzdHJhY3QgY29udHJhY3QgRmVsaW5lIHsKICAgIGZ1bmN0aW9uIHV0dGVyYW5jZSgpIHB1YmxpYyBwdXJlIHZpcnR1YWwgcmV0dXJucyAoYnl0ZXMzMik7Cn0KCmNvbnRyYWN0IENhdCBpcyBGZWxpbmUgewogICAgZnVuY3Rpb24gdXR0ZXJhbmNlKCkgcHVibGljIHB1cmUgb3ZlcnJpZGUgcmV0dXJucyAoYnl0ZXMzMikgeyByZXR1cm4gIm1pYW93IjsgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

abstract contract Feline {
    function utterance() public pure virtual returns (bytes32);
}

contract Cat is Feline {
    function utterance() public pure override returns (bytes32) { return "miaow"; }
}

If a contract inherits from an abstract contract and does not implement all non-implemented functions by overriding, it needs to be marked as abstract as well.

Note that a function without implementation is different from a [Function Type](types.html#function-types) even though their syntax looks very similar.

Example of function without implementation (a function declaration):

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=ZnVuY3Rpb24gZm9vKGFkZHJlc3MpIGV4dGVybmFsIHJldHVybnMgKGFkZHJlc3MpOw==)

function foo(address) external returns (address);

Example of a declaration of a variable whose type is a function type:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=ZnVuY3Rpb24oYWRkcmVzcykgZXh0ZXJuYWwgcmV0dXJucyAoYWRkcmVzcykgZm9vOw==)

function(address) external returns (address) foo;

Abstract contracts decouple the definition of a contract from its implementation providing better extensibility and self-documentation and facilitating patterns like the [Template method](https://en.wikipedia.org/wiki/Template_method_pattern) and removing code duplication. Abstract contracts are useful in the same way that defining methods in an interface is useful. It is a way for the designer of the abstract contract to say “any child of mine must implement this method”.

Note

Abstract contracts cannot override an implemented virtual function with an unimplemented one.

## Interfaces[](#interfaces "Permalink to this heading")

Interfaces are similar to abstract contracts, but they cannot have any functions implemented. There are further restrictions:

- They cannot inherit from other contracts, but they can inherit from other interfaces.
    
- All declared functions must be external in the interface, even if they are public in the contract.
    
- They cannot declare a constructor.
    
- They cannot declare state variables.
    
- They cannot declare modifiers.
    

Some of these restrictions might be lifted in the future.

Interfaces are basically limited to what the Contract ABI can represent, and the conversion between the ABI and an interface should be possible without any information loss.

Interfaces are denoted by their own keyword:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjIgPDAuOS4wOwoKaW50ZXJmYWNlIFRva2VuIHsKICAgIGVudW0gVG9rZW5UeXBlIHsgRnVuZ2libGUsIE5vbkZ1bmdpYmxlIH0KICAgIHN0cnVjdCBDb2luIHsgc3RyaW5nIG9idmVyc2U7IHN0cmluZyByZXZlcnNlOyB9CiAgICBmdW5jdGlvbiB0cmFuc2ZlcihhZGRyZXNzIHJlY2lwaWVudCwgdWludCBhbW91bnQpIGV4dGVybmFsOwp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.2 <0.9.0;

interface Token {
    enum TokenType { Fungible, NonFungible }
    struct Coin { string obverse; string reverse; }
    function transfer(address recipient, uint amount) external;
}

Contracts can inherit interfaces as they would inherit other contracts.

All functions declared in interfaces are implicitly `virtual` and any functions that override them do not need the `override` keyword. This does not automatically mean that an overriding function can be overridden again - this is only possible if the overriding function is marked `virtual`.

Interfaces can inherit from other interfaces. This has the same rules as normal inheritance.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjIgPDAuOS4wOwoKaW50ZXJmYWNlIFBhcmVudEEgewogICAgZnVuY3Rpb24gdGVzdCgpIGV4dGVybmFsIHJldHVybnMgKHVpbnQyNTYpOwp9CgppbnRlcmZhY2UgUGFyZW50QiB7CiAgICBmdW5jdGlvbiB0ZXN0KCkgZXh0ZXJuYWwgcmV0dXJucyAodWludDI1Nik7Cn0KCmludGVyZmFjZSBTdWJJbnRlcmZhY2UgaXMgUGFyZW50QSwgUGFyZW50QiB7CiAgICAvLyBNdXN0IHJlZGVmaW5lIHRlc3QgaW4gb3JkZXIgdG8gYXNzZXJ0IHRoYXQgdGhlIHBhcmVudAogICAgLy8gbWVhbmluZ3MgYXJlIGNvbXBhdGlibGUuCiAgICBmdW5jdGlvbiB0ZXN0KCkgZXh0ZXJuYWwgb3ZlcnJpZGUoUGFyZW50QSwgUGFyZW50QikgcmV0dXJucyAodWludDI1Nik7Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.2 <0.9.0;

interface ParentA {
    function test() external returns (uint256);
}

interface ParentB {
    function test() external returns (uint256);
}

interface SubInterface is ParentA, ParentB {
    // Must redefine test in order to assert that the parent
    // meanings are compatible.
    function test() external override(ParentA, ParentB) returns (uint256);
}

Types defined inside interfaces and other contract-like structures can be accessed from other contracts: `Token.TokenType` or `Token.Coin`.

Warning

Interfaces have supported `enum` types since [Solidity version 0.5.0](050-breaking-changes.html), make sure the pragma version specifies this version as a minimum.

## Libraries[](#libraries "Permalink to this heading")

Libraries are similar to contracts, but their purpose is that they are deployed only once at a specific address and their code is reused using the `DELEGATECALL` (`CALLCODE` until Homestead) feature of the EVM. This means that if library functions are called, their code is executed in the context of the calling contract, i.e. `this` points to the calling contract, and especially the storage from the calling contract can be accessed. As a library is an isolated piece of source code, it can only access state variables of the calling contract if they are explicitly supplied (it would have no way to name them, otherwise). Library functions can only be called directly (i.e. without the use of `DELEGATECALL`) if they do not modify the state (i.e. if they are `view` or `pure` functions), because libraries are assumed to be stateless. In particular, it is not possible to destroy a library.

Note

Until version 0.4.20, it was possible to destroy libraries by circumventing Solidity’s type system. Starting from that version, libraries contain a [mechanism](#call-protection) that disallows state-modifying functions to be called directly (i.e. without `DELEGATECALL`).

Libraries can be seen as implicit base contracts of the contracts that use them. They will not be explicitly visible in the inheritance hierarchy, but calls to library functions look just like calls to functions of explicit base contracts (using qualified access like `L.f()`). Of course, calls to internal functions use the internal calling convention, which means that all internal types can be passed and types [stored in memory](types.html#data-location) will be passed by reference and not copied. To realize this in the EVM, the code of internal library functions that are called from a contract and all functions called from therein will at compile time be included in the calling contract, and a regular `JUMP` call will be used instead of a `DELEGATECALL`.

Note

The inheritance analogy breaks down when it comes to public functions. Calling a public library function with `L.f()` results in an external call (`DELEGATECALL` to be precise). In contrast, `A.f()` is an internal call when `A` is a base contract of the current contract.

The following example illustrates how to use libraries (but using a manual method, be sure to check out [using for](#using-for) for a more advanced example to implement a set).

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKCi8vIFdlIGRlZmluZSBhIG5ldyBzdHJ1Y3QgZGF0YXR5cGUgdGhhdCB3aWxsIGJlIHVzZWQgdG8KLy8gaG9sZCBpdHMgZGF0YSBpbiB0aGUgY2FsbGluZyBjb250cmFjdC4Kc3RydWN0IERhdGEgewogICAgbWFwcGluZyh1aW50ID0+IGJvb2wpIGZsYWdzOwp9CgpsaWJyYXJ5IFNldCB7CiAgICAvLyBOb3RlIHRoYXQgdGhlIGZpcnN0IHBhcmFtZXRlciBpcyBvZiB0eXBlICJzdG9yYWdlCiAgICAvLyByZWZlcmVuY2UiIGFuZCB0aHVzIG9ubHkgaXRzIHN0b3JhZ2UgYWRkcmVzcyBhbmQgbm90CiAgICAvLyBpdHMgY29udGVudHMgaXMgcGFzc2VkIGFzIHBhcnQgb2YgdGhlIGNhbGwuICBUaGlzIGlzIGEKICAgIC8vIHNwZWNpYWwgZmVhdHVyZSBvZiBsaWJyYXJ5IGZ1bmN0aW9ucy4gIEl0IGlzIGlkaW9tYXRpYwogICAgLy8gdG8gY2FsbCB0aGUgZmlyc3QgcGFyYW1ldGVyIGBzZWxmYCwgaWYgdGhlIGZ1bmN0aW9uIGNhbgogICAgLy8gYmUgc2VlbiBhcyBhIG1ldGhvZCBvZiB0aGF0IG9iamVjdC4KICAgIGZ1bmN0aW9uIGluc2VydChEYXRhIHN0b3JhZ2Ugc2VsZiwgdWludCB2YWx1ZSkKICAgICAgICBwdWJsaWMKICAgICAgICByZXR1cm5zIChib29sKQogICAgewogICAgICAgIGlmIChzZWxmLmZsYWdzW3ZhbHVlXSkKICAgICAgICAgICAgcmV0dXJuIGZhbHNlOyAvLyBhbHJlYWR5IHRoZXJlCiAgICAgICAgc2VsZi5mbGFnc1t2YWx1ZV0gPSB0cnVlOwogICAgICAgIHJldHVybiB0cnVlOwogICAgfQoKICAgIGZ1bmN0aW9uIHJlbW92ZShEYXRhIHN0b3JhZ2Ugc2VsZiwgdWludCB2YWx1ZSkKICAgICAgICBwdWJsaWMKICAgICAgICByZXR1cm5zIChib29sKQogICAgewogICAgICAgIGlmICghc2VsZi5mbGFnc1t2YWx1ZV0pCiAgICAgICAgICAgIHJldHVybiBmYWxzZTsgLy8gbm90IHRoZXJlCiAgICAgICAgc2VsZi5mbGFnc1t2YWx1ZV0gPSBmYWxzZTsKICAgICAgICByZXR1cm4gdHJ1ZTsKICAgIH0KCiAgICBmdW5jdGlvbiBjb250YWlucyhEYXRhIHN0b3JhZ2Ugc2VsZiwgdWludCB2YWx1ZSkKICAgICAgICBwdWJsaWMKICAgICAgICB2aWV3CiAgICAgICAgcmV0dXJucyAoYm9vbCkKICAgIHsKICAgICAgICByZXR1cm4gc2VsZi5mbGFnc1t2YWx1ZV07CiAgICB9Cn0KCgpjb250cmFjdCBDIHsKICAgIERhdGEga25vd25WYWx1ZXM7CgogICAgZnVuY3Rpb24gcmVnaXN0ZXIodWludCB2YWx1ZSkgcHVibGljIHsKICAgICAgICAvLyBUaGUgbGlicmFyeSBmdW5jdGlvbnMgY2FuIGJlIGNhbGxlZCB3aXRob3V0IGEKICAgICAgICAvLyBzcGVjaWZpYyBpbnN0YW5jZSBvZiB0aGUgbGlicmFyeSwgc2luY2UgdGhlCiAgICAgICAgLy8gImluc3RhbmNlIiB3aWxsIGJlIHRoZSBjdXJyZW50IGNvbnRyYWN0LgogICAgICAgIHJlcXVpcmUoU2V0Lmluc2VydChrbm93blZhbHVlcywgdmFsdWUpKTsKICAgIH0KICAgIC8vIEluIHRoaXMgY29udHJhY3QsIHdlIGNhbiBhbHNvIGRpcmVjdGx5IGFjY2VzcyBrbm93blZhbHVlcy5mbGFncywgaWYgd2Ugd2FudC4KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

// We define a new struct datatype that will be used to
// hold its data in the calling contract.
struct Data {
    mapping(uint => bool) flags;
}

library Set {
    // Note that the first parameter is of type "storage
    // reference" and thus only its storage address and not
    // its contents is passed as part of the call.  This is a
    // special feature of library functions.  It is idiomatic
    // to call the first parameter `self`, if the function can
    // be seen as a method of that object.
    function insert(Data storage self, uint value)
        public
        returns (bool)
    {
        if (self.flags[value])
            return false; // already there
        self.flags[value] = true;
        return true;
    }

    function remove(Data storage self, uint value)
        public
        returns (bool)
    {
        if (!self.flags[value])
            return false; // not there
        self.flags[value] = false;
        return true;
    }

    function contains(Data storage self, uint value)
        public
        view
        returns (bool)
    {
        return self.flags[value];
    }
}

contract C {
    Data knownValues;

    function register(uint value) public {
        // The library functions can be called without a
        // specific instance of the library, since the
        // "instance" will be the current contract.
        require(Set.insert(knownValues, value));
    }
    // In this contract, we can also directly access knownValues.flags, if we want.
}

Of course, you do not have to follow this way to use libraries: they can also be used without defining struct data types. Functions also work without any storage reference parameters, and they can have multiple storage reference parameters and in any position.

The calls to `Set.contains`, `Set.insert` and `Set.remove` are all compiled as calls (`DELEGATECALL`) to an external contract/library. If you use libraries, be aware that an actual external function call is performed. `msg.sender`, `msg.value` and `this` will retain their values in this call, though (prior to Homestead, because of the use of `CALLCODE`, `msg.sender` and `msg.value` changed, though).

The following example shows how to use [types stored in memory](types.html#data-location) and internal functions in libraries in order to implement custom types without the overhead of external function calls:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguMDsKCnN0cnVjdCBiaWdpbnQgewogICAgdWludFtdIGxpbWJzOwp9CgpsaWJyYXJ5IEJpZ0ludCB7CiAgICBmdW5jdGlvbiBmcm9tVWludCh1aW50IHgpIGludGVybmFsIHB1cmUgcmV0dXJucyAoYmlnaW50IG1lbW9yeSByKSB7CiAgICAgICAgci5saW1icyA9IG5ldyB1aW50W10oMSk7CiAgICAgICAgci5saW1ic1swXSA9IHg7CiAgICB9CgogICAgZnVuY3Rpb24gYWRkKGJpZ2ludCBtZW1vcnkgYSwgYmlnaW50IG1lbW9yeSBiKSBpbnRlcm5hbCBwdXJlIHJldHVybnMgKGJpZ2ludCBtZW1vcnkgcikgewogICAgICAgIHIubGltYnMgPSBuZXcgdWludFtdKG1heChhLmxpbWJzLmxlbmd0aCwgYi5saW1icy5sZW5ndGgpKTsKICAgICAgICB1aW50IGNhcnJ5ID0gMDsKICAgICAgICBmb3IgKHVpbnQgaSA9IDA7IGkgPCByLmxpbWJzLmxlbmd0aDsgKytpKSB7CiAgICAgICAgICAgIHVpbnQgbGltYkEgPSBsaW1iKGEsIGkpOwogICAgICAgICAgICB1aW50IGxpbWJCID0gbGltYihiLCBpKTsKICAgICAgICAgICAgdW5jaGVja2VkIHsKICAgICAgICAgICAgICAgIHIubGltYnNbaV0gPSBsaW1iQSArIGxpbWJCICsgY2Fycnk7CgogICAgICAgICAgICAgICAgaWYgKGxpbWJBICsgbGltYkIgPCBsaW1iQSB8fCAobGltYkEgKyBsaW1iQiA9PSB0eXBlKHVpbnQpLm1heCAmJiBjYXJyeSA+IDApKQogICAgICAgICAgICAgICAgICAgIGNhcnJ5ID0gMTsKICAgICAgICAgICAgICAgIGVsc2UKICAgICAgICAgICAgICAgICAgICBjYXJyeSA9IDA7CiAgICAgICAgICAgIH0KICAgICAgICB9CiAgICAgICAgaWYgKGNhcnJ5ID4gMCkgewogICAgICAgICAgICAvLyB0b28gYmFkLCB3ZSBoYXZlIHRvIGFkZCBhIGxpbWIKICAgICAgICAgICAgdWludFtdIG1lbW9yeSBuZXdMaW1icyA9IG5ldyB1aW50W10oci5saW1icy5sZW5ndGggKyAxKTsKICAgICAgICAgICAgdWludCBpOwogICAgICAgICAgICBmb3IgKGkgPSAwOyBpIDwgci5saW1icy5sZW5ndGg7ICsraSkKICAgICAgICAgICAgICAgIG5ld0xpbWJzW2ldID0gci5saW1ic1tpXTsKICAgICAgICAgICAgbmV3TGltYnNbaV0gPSBjYXJyeTsKICAgICAgICAgICAgci5saW1icyA9IG5ld0xpbWJzOwogICAgICAgIH0KICAgIH0KCiAgICBmdW5jdGlvbiBsaW1iKGJpZ2ludCBtZW1vcnkgYSwgdWludCBpbmRleCkgaW50ZXJuYWwgcHVyZSByZXR1cm5zICh1aW50KSB7CiAgICAgICAgcmV0dXJuIGluZGV4IDwgYS5saW1icy5sZW5ndGggPyBhLmxpbWJzW2luZGV4XSA6IDA7CiAgICB9CgogICAgZnVuY3Rpb24gbWF4KHVpbnQgYSwgdWludCBiKSBwcml2YXRlIHB1cmUgcmV0dXJucyAodWludCkgewogICAgICAgIHJldHVybiBhID4gYiA/IGEgOiBiOwogICAgfQp9Cgpjb250cmFjdCBDIHsKICAgIHVzaW5nIEJpZ0ludCBmb3IgYmlnaW50OwoKICAgIGZ1bmN0aW9uIGYoKSBwdWJsaWMgcHVyZSB7CiAgICAgICAgYmlnaW50IG1lbW9yeSB4ID0gQmlnSW50LmZyb21VaW50KDcpOwogICAgICAgIGJpZ2ludCBtZW1vcnkgeSA9IEJpZ0ludC5mcm9tVWludCh0eXBlKHVpbnQpLm1heCk7CiAgICAgICAgYmlnaW50IG1lbW9yeSB6ID0geC5hZGQoeSk7CiAgICAgICAgYXNzZXJ0KHoubGltYigxKSA+IDApOwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.0;

struct bigint {
    uint[] limbs;
}

library BigInt {
    function fromUint(uint x) internal pure returns (bigint memory r) {
        r.limbs = new uint[](1);
        r.limbs[0] = x;
    }

    function add(bigint memory a, bigint memory b) internal pure returns (bigint memory r) {
        r.limbs = new uint[](max(a.limbs.length, b.limbs.length));
        uint carry = 0;
        for (uint i = 0; i < r.limbs.length; ++i) {
            uint limbA = limb(a, i);
            uint limbB = limb(b, i);
            unchecked {
                r.limbs[i] = limbA + limbB + carry;

                if (limbA + limbB < limbA || (limbA + limbB == type(uint).max && carry > 0))
                    carry = 1;
                else
                    carry = 0;
            }
        }
        if (carry > 0) {
            // too bad, we have to add a limb
            uint[] memory newLimbs = new uint[](r.limbs.length + 1);
            uint i;
            for (i = 0; i < r.limbs.length; ++i)
                newLimbs[i] = r.limbs[i];
            newLimbs[i] = carry;
            r.limbs = newLimbs;
        }
    }

    function limb(bigint memory a, uint index) internal pure returns (uint) {
        return index < a.limbs.length ? a.limbs[index] : 0;
    }

    function max(uint a, uint b) private pure returns (uint) {
        return a > b ? a : b;
    }
}

contract C {
    using BigInt for bigint;

    function f() public pure {
        bigint memory x = BigInt.fromUint(7);
        bigint memory y = BigInt.fromUint(type(uint).max);
        bigint memory z = x.add(y);
        assert(z.limb(1) > 0);
    }
}

It is possible to obtain the address of a library by converting the library type to the `address` type, i.e. using `address(LibraryName)`.

As the compiler does not know the address where the library will be deployed, the compiled hex code will contain placeholders of the form `__$30bbc0abd4d6364515865950d3e0d10953$__`. The placeholder is a 34 character prefix of the hex encoding of the keccak256 hash of the fully qualified library name, which would be for example `libraries/bigint.sol:BigInt` if the library was stored in a file called `bigint.sol` in a `libraries/` directory. Such bytecode is incomplete and should not be deployed. Placeholders need to be replaced with actual addresses. You can do that by either passing them to the compiler when the library is being compiled or by using the linker to update an already compiled binary. See [Library Linking](using-the-compiler.html#library-linking) for information on how to use the commandline compiler for linking.

In comparison to contracts, libraries are restricted in the following ways:

- they cannot have state variables
    
- they cannot inherit nor be inherited
    
- they cannot receive Ether
    
- they cannot be destroyed
    

(These might be lifted at a later point.)

### Function Signatures and Selectors in Libraries[](#function-signatures-and-selectors-in-libraries "Permalink to this heading")

While external calls to public or external library functions are possible, the calling convention for such calls is considered to be internal to Solidity and not the same as specified for the regular [contract ABI](abi-spec.html#abi). External library functions support more argument types than external contract functions, for example recursive structs and storage pointers. For that reason, the function signatures used to compute the 4-byte selector are computed following an internal naming schema and arguments of types not supported in the contract ABI use an internal encoding.

The following identifiers are used for the types in the signatures:

- Value types, non-storage `string` and non-storage `bytes` use the same identifiers as in the contract ABI.
    
- Non-storage array types follow the same convention as in the contract ABI, i.e. `<type>[]` for dynamic arrays and `<type>[M]` for fixed-size arrays of `M` elements.
    
- Non-storage structs are referred to by their fully qualified name, i.e. `C.S` for `contract C { struct S { ... } }`.
    
- Storage pointer mappings use `mapping(<keyType> => <valueType>) storage` where `<keyType>` and `<valueType>` are the identifiers for the key and value types of the mapping, respectively.
    
- Other storage pointer types use the type identifier of their corresponding non-storage type, but append a single space followed by `storage` to it.
    

The argument encoding is the same as for the regular contract ABI, except for storage pointers, which are encoded as a `uint256` value referring to the storage slot to which they point.

Similarly to the contract ABI, the selector consists of the first four bytes of the Keccak256-hash of the signature. Its value can be obtained from Solidity using the `.selector` member as follows:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC41LjE0IDwwLjkuMDsKCmxpYnJhcnkgTCB7CiAgICBmdW5jdGlvbiBmKHVpbnQyNTYpIGV4dGVybmFsIHt9Cn0KCmNvbnRyYWN0IEMgewogICAgZnVuY3Rpb24gZygpIHB1YmxpYyBwdXJlIHJldHVybnMgKGJ5dGVzNCkgewogICAgICAgIHJldHVybiBMLmYuc2VsZWN0b3I7CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.5.14 <0.9.0;

library L {
    function f(uint256) external {}
}

contract C {
    function g() public pure returns (bytes4) {
        return L.f.selector;
    }
}

### Call Protection For Libraries[](#call-protection-for-libraries "Permalink to this heading")

As mentioned in the introduction, if a library’s code is executed using a `CALL` instead of a `DELEGATECALL` or `CALLCODE`, it will revert unless a `view` or `pure` function is called.

The EVM does not provide a direct way for a contract to detect whether it was called using `CALL` or not, but a contract can use the `ADDRESS` opcode to find out “where” it is currently running. The generated code compares this address to the address used at construction time to determine the mode of calling.

More specifically, the runtime code of a library always starts with a push instruction, which is a zero of 20 bytes at compilation time. When the deploy code runs, this constant is replaced in memory by the current address and this modified code is stored in the contract. At runtime, this causes the deploy time address to be the first constant to be pushed onto the stack and the dispatcher code compares the current address against this constant for any non-view and non-pure function.

This means that the actual code stored on chain for a library is different from the code reported by the compiler as `deployedBytecode`.

## Using For[](#using-for "Permalink to this heading")

The directive `using A for B` can be used to attach functions (`A`) as operators to user-defined value types or as member functions to any type (`B`). The member functions receive the object they are called on as their first parameter (like the `self` variable in Python). The operator functions receive operands as parameters.

It is valid either at file level or inside a contract, at contract level.

The first part, `A`, can be one of:

- A list of functions, optionally with an operator name assigned (e.g. `using {f, g as +, h, L.t} for uint`). If no operator is specified, the function can be either a library function or a free function and is attached to the type as a member function. Otherwise it must be a free function and it becomes the definition of that operator on the type.
    
- The name of a library (e.g. `using L for uint`) - all non-private functions of the library are attached to the type as member functions
    

At file level, the second part, `B`, has to be an explicit type (without data location specifier). Inside contracts, you can also use `*` in place of the type (e.g. `using L for *;`), which has the effect that all functions of the library `L` are attached to _all_ types.

If you specify a library, _all_ non-private functions in the library get attached, even those where the type of the first parameter does not match the type of the object. The type is checked at the point the function is called and function overload resolution is performed.

If you use a list of functions (e.g. `using {f, g, h, L.t} for uint`), then the type (`uint`) has to be implicitly convertible to the first parameter of each of these functions. This check is performed even if none of these functions are called. Note that private library functions can only be specified when `using for` is inside a library.

If you define an operator (e.g. `using {f as +} for T`), then the type (`T`) must be a [user-defined value type](types.html#user-defined-value-types) and the definition must be a `pure` function. Operator definitions must be global. The following operators can be defined this way:

  
|Category|Operator|Possible signatures|
|---|---|---|
|Bitwise|`&`|`function (T, T) pure returns (T)`|
|`\|`|`function (T, T) pure returns (T)`|
|`^`|`function (T, T) pure returns (T)`|
|`~`|`function (T) pure returns (T)`|
|Arithmetic|`+`|`function (T, T) pure returns (T)`|
|`-`|`function (T, T) pure returns (T)`|
|`function (T) pure returns (T)`|
|`*`|`function (T, T) pure returns (T)`|
|`/`|`function (T, T) pure returns (T)`|
|`%`|`function (T, T) pure returns (T)`|
|Comparison|`==`|`function (T, T) pure returns (bool)`|
|`!=`|`function (T, T) pure returns (bool)`|
|`<`|`function (T, T) pure returns (bool)`|
|`<=`|`function (T, T) pure returns (bool)`|
|`>`|`function (T, T) pure returns (bool)`|
|`>=`|`function (T, T) pure returns (bool)`|

Note that unary and binary `-` need separate definitions. The compiler will choose the right definition based on how the operator is invoked.

The `using A for B;` directive is active only within the current scope (either the contract or the current module/source unit), including within all of its functions, and has no effect outside of the contract or module in which it is used.

When the directive is used at file level and applied to a user-defined type which was defined at file level in the same file, the word `global` can be added at the end. This will have the effect that the functions and operators are attached to the type everywhere the type is available (including other files), not only in the scope of the using statement.

Let us rewrite the set example from the [Libraries](#libraries) section in this way, using file-level functions instead of library functions.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguMTM7CgpzdHJ1Y3QgRGF0YSB7IG1hcHBpbmcodWludCA9PiBib29sKSBmbGFnczsgfQovLyBOb3cgd2UgYXR0YWNoIGZ1bmN0aW9ucyB0byB0aGUgdHlwZS4KLy8gVGhlIGF0dGFjaGVkIGZ1bmN0aW9ucyBjYW4gYmUgdXNlZCB0aHJvdWdob3V0IHRoZSByZXN0IG9mIHRoZSBtb2R1bGUuCi8vIElmIHlvdSBpbXBvcnQgdGhlIG1vZHVsZSwgeW91IGhhdmUgdG8KLy8gcmVwZWF0IHRoZSB1c2luZyBkaXJlY3RpdmUgdGhlcmUsIGZvciBleGFtcGxlIGFzCi8vICAgaW1wb3J0ICJmbGFncy5zb2wiIGFzIEZsYWdzOwovLyAgIHVzaW5nIHtGbGFncy5pbnNlcnQsIEZsYWdzLnJlbW92ZSwgRmxhZ3MuY29udGFpbnN9Ci8vICAgICBmb3IgRmxhZ3MuRGF0YTsKdXNpbmcge2luc2VydCwgcmVtb3ZlLCBjb250YWluc30gZm9yIERhdGE7CgpmdW5jdGlvbiBpbnNlcnQoRGF0YSBzdG9yYWdlIHNlbGYsIHVpbnQgdmFsdWUpCiAgICByZXR1cm5zIChib29sKQp7CiAgICBpZiAoc2VsZi5mbGFnc1t2YWx1ZV0pCiAgICAgICAgcmV0dXJuIGZhbHNlOyAvLyBhbHJlYWR5IHRoZXJlCiAgICBzZWxmLmZsYWdzW3ZhbHVlXSA9IHRydWU7CiAgICByZXR1cm4gdHJ1ZTsKfQoKZnVuY3Rpb24gcmVtb3ZlKERhdGEgc3RvcmFnZSBzZWxmLCB1aW50IHZhbHVlKQogICAgcmV0dXJucyAoYm9vbCkKewogICAgaWYgKCFzZWxmLmZsYWdzW3ZhbHVlXSkKICAgICAgICByZXR1cm4gZmFsc2U7IC8vIG5vdCB0aGVyZQogICAgc2VsZi5mbGFnc1t2YWx1ZV0gPSBmYWxzZTsKICAgIHJldHVybiB0cnVlOwp9CgpmdW5jdGlvbiBjb250YWlucyhEYXRhIHN0b3JhZ2Ugc2VsZiwgdWludCB2YWx1ZSkKICAgIHZpZXcKICAgIHJldHVybnMgKGJvb2wpCnsKICAgIHJldHVybiBzZWxmLmZsYWdzW3ZhbHVlXTsKfQoKCmNvbnRyYWN0IEMgewogICAgRGF0YSBrbm93blZhbHVlczsKCiAgICBmdW5jdGlvbiByZWdpc3Rlcih1aW50IHZhbHVlKSBwdWJsaWMgewogICAgICAgIC8vIEhlcmUsIGFsbCB2YXJpYWJsZXMgb2YgdHlwZSBEYXRhIGhhdmUKICAgICAgICAvLyBjb3JyZXNwb25kaW5nIG1lbWJlciBmdW5jdGlvbnMuCiAgICAgICAgLy8gVGhlIGZvbGxvd2luZyBmdW5jdGlvbiBjYWxsIGlzIGlkZW50aWNhbCB0bwogICAgICAgIC8vIGBTZXQuaW5zZXJ0KGtub3duVmFsdWVzLCB2YWx1ZSlgCiAgICAgICAgcmVxdWlyZShrbm93blZhbHVlcy5pbnNlcnQodmFsdWUpKTsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.13;

struct Data { mapping(uint => bool) flags; }
// Now we attach functions to the type.
// The attached functions can be used throughout the rest of the module.
// If you import the module, you have to
// repeat the using directive there, for example as
//   import "flags.sol" as Flags;
//   using {Flags.insert, Flags.remove, Flags.contains}
//     for Flags.Data;
using {insert, remove, contains} for Data;

function insert(Data storage self, uint value)
    returns (bool)
{
    if (self.flags[value])
        return false; // already there
    self.flags[value] = true;
    return true;
}

function remove(Data storage self, uint value)
    returns (bool)
{
    if (!self.flags[value])
        return false; // not there
    self.flags[value] = false;
    return true;
}

function contains(Data storage self, uint value)
    view
    returns (bool)
{
    return self.flags[value];
}

contract C {
    Data knownValues;

    function register(uint value) public {
        // Here, all variables of type Data have
        // corresponding member functions.
        // The following function call is identical to
        // `Set.insert(knownValues, value)`
        require(knownValues.insert(value));
    }
}

It is also possible to extend built-in types in that way. In this example, we will use a library.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguMTM7CgpsaWJyYXJ5IFNlYXJjaCB7CiAgICBmdW5jdGlvbiBpbmRleE9mKHVpbnRbXSBzdG9yYWdlIHNlbGYsIHVpbnQgdmFsdWUpCiAgICAgICAgcHVibGljCiAgICAgICAgdmlldwogICAgICAgIHJldHVybnMgKHVpbnQpCiAgICB7CiAgICAgICAgZm9yICh1aW50IGkgPSAwOyBpIDwgc2VsZi5sZW5ndGg7IGkrKykKICAgICAgICAgICAgaWYgKHNlbGZbaV0gPT0gdmFsdWUpIHJldHVybiBpOwogICAgICAgIHJldHVybiB0eXBlKHVpbnQpLm1heDsKICAgIH0KfQp1c2luZyBTZWFyY2ggZm9yIHVpbnRbXTsKCmNvbnRyYWN0IEMgewogICAgdWludFtdIGRhdGE7CgogICAgZnVuY3Rpb24gYXBwZW5kKHVpbnQgdmFsdWUpIHB1YmxpYyB7CiAgICAgICAgZGF0YS5wdXNoKHZhbHVlKTsKICAgIH0KCiAgICBmdW5jdGlvbiByZXBsYWNlKHVpbnQgZnJvbSwgdWludCB0bykgcHVibGljIHsKICAgICAgICAvLyBUaGlzIHBlcmZvcm1zIHRoZSBsaWJyYXJ5IGZ1bmN0aW9uIGNhbGwKICAgICAgICB1aW50IGluZGV4ID0gZGF0YS5pbmRleE9mKGZyb20pOwogICAgICAgIGlmIChpbmRleCA9PSB0eXBlKHVpbnQpLm1heCkKICAgICAgICAgICAgZGF0YS5wdXNoKHRvKTsKICAgICAgICBlbHNlCiAgICAgICAgICAgIGRhdGFbaW5kZXhdID0gdG87CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.13;

library Search {
    function indexOf(uint[] storage self, uint value)
        public
        view
        returns (uint)
    {
        for (uint i = 0; i < self.length; i++)
            if (self[i] == value) return i;
        return type(uint).max;
    }
}
using Search for uint[];

contract C {
    uint[] data;

    function append(uint value) public {
        data.push(value);
    }

    function replace(uint from, uint to) public {
        // This performs the library function call
        uint index = data.indexOf(from);
        if (index == type(uint).max)
            data.push(to);
        else
            data[index] = to;
    }
}

Note that all external library calls are actual EVM function calls. This means that if you pass memory or value types, a copy will be performed, even in case of the `self` variable. The only situation where no copy will be performed is when storage reference variables are used or when internal library functions are called.

Another example shows how to define a custom operator for a user-defined type:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguMTk7Cgp0eXBlIFVGaXhlZDE2eDIgaXMgdWludDE2OwoKdXNpbmcgewogICAgYWRkIGFzICssCiAgICBkaXYgYXMgLwp9IGZvciBVRml4ZWQxNngyIGdsb2JhbDsKCnVpbnQzMiBjb25zdGFudCBTQ0FMRSA9IDEwMDsKCmZ1bmN0aW9uIGFkZChVRml4ZWQxNngyIGEsIFVGaXhlZDE2eDIgYikgcHVyZSByZXR1cm5zIChVRml4ZWQxNngyKSB7CiAgICByZXR1cm4gVUZpeGVkMTZ4Mi53cmFwKFVGaXhlZDE2eDIudW53cmFwKGEpICsgVUZpeGVkMTZ4Mi51bndyYXAoYikpOwp9CgpmdW5jdGlvbiBkaXYoVUZpeGVkMTZ4MiBhLCBVRml4ZWQxNngyIGIpIHB1cmUgcmV0dXJucyAoVUZpeGVkMTZ4MikgewogICAgdWludDMyIGEzMiA9IFVGaXhlZDE2eDIudW53cmFwKGEpOwogICAgdWludDMyIGIzMiA9IFVGaXhlZDE2eDIudW53cmFwKGIpOwogICAgdWludDMyIHJlc3VsdDMyID0gYTMyICogU0NBTEUgLyBiMzI7CiAgICByZXF1aXJlKHJlc3VsdDMyIDw9IHR5cGUodWludDE2KS5tYXgsICJEaXZpZGUgb3ZlcmZsb3ciKTsKICAgIHJldHVybiBVRml4ZWQxNngyLndyYXAodWludDE2KGEzMiAqIFNDQUxFIC8gYjMyKSk7Cn0KCmNvbnRyYWN0IE1hdGggewogICAgZnVuY3Rpb24gYXZnKFVGaXhlZDE2eDIgYSwgVUZpeGVkMTZ4MiBiKSBwdWJsaWMgcHVyZSByZXR1cm5zIChVRml4ZWQxNngyKSB7CiAgICAgICAgcmV0dXJuIChhICsgYikgLyBVRml4ZWQxNngyLndyYXAoMjAwKTsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.19;

type UFixed16x2 is uint16;

using {
    add as +,
    div as /
} for UFixed16x2 global;

uint32 constant SCALE = 100;

function add(UFixed16x2 a, UFixed16x2 b) pure returns (UFixed16x2) {
    return UFixed16x2.wrap(UFixed16x2.unwrap(a) + UFixed16x2.unwrap(b));
}

function div(UFixed16x2 a, UFixed16x2 b) pure returns (UFixed16x2) {
    uint32 a32 = UFixed16x2.unwrap(a);
    uint32 b32 = UFixed16x2.unwrap(b);
    uint32 result32 = a32 * SCALE / b32;
    require(result32 <= type(uint16).max, "Divide overflow");
    return UFixed16x2.wrap(uint16(a32 * SCALE / b32));
}

contract Math {
    function avg(UFixed16x2 a, UFixed16x2 b) public pure returns (UFixed16x2) {
        return (a + b) / UFixed16x2.wrap(200);
    }
}

[Previous](control-structures.html "Expressions and Control Structures") [Next](assembly.html "Inline Assembly")

---

© Copyright 2016-2023, The Solidity Authors. Revision `1acebf78`.

Customized with ❤️ by the [ethereum.org](https://ethereum.org/) team.

[Credits and attribution](credits-and-attribution.html).