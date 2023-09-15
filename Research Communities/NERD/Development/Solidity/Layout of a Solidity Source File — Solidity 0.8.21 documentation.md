[![Solidity logo](https://docs.soliditylang.org/en/v0.8.21/layout-of-source-files.html_static/img/logo.svg)](https://soliditylang.org)[{ skip to content }](#content)

[Blog](https://soliditylang.org/blog)[Documentation](/)[Use cases](https://soliditylang.org/use-cases)[Contribute](/en/latest/contributing.html)[About](https://soliditylang.org/about)[Forum](https://forum.soliditylang.org/)

![Color mode toggle icon](https://docs.soliditylang.org/en/v0.8.21/layout-of-source-files.html_static/img/moon.svg)![Toggle menu](https://docs.soliditylang.org/en/v0.8.21/layout-of-source-files.html_static/img/hamburger-light.svg)

v0.8.21

  

Basics

- [Introduction to Smart Contracts](introduction-to-smart-contracts.html)
- [Solidity by Example](solidity-by-example.html)
- [Installing the Solidity Compiler](installing-solidity.html)

Language Description

- [Layout of a Solidity Source File](#)
    - [SPDX License Identifier](#spdx-license-identifier)
    - [Pragmas](#pragmas)
        - [Version Pragma](#version-pragma)
        - [ABI Coder Pragma](#abi-coder-pragma)
        - [Experimental Pragma](#experimental-pragma)
            - [ABIEncoderV2](#abiencoderv2)
            - [SMTChecker](#smtchecker)
    - [Importing other Source Files](#importing-other-source-files)
        - [Syntax and Semantics](#syntax-and-semantics)
        - [Import Paths](#import-paths)
    - [Comments](#comments)
- [Structure of a Contract](structure-of-a-contract.html)
- [Types](types.html)
- [Units and Globally Available Variables](units-and-global-variables.html)
- [Expressions and Control Structures](control-structures.html)
- [Contracts](contracts.html)
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

[en](https://docs.soliditylang.org/en/v0.8.21/layout-of-source-files.html)

[zh](https://docs.soliditylang.org/zh/v0.8.19/layout-of-source-files.html)

[fr](https://docs.soliditylang.org/fr/latest/layout-of-source-files.html)

[tr](https://docs.soliditylang.org/tr/v0.8.16/layout-of-source-files.html)

Versions

[latest](https://docs.soliditylang.org/en/latest/layout-of-source-files.html)

[stable](https://docs.soliditylang.org/en/stable/layout-of-source-files.html)

[v0.8.21](https://docs.soliditylang.org/en/v0.8.21/layout-of-source-files.html)

[v0.8.20](https://docs.soliditylang.org/en/v0.8.20/layout-of-source-files.html)

[v0.8.19](https://docs.soliditylang.org/en/v0.8.19/layout-of-source-files.html)

[v0.8.18](https://docs.soliditylang.org/en/v0.8.18/layout-of-source-files.html)

[v0.8.17](https://docs.soliditylang.org/en/v0.8.17/layout-of-source-files.html)

[v0.8.16](https://docs.soliditylang.org/en/v0.8.16/layout-of-source-files.html)

[v0.8.15](https://docs.soliditylang.org/en/v0.8.15/layout-of-source-files.html)

[v0.8.14](https://docs.soliditylang.org/en/v0.8.14/layout-of-source-files.html)

[v0.8.13](https://docs.soliditylang.org/en/v0.8.13/layout-of-source-files.html)

[v0.8.12](https://docs.soliditylang.org/en/v0.8.12/layout-of-source-files.html)

[v0.8.11](https://docs.soliditylang.org/en/v0.8.11/layout-of-source-files.html)

[v0.8.10](https://docs.soliditylang.org/en/v0.8.10/layout-of-source-files.html)

[v0.8.9](https://docs.soliditylang.org/en/v0.8.9/layout-of-source-files.html)

[v0.8.8](https://docs.soliditylang.org/en/v0.8.8/layout-of-source-files.html)

[v0.8.7](https://docs.soliditylang.org/en/v0.8.7/layout-of-source-files.html)

[v0.8.6](https://docs.soliditylang.org/en/v0.8.6/layout-of-source-files.html)

[v0.8.5](https://docs.soliditylang.org/en/v0.8.5/layout-of-source-files.html)

[v0.8.4](https://docs.soliditylang.org/en/v0.8.4/layout-of-source-files.html)

[v0.8.3](https://docs.soliditylang.org/en/v0.8.3/layout-of-source-files.html)

[v0.8.2](https://docs.soliditylang.org/en/v0.8.2/layout-of-source-files.html)

[v0.8.1](https://docs.soliditylang.org/en/v0.8.1/layout-of-source-files.html)

[v0.8.0](https://docs.soliditylang.org/en/v0.8.0/layout-of-source-files.html)

[v0.7.6](https://docs.soliditylang.org/en/v0.7.6/layout-of-source-files.html)

[v0.7.5](https://docs.soliditylang.org/en/v0.7.5/layout-of-source-files.html)

[v0.7.4](https://docs.soliditylang.org/en/v0.7.4/layout-of-source-files.html)

[v0.7.3](https://docs.soliditylang.org/en/v0.7.3/layout-of-source-files.html)

[v0.7.2](https://docs.soliditylang.org/en/v0.7.2/layout-of-source-files.html)

[v0.7.1](https://docs.soliditylang.org/en/v0.7.1/layout-of-source-files.html)

[v0.7.0](https://docs.soliditylang.org/en/v0.7.0/layout-of-source-files.html)

[v0.6.12](https://docs.soliditylang.org/en/v0.6.12/layout-of-source-files.html)

[v0.6.11](https://docs.soliditylang.org/en/v0.6.11/layout-of-source-files.html)

[v0.6.10](https://docs.soliditylang.org/en/v0.6.10/layout-of-source-files.html)

[v0.6.9](https://docs.soliditylang.org/en/v0.6.9/layout-of-source-files.html)

[v0.6.8](https://docs.soliditylang.org/en/v0.6.8/layout-of-source-files.html)

[v0.6.7](https://docs.soliditylang.org/en/v0.6.7/layout-of-source-files.html)

[v0.6.6](https://docs.soliditylang.org/en/v0.6.6/layout-of-source-files.html)

[v0.6.5](https://docs.soliditylang.org/en/v0.6.5/layout-of-source-files.html)

[v0.6.4](https://docs.soliditylang.org/en/v0.6.4/layout-of-source-files.html)

[v0.6.3](https://docs.soliditylang.org/en/v0.6.3/layout-of-source-files.html)

[v0.6.2](https://docs.soliditylang.org/en/v0.6.2/layout-of-source-files.html)

[v0.6.1](https://docs.soliditylang.org/en/v0.6.1/layout-of-source-files.html)

[v0.6.0](https://docs.soliditylang.org/en/v0.6.0/layout-of-source-files.html)

[v0.5.17](https://docs.soliditylang.org/en/v0.5.17/layout-of-source-files.html)

[v0.5.16](https://docs.soliditylang.org/en/v0.5.16/layout-of-source-files.html)

[v0.5.15](https://docs.soliditylang.org/en/v0.5.15/layout-of-source-files.html)

[v0.5.14](https://docs.soliditylang.org/en/v0.5.14/layout-of-source-files.html)

[v0.5.13](https://docs.soliditylang.org/en/v0.5.13/layout-of-source-files.html)

[v0.5.12](https://docs.soliditylang.org/en/v0.5.12/layout-of-source-files.html)

[v0.5.11](https://docs.soliditylang.org/en/v0.5.11/layout-of-source-files.html)

[v0.5.10](https://docs.soliditylang.org/en/v0.5.10/layout-of-source-files.html)

[v0.5.9](https://docs.soliditylang.org/en/v0.5.9/layout-of-source-files.html)

[v0.5.8](https://docs.soliditylang.org/en/v0.5.8/layout-of-source-files.html)

[v0.5.7](https://docs.soliditylang.org/en/v0.5.7/layout-of-source-files.html)

[v0.5.6](https://docs.soliditylang.org/en/v0.5.6/layout-of-source-files.html)

[v0.5.5](https://docs.soliditylang.org/en/v0.5.5/layout-of-source-files.html)

[v0.5.4](https://docs.soliditylang.org/en/v0.5.4/layout-of-source-files.html)

[v0.5.3](https://docs.soliditylang.org/en/v0.5.3/layout-of-source-files.html)

[v0.5.2](https://docs.soliditylang.org/en/v0.5.2/layout-of-source-files.html)

[v0.5.1](https://docs.soliditylang.org/en/v0.5.1/layout-of-source-files.html)

[v0.5.0](https://docs.soliditylang.org/en/v0.5.0/layout-of-source-files.html)

[v0.4.26](https://docs.soliditylang.org/en/v0.4.26/layout-of-source-files.html)

[v0.4.25](https://docs.soliditylang.org/en/v0.4.25/layout-of-source-files.html)

[v0.4.24](https://docs.soliditylang.org/en/v0.4.24/layout-of-source-files.html)

[v0.4.23](https://docs.soliditylang.org/en/v0.4.23/layout-of-source-files.html)

[v0.4.22](https://docs.soliditylang.org/en/v0.4.22/layout-of-source-files.html)

[v0.4.21](https://docs.soliditylang.org/en/v0.4.21/layout-of-source-files.html)

[v0.4.20](https://docs.soliditylang.org/en/v0.4.20/layout-of-source-files.html)

[v0.4.19](https://docs.soliditylang.org/en/v0.4.19/layout-of-source-files.html)

[v0.4.18](https://docs.soliditylang.org/en/v0.4.18/layout-of-source-files.html)

[v0.4.17](https://docs.soliditylang.org/en/v0.4.17/layout-of-source-files.html)

[v0.4.16](https://docs.soliditylang.org/en/v0.4.16/layout-of-source-files.html)

[v0.4.15](https://docs.soliditylang.org/en/v0.4.15/layout-of-source-files.html)

[v0.4.14](https://docs.soliditylang.org/en/v0.4.14/layout-of-source-files.html)

[v0.4.13](https://docs.soliditylang.org/en/v0.4.13/layout-of-source-files.html)

[v0.4.12](https://docs.soliditylang.org/en/v0.4.12/layout-of-source-files.html)

[v0.4.11](https://docs.soliditylang.org/en/v0.4.11/layout-of-source-files.html)

[v0.4.10](https://docs.soliditylang.org/en/v0.4.10/layout-of-source-files.html)

[v0.4.9](https://docs.soliditylang.org/en/v0.4.9/layout-of-source-files.html)

[v0.4.8](https://docs.soliditylang.org/en/v0.4.8/layout-of-source-files.html)

[v0.4.7](https://docs.soliditylang.org/en/v0.4.7/layout-of-source-files.html)

[v0.4.6](https://docs.soliditylang.org/en/v0.4.6/layout-of-source-files.html)

[v0.4.5](https://docs.soliditylang.org/en/v0.4.5/layout-of-source-files.html)

[v0.4.4](https://docs.soliditylang.org/en/v0.4.4/layout-of-source-files.html)

[v0.4.3](https://docs.soliditylang.org/en/v0.4.3/layout-of-source-files.html)

[v0.4.2](https://docs.soliditylang.org/en/v0.4.2/layout-of-source-files.html)

[v0.4.1](https://docs.soliditylang.org/en/v0.4.1/layout-of-source-files.html)

[v0.4.0](https://docs.soliditylang.org/en/v0.4.0/layout-of-source-files.html)

[v0.3.6](https://docs.soliditylang.org/en/v0.3.6/layout-of-source-files.html)

[v0.3.5](https://docs.soliditylang.org/en/v0.3.5/layout-of-source-files.html)

[v0.3.4](https://docs.soliditylang.org/en/v0.3.4/layout-of-source-files.html)

[v0.3.3](https://docs.soliditylang.org/en/v0.3.3/layout-of-source-files.html)

[v0.3.2](https://docs.soliditylang.org/en/v0.3.2/layout-of-source-files.html)

[v0.3.1](https://docs.soliditylang.org/en/v0.3.1/layout-of-source-files.html)

[v0.3.0](https://docs.soliditylang.org/en/v0.3.0/layout-of-source-files.html)

[v0.2.2](https://docs.soliditylang.org/en/v0.2.2/layout-of-source-files.html)

[v0.2.1](https://docs.soliditylang.org/en/v0.2.1/layout-of-source-files.html)

[v0.2.0](https://docs.soliditylang.org/en/v0.2.0/layout-of-source-files.html)

[v0.1.7](https://docs.soliditylang.org/en/v0.1.7/layout-of-source-files.html)

[v0.1.6](https://docs.soliditylang.org/en/v0.1.6/layout-of-source-files.html)

[v0.1.5](https://docs.soliditylang.org/en/v0.1.5/layout-of-source-files.html)

[v0.1.4](https://docs.soliditylang.org/en/v0.1.4/layout-of-source-files.html)

[v0.1.3](https://docs.soliditylang.org/en/v0.1.3/layout-of-source-files.html)

[v0.1.2](https://docs.soliditylang.org/en/v0.1.2/layout-of-source-files.html)

[develop](https://docs.soliditylang.org/en/develop/layout-of-source-files.html)

[breaking](https://docs.soliditylang.org/en/breaking/layout-of-source-files.html)

Downloads

[PDF](//docs.soliditylang.org/_/downloads/en/v0.8.21/pdf/)

[Epub](//docs.soliditylang.org/_/downloads/en/v0.8.21/epub/)

On Read the Docs

[Project Home](//readthedocs.org/projects/solidity/)

[Builds](//readthedocs.org/projects/solidity/builds/)

[Downloads](//readthedocs.org/projects/solidity/downloads/)

On GitHub

[View](https://github.com/ethereum/solidity/blob/v0.8.21/docs/layout-of-source-files.rst)

Search

---

Hosted by [Read the Docs](https://readthedocs.org) · [Privacy Policy](https://docs.readthedocs.io/page/privacy-policy.html)

- [](index.html)
- Layout of a Solidity Source File
- [Edit on GitHub](https://github.com/ethereum/solidity/blob/v0.8.21/docs/layout-of-source-files.rst)

---

# Layout of a Solidity Source File[](#layout-of-a-solidity-source-file "Permalink to this heading")

Source files can contain an arbitrary number of [contract definitions](structure-of-a-contract.html#contract-structure), [import](#import) , [pragma](#pragma) and [using for](contracts.html#using-for) directives and [struct](types.html#structs), [enum](types.html#enums), [function](contracts.html#functions), [error](contracts.html#errors) and [constant variable](contracts.html#constants) definitions.

## SPDX License Identifier[](#spdx-license-identifier "Permalink to this heading")

Trust in smart contracts can be better established if their source code is available. Since making source code available always touches on legal problems with regards to copyright, the Solidity compiler encourages the use of machine-readable [SPDX license identifiers](https://spdx.org). Every source file should start with a comment indicating its license:

`// SPDX-License-Identifier: MIT`

The compiler does not validate that the license is part of the [list allowed by SPDX](https://spdx.org/licenses/), but it does include the supplied string in the [bytecode metadata](metadata.html#metadata).

If you do not want to specify a license or if the source code is not open-source, please use the special value `UNLICENSED`. Note that `UNLICENSED` (no usage allowed, not present in SPDX license list) is different from `UNLICENSE` (grants all rights to everyone). Solidity follows [the npm recommendation](https://docs.npmjs.com/cli/v7/configuring-npm/package-json#license).

Supplying this comment of course does not free you from other obligations related to licensing like having to mention a specific license header in each source file or the original copyright holder.

The comment is recognized by the compiler anywhere in the file at the file level, but it is recommended to put it at the top of the file.

More information about how to use SPDX license identifiers can be found at the [SPDX website](https://spdx.org/ids-how).

## Pragmas[](#pragmas "Permalink to this heading")

The `pragma` keyword is used to enable certain compiler features or checks. A pragma directive is always local to a source file, so you have to add the pragma to all your files if you want to enable it in your whole project. If you [import](#import) another file, the pragma from that file does _not_ automatically apply to the importing file.

### Version Pragma[](#version-pragma "Permalink to this heading")

Source files can (and should) be annotated with a version pragma to reject compilation with future compiler versions that might introduce incompatible changes. We try to keep these to an absolute minimum and introduce them in a way that changes in semantics also require changes in the syntax, but this is not always possible. Because of this, it is always a good idea to read through the changelog at least for releases that contain breaking changes. These releases always have versions of the form `0.x.0` or `x.0.0`.

The version pragma is used as follows: `pragma solidity ^0.5.2;`

A source file with the line above does not compile with a compiler earlier than version 0.5.2, and it also does not work on a compiler starting from version 0.6.0 (this second condition is added by using `^`). Because there will be no breaking changes until version `0.6.0`, you can be sure that your code compiles the way you intended. The exact version of the compiler is not fixed, so that bugfix releases are still possible.

It is possible to specify more complex rules for the compiler version, these follow the same syntax used by [npm](https://docs.npmjs.com/cli/v6/using-npm/semver).

Note

Using the version pragma _does not_ change the version of the compiler. It also _does not_ enable or disable features of the compiler. It just instructs the compiler to check whether its version matches the one required by the pragma. If it does not match, the compiler issues an error.

### ABI Coder Pragma[](#abi-coder-pragma "Permalink to this heading")

By using `pragma abicoder v1` or `pragma abicoder v2` you can select between the two implementations of the ABI encoder and decoder.

The new ABI coder (v2) is able to encode and decode arbitrarily nested arrays and structs. Apart from supporting more types, it involves more extensive validation and safety checks, which may result in higher gas costs, but also heightened security. It is considered non-experimental as of Solidity 0.6.0 and it is enabled by default starting with Solidity 0.8.0. The old ABI coder can still be selected using `pragma abicoder v1;`.

The set of types supported by the new encoder is a strict superset of the ones supported by the old one. Contracts that use it can interact with ones that do not without limitations. The reverse is possible only as long as the non-`abicoder v2` contract does not try to make calls that would require decoding types only supported by the new encoder. The compiler can detect this and will issue an error. Simply enabling `abicoder v2` for your contract is enough to make the error go away.

Note

This pragma applies to all the code defined in the file where it is activated, regardless of where that code ends up eventually. This means that a contract whose source file is selected to compile with ABI coder v1 can still contain code that uses the new encoder by inheriting it from another contract. This is allowed if the new types are only used internally and not in external function signatures.

Note

Up to Solidity 0.7.4, it was possible to select the ABI coder v2 by using `pragma experimental ABIEncoderV2`, but it was not possible to explicitly select coder v1 because it was the default.

### Experimental Pragma[](#experimental-pragma "Permalink to this heading")

The second pragma is the experimental pragma. It can be used to enable features of the compiler or language that are not yet enabled by default. The following experimental pragmas are currently supported:

#### ABIEncoderV2[](#abiencoderv2 "Permalink to this heading")

Because the ABI coder v2 is not considered experimental anymore, it can be selected via `pragma abicoder v2` (please see above) since Solidity 0.7.4.

#### SMTChecker[](#smtchecker "Permalink to this heading")

This component has to be enabled when the Solidity compiler is built and therefore it is not available in all Solidity binaries. The [build instructions](installing-solidity.html#smt-solvers-build) explain how to activate this option. It is activated for the Ubuntu PPA releases in most versions, but not for the Docker images, Windows binaries or the statically-built Linux binaries. It can be activated for solc-js via the [smtCallback](https://github.com/ethereum/solc-js#example-usage-with-smtsolver-callback) if you have an SMT solver installed locally and run solc-js via node (not via the browser).

If you use `pragma experimental SMTChecker;`, then you get additional [safety warnings](smtchecker.html#formal-verification) which are obtained by querying an SMT solver. The component does not yet support all features of the Solidity language and likely outputs many warnings. In case it reports unsupported features, the analysis may not be fully sound.

## Importing other Source Files[](#importing-other-source-files "Permalink to this heading")

### Syntax and Semantics[](#syntax-and-semantics "Permalink to this heading")

Solidity supports import statements to help modularise your code that are similar to those available in JavaScript (from ES6 on). However, Solidity does not support the concept of a [default export](https://developer.mozilla.org/en-US/docs/web/javascript/reference/statements/export#description).

At a global level, you can use import statements of the following form:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=aW1wb3J0ICJmaWxlbmFtZSI7)

import "filename";

The `filename` part is called an _import path_. This statement imports all global symbols from “filename” (and symbols imported there) into the current global scope (different than in ES6 but backwards-compatible for Solidity). This form is not recommended for use, because it unpredictably pollutes the namespace. If you add new top-level items inside “filename”, they automatically appear in all files that import like this from “filename”. It is better to import specific symbols explicitly.

The following example creates a new global symbol `symbolName` whose members are all the global symbols from `"filename"`:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=aW1wb3J0ICogYXMgc3ltYm9sTmFtZSBmcm9tICJmaWxlbmFtZSI7)

import * as symbolName from "filename";

which results in all global symbols being available in the format `symbolName.symbol`.

A variant of this syntax that is not part of ES6, but possibly useful is:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=aW1wb3J0ICJmaWxlbmFtZSIgYXMgc3ltYm9sTmFtZTs=)

import "filename" as symbolName;

which is equivalent to `import * as symbolName from "filename";`.

If there is a naming collision, you can rename symbols while importing. For example, the code below creates new global symbols `alias` and `symbol2` which reference `symbol1` and `symbol2` from inside `"filename"`, respectively.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=aW1wb3J0IHtzeW1ib2wxIGFzIGFsaWFzLCBzeW1ib2wyfSBmcm9tICJmaWxlbmFtZSI7)

import {symbol1 as alias, symbol2} from "filename";

### Import Paths[](#import-paths "Permalink to this heading")

In order to be able to support reproducible builds on all platforms, the Solidity compiler has to abstract away the details of the filesystem where source files are stored. For this reason import paths do not refer directly to files in the host filesystem. Instead the compiler maintains an internal database (_virtual filesystem_ or _VFS_ for short) where each source unit is assigned a unique _source unit name_ which is an opaque and unstructured identifier. The import path specified in an import statement is translated into a source unit name and used to find the corresponding source unit in this database.

Using the [Standard JSON](using-the-compiler.html#compiler-api) API it is possible to directly provide the names and content of all the source files as a part of the compiler input. In this case source unit names are truly arbitrary. If, however, you want the compiler to automatically find and load source code into the VFS, your source unit names need to be structured in a way that makes it possible for an [import callback](path-resolution.html#import-callback) to locate them. When using the command-line compiler the default import callback supports only loading source code from the host filesystem, which means that your source unit names must be paths. Some environments provide custom callbacks that are more versatile. For example the [Remix IDE](https://remix.ethereum.org/) provides one that lets you [import files from HTTP, IPFS and Swarm URLs or refer directly to packages in NPM registry](https://remix-ide.readthedocs.io/en/latest/import.html).

For a complete description of the virtual filesystem and the path resolution logic used by the compiler see [Path Resolution](path-resolution.html#path-resolution).

## Comments[](#comments "Permalink to this heading")

Single-line comments (`//`) and multi-line comments (`/*...*/`) are possible.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gVGhpcyBpcyBhIHNpbmdsZS1saW5lIGNvbW1lbnQuCgovKgpUaGlzIGlzIGEKbXVsdGktbGluZSBjb21tZW50LgoqLw==)

// This is a single-line comment.

/*
This is a
multi-line comment.
*/

Note

A single-line comment is terminated by any unicode line terminator (LF, VF, FF, CR, NEL, LS or PS) in UTF-8 encoding. The terminator is still part of the source code after the comment, so if it is not an ASCII symbol (these are NEL, LS and PS), it will lead to a parser error.

Additionally, there is another type of comment called a NatSpec comment, which is detailed in the [style guide](style-guide.html#style-guide-natspec). They are written with a triple slash (`///`) or a double asterisk block (`/** ... */`) and they should be used directly above function declarations or statements.

[Previous](installing-solidity.html "Installing the Solidity Compiler") [Next](structure-of-a-contract.html "Structure of a Contract")

---

© Copyright 2016-2023, The Solidity Authors. Revision `1acebf78`.

Customized with ❤️ by the [ethereum.org](https://ethereum.org/) team.

[Credits and attribution](credits-and-attribution.html).