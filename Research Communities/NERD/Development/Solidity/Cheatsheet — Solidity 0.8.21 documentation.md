[![Solidity logo](https://docs.soliditylang.org/en/v0.8.21/cheatsheet.html_static/img/logo.svg)](https://soliditylang.org)[{ skip to content }](#content)

[Blog](https://soliditylang.org/blog)[Documentation](/)[Use cases](https://soliditylang.org/use-cases)[Contribute](/en/latest/contributing.html)[About](https://soliditylang.org/about)[Forum](https://forum.soliditylang.org/)

![Color mode toggle icon](https://docs.soliditylang.org/en/v0.8.21/cheatsheet.html_static/img/moon.svg)![Toggle menu](https://docs.soliditylang.org/en/v0.8.21/cheatsheet.html_static/img/hamburger-light.svg)

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
- [Contracts](contracts.html)
- [Inline Assembly](assembly.html)
- [Cheatsheet](#)
    - [Order of Precedence of Operators](#order-of-precedence-of-operators)
    - [ABI Encoding and Decoding Functions](#abi-encoding-and-decoding-functions)
    - [Members of `bytes` and `string`](#members-of-bytes-and-string)
    - [Members of `address`](#members-of-address)
    - [Block and Transaction Properties](#block-and-transaction-properties)
    - [Validations and Assertions](#validations-and-assertions)
    - [Mathematical and Cryptographic Functions](#mathematical-and-cryptographic-functions)
    - [Contract-related](#contract-related)
    - [Type Information](#type-information)
    - [Function Visibility Specifiers](#function-visibility-specifiers)
    - [Modifiers](#modifiers)
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

[en](https://docs.soliditylang.org/en/v0.8.21/cheatsheet.html)

[zh](https://docs.soliditylang.org/zh/v0.8.19/cheatsheet.html)

[fr](https://docs.soliditylang.org/fr/latest/cheatsheet.html)

[tr](https://docs.soliditylang.org/tr/v0.8.16/cheatsheet.html)

Versions

[latest](https://docs.soliditylang.org/en/latest/cheatsheet.html)

[stable](https://docs.soliditylang.org/en/stable/cheatsheet.html)

[v0.8.21](https://docs.soliditylang.org/en/v0.8.21/cheatsheet.html)

[v0.8.20](https://docs.soliditylang.org/en/v0.8.20/cheatsheet.html)

[v0.8.19](https://docs.soliditylang.org/en/v0.8.19/cheatsheet.html)

[v0.8.18](https://docs.soliditylang.org/en/v0.8.18/cheatsheet.html)

[v0.8.17](https://docs.soliditylang.org/en/v0.8.17/cheatsheet.html)

[v0.8.16](https://docs.soliditylang.org/en/v0.8.16/cheatsheet.html)

[v0.8.15](https://docs.soliditylang.org/en/v0.8.15/cheatsheet.html)

[v0.8.14](https://docs.soliditylang.org/en/v0.8.14/cheatsheet.html)

[v0.8.13](https://docs.soliditylang.org/en/v0.8.13/cheatsheet.html)

[v0.8.12](https://docs.soliditylang.org/en/v0.8.12/cheatsheet.html)

[v0.8.11](https://docs.soliditylang.org/en/v0.8.11/cheatsheet.html)

[v0.8.10](https://docs.soliditylang.org/en/v0.8.10/cheatsheet.html)

[v0.8.9](https://docs.soliditylang.org/en/v0.8.9/cheatsheet.html)

[v0.8.8](https://docs.soliditylang.org/en/v0.8.8/cheatsheet.html)

[v0.8.7](https://docs.soliditylang.org/en/v0.8.7/cheatsheet.html)

[v0.8.6](https://docs.soliditylang.org/en/v0.8.6/cheatsheet.html)

[v0.8.5](https://docs.soliditylang.org/en/v0.8.5/cheatsheet.html)

[v0.8.4](https://docs.soliditylang.org/en/v0.8.4/cheatsheet.html)

[v0.8.3](https://docs.soliditylang.org/en/v0.8.3/cheatsheet.html)

[v0.8.2](https://docs.soliditylang.org/en/v0.8.2/cheatsheet.html)

[v0.8.1](https://docs.soliditylang.org/en/v0.8.1/cheatsheet.html)

[v0.8.0](https://docs.soliditylang.org/en/v0.8.0/cheatsheet.html)

[v0.7.6](https://docs.soliditylang.org/en/v0.7.6/cheatsheet.html)

[v0.7.5](https://docs.soliditylang.org/en/v0.7.5/cheatsheet.html)

[v0.7.4](https://docs.soliditylang.org/en/v0.7.4/cheatsheet.html)

[v0.7.3](https://docs.soliditylang.org/en/v0.7.3/cheatsheet.html)

[v0.7.2](https://docs.soliditylang.org/en/v0.7.2/cheatsheet.html)

[v0.7.1](https://docs.soliditylang.org/en/v0.7.1/cheatsheet.html)

[v0.7.0](https://docs.soliditylang.org/en/v0.7.0/cheatsheet.html)

[v0.6.12](https://docs.soliditylang.org/en/v0.6.12/cheatsheet.html)

[v0.6.11](https://docs.soliditylang.org/en/v0.6.11/cheatsheet.html)

[v0.6.10](https://docs.soliditylang.org/en/v0.6.10/cheatsheet.html)

[v0.6.9](https://docs.soliditylang.org/en/v0.6.9/cheatsheet.html)

[v0.6.8](https://docs.soliditylang.org/en/v0.6.8/cheatsheet.html)

[v0.6.7](https://docs.soliditylang.org/en/v0.6.7/cheatsheet.html)

[v0.6.6](https://docs.soliditylang.org/en/v0.6.6/cheatsheet.html)

[v0.6.5](https://docs.soliditylang.org/en/v0.6.5/cheatsheet.html)

[v0.6.4](https://docs.soliditylang.org/en/v0.6.4/cheatsheet.html)

[v0.6.3](https://docs.soliditylang.org/en/v0.6.3/cheatsheet.html)

[v0.6.2](https://docs.soliditylang.org/en/v0.6.2/cheatsheet.html)

[v0.6.1](https://docs.soliditylang.org/en/v0.6.1/cheatsheet.html)

[v0.6.0](https://docs.soliditylang.org/en/v0.6.0/cheatsheet.html)

[v0.5.17](https://docs.soliditylang.org/en/v0.5.17/cheatsheet.html)

[v0.5.16](https://docs.soliditylang.org/en/v0.5.16/cheatsheet.html)

[v0.5.15](https://docs.soliditylang.org/en/v0.5.15/cheatsheet.html)

[v0.5.14](https://docs.soliditylang.org/en/v0.5.14/cheatsheet.html)

[v0.5.13](https://docs.soliditylang.org/en/v0.5.13/cheatsheet.html)

[v0.5.12](https://docs.soliditylang.org/en/v0.5.12/cheatsheet.html)

[v0.5.11](https://docs.soliditylang.org/en/v0.5.11/cheatsheet.html)

[v0.5.10](https://docs.soliditylang.org/en/v0.5.10/cheatsheet.html)

[v0.5.9](https://docs.soliditylang.org/en/v0.5.9/cheatsheet.html)

[v0.5.8](https://docs.soliditylang.org/en/v0.5.8/cheatsheet.html)

[v0.5.7](https://docs.soliditylang.org/en/v0.5.7/cheatsheet.html)

[v0.5.6](https://docs.soliditylang.org/en/v0.5.6/cheatsheet.html)

[v0.5.5](https://docs.soliditylang.org/en/v0.5.5/cheatsheet.html)

[v0.5.4](https://docs.soliditylang.org/en/v0.5.4/cheatsheet.html)

[v0.5.3](https://docs.soliditylang.org/en/v0.5.3/cheatsheet.html)

[v0.5.2](https://docs.soliditylang.org/en/v0.5.2/cheatsheet.html)

[v0.5.1](https://docs.soliditylang.org/en/v0.5.1/cheatsheet.html)

[v0.5.0](https://docs.soliditylang.org/en/v0.5.0/cheatsheet.html)

[v0.4.26](https://docs.soliditylang.org/en/v0.4.26/cheatsheet.html)

[v0.4.25](https://docs.soliditylang.org/en/v0.4.25/cheatsheet.html)

[v0.4.24](https://docs.soliditylang.org/en/v0.4.24/cheatsheet.html)

[v0.4.23](https://docs.soliditylang.org/en/v0.4.23/cheatsheet.html)

[v0.4.22](https://docs.soliditylang.org/en/v0.4.22/cheatsheet.html)

[v0.4.21](https://docs.soliditylang.org/en/v0.4.21/cheatsheet.html)

[v0.4.20](https://docs.soliditylang.org/en/v0.4.20/cheatsheet.html)

[v0.4.19](https://docs.soliditylang.org/en/v0.4.19/cheatsheet.html)

[v0.4.18](https://docs.soliditylang.org/en/v0.4.18/cheatsheet.html)

[v0.4.17](https://docs.soliditylang.org/en/v0.4.17/cheatsheet.html)

[v0.4.16](https://docs.soliditylang.org/en/v0.4.16/cheatsheet.html)

[v0.4.15](https://docs.soliditylang.org/en/v0.4.15/cheatsheet.html)

[v0.4.14](https://docs.soliditylang.org/en/v0.4.14/cheatsheet.html)

[v0.4.13](https://docs.soliditylang.org/en/v0.4.13/cheatsheet.html)

[v0.4.12](https://docs.soliditylang.org/en/v0.4.12/cheatsheet.html)

[v0.4.11](https://docs.soliditylang.org/en/v0.4.11/cheatsheet.html)

[v0.4.10](https://docs.soliditylang.org/en/v0.4.10/cheatsheet.html)

[v0.4.9](https://docs.soliditylang.org/en/v0.4.9/cheatsheet.html)

[v0.4.8](https://docs.soliditylang.org/en/v0.4.8/cheatsheet.html)

[v0.4.7](https://docs.soliditylang.org/en/v0.4.7/cheatsheet.html)

[v0.4.6](https://docs.soliditylang.org/en/v0.4.6/cheatsheet.html)

[v0.4.5](https://docs.soliditylang.org/en/v0.4.5/cheatsheet.html)

[v0.4.4](https://docs.soliditylang.org/en/v0.4.4/cheatsheet.html)

[v0.4.3](https://docs.soliditylang.org/en/v0.4.3/cheatsheet.html)

[v0.4.2](https://docs.soliditylang.org/en/v0.4.2/cheatsheet.html)

[v0.4.1](https://docs.soliditylang.org/en/v0.4.1/cheatsheet.html)

[v0.4.0](https://docs.soliditylang.org/en/v0.4.0/cheatsheet.html)

[v0.3.6](https://docs.soliditylang.org/en/v0.3.6/cheatsheet.html)

[v0.3.5](https://docs.soliditylang.org/en/v0.3.5/cheatsheet.html)

[v0.3.4](https://docs.soliditylang.org/en/v0.3.4/cheatsheet.html)

[v0.3.3](https://docs.soliditylang.org/en/v0.3.3/cheatsheet.html)

[v0.3.2](https://docs.soliditylang.org/en/v0.3.2/cheatsheet.html)

[v0.3.1](https://docs.soliditylang.org/en/v0.3.1/cheatsheet.html)

[v0.3.0](https://docs.soliditylang.org/en/v0.3.0/cheatsheet.html)

[v0.2.2](https://docs.soliditylang.org/en/v0.2.2/cheatsheet.html)

[v0.2.1](https://docs.soliditylang.org/en/v0.2.1/cheatsheet.html)

[v0.2.0](https://docs.soliditylang.org/en/v0.2.0/cheatsheet.html)

[v0.1.7](https://docs.soliditylang.org/en/v0.1.7/cheatsheet.html)

[v0.1.6](https://docs.soliditylang.org/en/v0.1.6/cheatsheet.html)

[v0.1.5](https://docs.soliditylang.org/en/v0.1.5/cheatsheet.html)

[v0.1.4](https://docs.soliditylang.org/en/v0.1.4/cheatsheet.html)

[v0.1.3](https://docs.soliditylang.org/en/v0.1.3/cheatsheet.html)

[v0.1.2](https://docs.soliditylang.org/en/v0.1.2/cheatsheet.html)

[develop](https://docs.soliditylang.org/en/develop/cheatsheet.html)

[breaking](https://docs.soliditylang.org/en/breaking/cheatsheet.html)

Downloads

[PDF](//docs.soliditylang.org/_/downloads/en/v0.8.21/pdf/)

[Epub](//docs.soliditylang.org/_/downloads/en/v0.8.21/epub/)

On Read the Docs

[Project Home](//readthedocs.org/projects/solidity/)

[Builds](//readthedocs.org/projects/solidity/builds/)

[Downloads](//readthedocs.org/projects/solidity/downloads/)

On GitHub

[View](https://github.com/ethereum/solidity/blob/v0.8.21/docs/cheatsheet.rst)

Search

---

Hosted by [Read the Docs](https://readthedocs.org) · [Privacy Policy](https://docs.readthedocs.io/page/privacy-policy.html)

- [](index.html)
- Cheatsheet
- [Edit on GitHub](https://github.com/ethereum/solidity/blob/v0.8.21/docs/cheatsheet.rst)

---

# Cheatsheet[](#cheatsheet "Permalink to this heading")

## Order of Precedence of Operators[](#order-of-precedence-of-operators "Permalink to this heading")

The following is the order of precedence for operators, listed in order of evaluation.

  
|Precedence|Description|Operator|
|---|---|---|
|_1_|Postfix increment and decrement|`++`, `--`|
|New expression|`new <typename>`|
|Array subscripting|`<array>[<index>]`|
|Member access|`<object>.<member>`|
|Function-like call|`<func>(<args...>)`|
|Parentheses|`(<statement>)`|
|_2_|Prefix increment and decrement|`++`, `--`|
|Unary minus|`-`|
|Unary operations|`delete`|
|Logical NOT|`!`|
|Bitwise NOT|`~`|
|_3_|Exponentiation|`**`|
|_4_|Multiplication, division and modulo|`*`, `/`, `%`|
|_5_|Addition and subtraction|`+`, `-`|
|_6_|Bitwise shift operators|`<<`, `>>`|
|_7_|Bitwise AND|`&`|
|_8_|Bitwise XOR|`^`|
|_9_|Bitwise OR|`\|`|
|_10_|Inequality operators|`<`, `>`, `<=`, `>=`|
|_11_|Equality operators|`==`, `!=`|
|_12_|Logical AND|`&&`|
|_13_|Logical OR|`\|`|
|_14_|Ternary operator|`<conditional> ? <if-true> : <if-false>`|
|Assignment operators|`=`, `\|=`, `^=`, `&=`, `<<=`, `>>=`, `+=`, `-=`, `*=`, `/=`, `%=`|
|_15_|Comma operator|`,`|

## ABI Encoding and Decoding Functions[](#abi-encoding-and-decoding-functions "Permalink to this heading")

- `abi.decode(bytes memory encodedData, (...)) returns (...)`: [ABI](abi-spec.html#abi)-decodes the provided data. The types are given in parentheses as second argument. Example: `(uint a, uint[2] memory b, bytes memory c) = abi.decode(data, (uint, uint[2], bytes))`
    
- `abi.encode(...) returns (bytes memory)`: [ABI](abi-spec.html#abi)-encodes the given arguments
    
- `abi.encodePacked(...) returns (bytes memory)`: Performs [packed encoding](abi-spec.html#abi-packed-mode) of the given arguments. Note that this encoding can be ambiguous!
    
- `abi.encodeWithSelector(bytes4 selector, ...) returns (bytes memory)`: [ABI](abi-spec.html#abi)-encodes the given arguments starting from the second and prepends the given four-byte selector
    
- `abi.encodeCall(function functionPointer, (...)) returns (bytes memory)`: ABI-encodes a call to `functionPointer` with the arguments found in the tuple. Performs a full type-check, ensuring the types match the function signature. Result equals `abi.encodeWithSelector(functionPointer.selector, (...))`
    
- `abi.encodeWithSignature(string memory signature, ...) returns (bytes memory)`: Equivalent to `abi.encodeWithSelector(bytes4(keccak256(bytes(signature))), ...)`
    

## Members of `bytes` and `string`[](#members-of-bytes-and-string "Permalink to this heading")

- `bytes.concat(...) returns (bytes memory)`: [Concatenates variable number of arguments to one byte array](types.html#bytes-concat)
    
- `string.concat(...) returns (string memory)`: [Concatenates variable number of arguments to one string array](types.html#string-concat)
    

## Members of `address`[](#members-of-address "Permalink to this heading")

- `<address>.balance` (`uint256`): balance of the [Address](types.html#address) in Wei
    
- `<address>.code` (`bytes memory`): code at the [Address](types.html#address) (can be empty)
    
- `<address>.codehash` (`bytes32`): the codehash of the [Address](types.html#address)
    
- `<address payable>.send(uint256 amount) returns (bool)`: send given amount of Wei to [Address](types.html#address), returns `false` on failure
    
- `<address payable>.transfer(uint256 amount)`: send given amount of Wei to [Address](types.html#address), throws on failure
    

## Block and Transaction Properties[](#block-and-transaction-properties "Permalink to this heading")

- `blockhash(uint blockNumber) returns (bytes32)`: hash of the given block - only works for 256 most recent blocks
    
- `block.basefee` (`uint`): current block’s base fee ([EIP-3198](https://eips.ethereum.org/EIPS/eip-3198) and [EIP-1559](https://eips.ethereum.org/EIPS/eip-1559))
    
- `block.chainid` (`uint`): current chain id
    
- `block.coinbase` (`address payable`): current block miner’s address
    
- `block.difficulty` (`uint`): current block difficulty (`EVM < Paris`). For other EVM versions it behaves as a deprecated alias for `block.prevrandao` that will be removed in the next breaking release
    
- `block.gaslimit` (`uint`): current block gaslimit
    
- `block.number` (`uint`): current block number
    
- `block.prevrandao` (`uint`): random number provided by the beacon chain (`EVM >= Paris`) (see [EIP-4399](https://eips.ethereum.org/EIPS/eip-4399) )
    
- `block.timestamp` (`uint`): current block timestamp in seconds since Unix epoch
    
- `gasleft() returns (uint256)`: remaining gas
    
- `msg.data` (`bytes`): complete calldata
    
- `msg.sender` (`address`): sender of the message (current call)
    
- `msg.sig` (`bytes4`): first four bytes of the calldata (i.e. function identifier)
    
- `msg.value` (`uint`): number of wei sent with the message
    
- `tx.gasprice` (`uint`): gas price of the transaction
    
- `tx.origin` (`address`): sender of the transaction (full call chain)
    

## Validations and Assertions[](#validations-and-assertions "Permalink to this heading")

- `assert(bool condition)`: abort execution and revert state changes if condition is `false` (use for internal error)
    
- `require(bool condition)`: abort execution and revert state changes if condition is `false` (use for malformed input or error in external component)
    
- `require(bool condition, string memory message)`: abort execution and revert state changes if condition is `false` (use for malformed input or error in external component). Also provide error message.
    
- `revert()`: abort execution and revert state changes
    
- `revert(string memory message)`: abort execution and revert state changes providing an explanatory string
    

## Mathematical and Cryptographic Functions[](#mathematical-and-cryptographic-functions "Permalink to this heading")

- `keccak256(bytes memory) returns (bytes32)`: compute the Keccak-256 hash of the input
    
- `sha256(bytes memory) returns (bytes32)`: compute the SHA-256 hash of the input
    
- `ripemd160(bytes memory) returns (bytes20)`: compute the RIPEMD-160 hash of the input
    
- `ecrecover(bytes32 hash, uint8 v, bytes32 r, bytes32 s) returns (address)`: recover address associated with the public key from elliptic curve signature, return zero on error
    
- `addmod(uint x, uint y, uint k) returns (uint)`: compute `(x + y) % k` where the addition is performed with arbitrary precision and does not wrap around at `2**256`. Assert that `k != 0` starting from version 0.5.0.
    
- `mulmod(uint x, uint y, uint k) returns (uint)`: compute `(x * y) % k` where the multiplication is performed with arbitrary precision and does not wrap around at `2**256`. Assert that `k != 0` starting from version 0.5.0.
    

## Contract-related[](#contract-related "Permalink to this heading")

- `this` (current contract’s type): the current contract, explicitly convertible to `address` or `address payable`
    
- `super`: a contract one level higher in the inheritance hierarchy
    
- `selfdestruct(address payable recipient)`: destroy the current contract, sending its funds to the given address
    

## Type Information[](#type-information "Permalink to this heading")

- `type(C).name` (`string`): the name of the contract
    
- `type(C).creationCode` (`bytes memory`): creation bytecode of the given contract, see [Type Information](units-and-global-variables.html#meta-type).
    
- `type(C).runtimeCode` (`bytes memory`): runtime bytecode of the given contract, see [Type Information](units-and-global-variables.html#meta-type).
    
- `type(I).interfaceId` (`bytes4`): value containing the EIP-165 interface identifier of the given interface, see [Type Information](units-and-global-variables.html#meta-type).
    
- `type(T).min` (`T`): the minimum value representable by the integer type `T`, see [Type Information](units-and-global-variables.html#meta-type).
    
- `type(T).max` (`T`): the maximum value representable by the integer type `T`, see [Type Information](units-and-global-variables.html#meta-type).
    

## Function Visibility Specifiers[](#function-visibility-specifiers "Permalink to this heading")

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=ZnVuY3Rpb24gbXlGdW5jdGlvbigpIDx2aXNpYmlsaXR5IHNwZWNpZmllcj4gcmV0dXJucyAoYm9vbCkgewogICAgcmV0dXJuIHRydWU7Cn0=)

function myFunction() <visibility specifier> returns (bool) {
    return true;
}

- `public`: visible externally and internally (creates a [getter function](contracts.html#getter-functions) for storage/state variables)
    
- `private`: only visible in the current contract
    
- `external`: only visible externally (only for functions) - i.e. can only be message-called (via `this.func`)
    
- `internal`: only visible internally
    

## Modifiers[](#modifiers "Permalink to this heading")

- `pure` for functions: Disallows modification or access of state.
    
- `view` for functions: Disallows modification of state.
    
- `payable` for functions: Allows them to receive Ether together with a call.
    
- `constant` for state variables: Disallows assignment (except initialisation), does not occupy storage slot.
    
- `immutable` for state variables: Allows assignment at construction time and is constant when deployed. Is stored in code.
    
- `anonymous` for events: Does not store event signature as topic.
    
- `indexed` for event parameters: Stores the parameter as topic.
    
- `virtual` for functions and modifiers: Allows the function’s or modifier’s behavior to be changed in derived contracts.
    
- `override`: States that this function, modifier or public state variable changes the behavior of a function or modifier in a base contract.
    

[Previous](assembly.html "Inline Assembly") [Next](grammar.html "Language Grammar")

---

© Copyright 2016-2023, The Solidity Authors. Revision `1acebf78`.

Customized with ❤️ by the [ethereum.org](https://ethereum.org/) team.

[Credits and attribution](credits-and-attribution.html).