[![Solidity logo](https://docs.soliditylang.org/en/v0.8.21/assembly.html_static/img/logo.svg)](https://soliditylang.org)[{ skip to content }](#content)

[Blog](https://soliditylang.org/blog)[Documentation](/)[Use cases](https://soliditylang.org/use-cases)[Contribute](/en/latest/contributing.html)[About](https://soliditylang.org/about)[Forum](https://forum.soliditylang.org/)

![Color mode toggle icon](https://docs.soliditylang.org/en/v0.8.21/assembly.html_static/img/moon.svg)![Toggle menu](https://docs.soliditylang.org/en/v0.8.21/assembly.html_static/img/hamburger-light.svg)

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
- [Inline Assembly](#)
    - [Example](#example)
    - [Access to External Variables, Functions and Libraries](#access-to-external-variables-functions-and-libraries)
    - [Things to Avoid](#things-to-avoid)
    - [Conventions in Solidity](#conventions-in-solidity)
        - [Values of Typed Variables](#values-of-typed-variables)
        - [Memory Management](#memory-management)
        - [Memory Safety](#memory-safety)
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

[en](https://docs.soliditylang.org/en/v0.8.21/assembly.html)

[zh](https://docs.soliditylang.org/zh/v0.8.19/assembly.html)

[fr](https://docs.soliditylang.org/fr/latest/assembly.html)

[tr](https://docs.soliditylang.org/tr/v0.8.16/assembly.html)

Versions

[latest](https://docs.soliditylang.org/en/latest/assembly.html)

[stable](https://docs.soliditylang.org/en/stable/assembly.html)

[v0.8.21](https://docs.soliditylang.org/en/v0.8.21/assembly.html)

[v0.8.20](https://docs.soliditylang.org/en/v0.8.20/assembly.html)

[v0.8.19](https://docs.soliditylang.org/en/v0.8.19/assembly.html)

[v0.8.18](https://docs.soliditylang.org/en/v0.8.18/assembly.html)

[v0.8.17](https://docs.soliditylang.org/en/v0.8.17/assembly.html)

[v0.8.16](https://docs.soliditylang.org/en/v0.8.16/assembly.html)

[v0.8.15](https://docs.soliditylang.org/en/v0.8.15/assembly.html)

[v0.8.14](https://docs.soliditylang.org/en/v0.8.14/assembly.html)

[v0.8.13](https://docs.soliditylang.org/en/v0.8.13/assembly.html)

[v0.8.12](https://docs.soliditylang.org/en/v0.8.12/assembly.html)

[v0.8.11](https://docs.soliditylang.org/en/v0.8.11/assembly.html)

[v0.8.10](https://docs.soliditylang.org/en/v0.8.10/assembly.html)

[v0.8.9](https://docs.soliditylang.org/en/v0.8.9/assembly.html)

[v0.8.8](https://docs.soliditylang.org/en/v0.8.8/assembly.html)

[v0.8.7](https://docs.soliditylang.org/en/v0.8.7/assembly.html)

[v0.8.6](https://docs.soliditylang.org/en/v0.8.6/assembly.html)

[v0.8.5](https://docs.soliditylang.org/en/v0.8.5/assembly.html)

[v0.8.4](https://docs.soliditylang.org/en/v0.8.4/assembly.html)

[v0.8.3](https://docs.soliditylang.org/en/v0.8.3/assembly.html)

[v0.8.2](https://docs.soliditylang.org/en/v0.8.2/assembly.html)

[v0.8.1](https://docs.soliditylang.org/en/v0.8.1/assembly.html)

[v0.8.0](https://docs.soliditylang.org/en/v0.8.0/assembly.html)

[v0.7.6](https://docs.soliditylang.org/en/v0.7.6/assembly.html)

[v0.7.5](https://docs.soliditylang.org/en/v0.7.5/assembly.html)

[v0.7.4](https://docs.soliditylang.org/en/v0.7.4/assembly.html)

[v0.7.3](https://docs.soliditylang.org/en/v0.7.3/assembly.html)

[v0.7.2](https://docs.soliditylang.org/en/v0.7.2/assembly.html)

[v0.7.1](https://docs.soliditylang.org/en/v0.7.1/assembly.html)

[v0.7.0](https://docs.soliditylang.org/en/v0.7.0/assembly.html)

[v0.6.12](https://docs.soliditylang.org/en/v0.6.12/assembly.html)

[v0.6.11](https://docs.soliditylang.org/en/v0.6.11/assembly.html)

[v0.6.10](https://docs.soliditylang.org/en/v0.6.10/assembly.html)

[v0.6.9](https://docs.soliditylang.org/en/v0.6.9/assembly.html)

[v0.6.8](https://docs.soliditylang.org/en/v0.6.8/assembly.html)

[v0.6.7](https://docs.soliditylang.org/en/v0.6.7/assembly.html)

[v0.6.6](https://docs.soliditylang.org/en/v0.6.6/assembly.html)

[v0.6.5](https://docs.soliditylang.org/en/v0.6.5/assembly.html)

[v0.6.4](https://docs.soliditylang.org/en/v0.6.4/assembly.html)

[v0.6.3](https://docs.soliditylang.org/en/v0.6.3/assembly.html)

[v0.6.2](https://docs.soliditylang.org/en/v0.6.2/assembly.html)

[v0.6.1](https://docs.soliditylang.org/en/v0.6.1/assembly.html)

[v0.6.0](https://docs.soliditylang.org/en/v0.6.0/assembly.html)

[v0.5.17](https://docs.soliditylang.org/en/v0.5.17/assembly.html)

[v0.5.16](https://docs.soliditylang.org/en/v0.5.16/assembly.html)

[v0.5.15](https://docs.soliditylang.org/en/v0.5.15/assembly.html)

[v0.5.14](https://docs.soliditylang.org/en/v0.5.14/assembly.html)

[v0.5.13](https://docs.soliditylang.org/en/v0.5.13/assembly.html)

[v0.5.12](https://docs.soliditylang.org/en/v0.5.12/assembly.html)

[v0.5.11](https://docs.soliditylang.org/en/v0.5.11/assembly.html)

[v0.5.10](https://docs.soliditylang.org/en/v0.5.10/assembly.html)

[v0.5.9](https://docs.soliditylang.org/en/v0.5.9/assembly.html)

[v0.5.8](https://docs.soliditylang.org/en/v0.5.8/assembly.html)

[v0.5.7](https://docs.soliditylang.org/en/v0.5.7/assembly.html)

[v0.5.6](https://docs.soliditylang.org/en/v0.5.6/assembly.html)

[v0.5.5](https://docs.soliditylang.org/en/v0.5.5/assembly.html)

[v0.5.4](https://docs.soliditylang.org/en/v0.5.4/assembly.html)

[v0.5.3](https://docs.soliditylang.org/en/v0.5.3/assembly.html)

[v0.5.2](https://docs.soliditylang.org/en/v0.5.2/assembly.html)

[v0.5.1](https://docs.soliditylang.org/en/v0.5.1/assembly.html)

[v0.5.0](https://docs.soliditylang.org/en/v0.5.0/assembly.html)

[v0.4.26](https://docs.soliditylang.org/en/v0.4.26/assembly.html)

[v0.4.25](https://docs.soliditylang.org/en/v0.4.25/assembly.html)

[v0.4.24](https://docs.soliditylang.org/en/v0.4.24/assembly.html)

[v0.4.23](https://docs.soliditylang.org/en/v0.4.23/assembly.html)

[v0.4.22](https://docs.soliditylang.org/en/v0.4.22/assembly.html)

[v0.4.21](https://docs.soliditylang.org/en/v0.4.21/assembly.html)

[v0.4.20](https://docs.soliditylang.org/en/v0.4.20/assembly.html)

[v0.4.19](https://docs.soliditylang.org/en/v0.4.19/assembly.html)

[v0.4.18](https://docs.soliditylang.org/en/v0.4.18/assembly.html)

[v0.4.17](https://docs.soliditylang.org/en/v0.4.17/assembly.html)

[v0.4.16](https://docs.soliditylang.org/en/v0.4.16/assembly.html)

[v0.4.15](https://docs.soliditylang.org/en/v0.4.15/assembly.html)

[v0.4.14](https://docs.soliditylang.org/en/v0.4.14/assembly.html)

[v0.4.13](https://docs.soliditylang.org/en/v0.4.13/assembly.html)

[v0.4.12](https://docs.soliditylang.org/en/v0.4.12/assembly.html)

[v0.4.11](https://docs.soliditylang.org/en/v0.4.11/assembly.html)

[v0.4.10](https://docs.soliditylang.org/en/v0.4.10/assembly.html)

[v0.4.9](https://docs.soliditylang.org/en/v0.4.9/assembly.html)

[v0.4.8](https://docs.soliditylang.org/en/v0.4.8/assembly.html)

[v0.4.7](https://docs.soliditylang.org/en/v0.4.7/assembly.html)

[v0.4.6](https://docs.soliditylang.org/en/v0.4.6/assembly.html)

[v0.4.5](https://docs.soliditylang.org/en/v0.4.5/assembly.html)

[v0.4.4](https://docs.soliditylang.org/en/v0.4.4/assembly.html)

[v0.4.3](https://docs.soliditylang.org/en/v0.4.3/assembly.html)

[v0.4.2](https://docs.soliditylang.org/en/v0.4.2/assembly.html)

[v0.4.1](https://docs.soliditylang.org/en/v0.4.1/assembly.html)

[v0.4.0](https://docs.soliditylang.org/en/v0.4.0/assembly.html)

[v0.3.6](https://docs.soliditylang.org/en/v0.3.6/assembly.html)

[v0.3.5](https://docs.soliditylang.org/en/v0.3.5/assembly.html)

[v0.3.4](https://docs.soliditylang.org/en/v0.3.4/assembly.html)

[v0.3.3](https://docs.soliditylang.org/en/v0.3.3/assembly.html)

[v0.3.2](https://docs.soliditylang.org/en/v0.3.2/assembly.html)

[v0.3.1](https://docs.soliditylang.org/en/v0.3.1/assembly.html)

[v0.3.0](https://docs.soliditylang.org/en/v0.3.0/assembly.html)

[v0.2.2](https://docs.soliditylang.org/en/v0.2.2/assembly.html)

[v0.2.1](https://docs.soliditylang.org/en/v0.2.1/assembly.html)

[v0.2.0](https://docs.soliditylang.org/en/v0.2.0/assembly.html)

[v0.1.7](https://docs.soliditylang.org/en/v0.1.7/assembly.html)

[v0.1.6](https://docs.soliditylang.org/en/v0.1.6/assembly.html)

[v0.1.5](https://docs.soliditylang.org/en/v0.1.5/assembly.html)

[v0.1.4](https://docs.soliditylang.org/en/v0.1.4/assembly.html)

[v0.1.3](https://docs.soliditylang.org/en/v0.1.3/assembly.html)

[v0.1.2](https://docs.soliditylang.org/en/v0.1.2/assembly.html)

[develop](https://docs.soliditylang.org/en/develop/assembly.html)

[breaking](https://docs.soliditylang.org/en/breaking/assembly.html)

Downloads

[PDF](//docs.soliditylang.org/_/downloads/en/v0.8.21/pdf/)

[Epub](//docs.soliditylang.org/_/downloads/en/v0.8.21/epub/)

On Read the Docs

[Project Home](//readthedocs.org/projects/solidity/)

[Builds](//readthedocs.org/projects/solidity/builds/)

[Downloads](//readthedocs.org/projects/solidity/downloads/)

On GitHub

[View](https://github.com/ethereum/solidity/blob/v0.8.21/docs/assembly.rst)

Search

---

Hosted by [Read the Docs](https://readthedocs.org) · [Privacy Policy](https://docs.readthedocs.io/page/privacy-policy.html)

- [](index.html)
- Inline Assembly
- [Edit on GitHub](https://github.com/ethereum/solidity/blob/v0.8.21/docs/assembly.rst)

---

# Inline Assembly[](#inline-assembly "Permalink to this heading")

You can interleave Solidity statements with inline assembly in a language close to the one of the Ethereum Virtual Machine. This gives you more fine-grained control, which is especially useful when you are enhancing the language by writing libraries.

The language used for inline assembly in Solidity is called [Yul](yul.html#yul) and it is documented in its own section. This section will only cover how the inline assembly code can interface with the surrounding Solidity code.

Warning

Inline assembly is a way to access the Ethereum Virtual Machine at a low level. This bypasses several important safety features and checks of Solidity. You should only use it for tasks that need it, and only if you are confident with using it.

An inline assembly block is marked by `assembly { ... }`, where the code inside the curly braces is code in the [Yul](yul.html#yul) language.

The inline assembly code can access local Solidity variables as explained below.

Different inline assembly blocks share no namespace, i.e. it is not possible to call a Yul function or access a Yul variable defined in a different inline assembly block.

## Example[](#example "Permalink to this heading")

The following example provides library code to access the code of another contract and load it into a `bytes` variable. This is possible with “plain Solidity” too, by using `<address>.code`. But the point here is that reusable assembly libraries can enhance the Solidity language without a compiler change.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmxpYnJhcnkgR2V0Q29kZSB7CiAgICBmdW5jdGlvbiBhdChhZGRyZXNzIGFkZHIpIHB1YmxpYyB2aWV3IHJldHVybnMgKGJ5dGVzIG1lbW9yeSBjb2RlKSB7CiAgICAgICAgYXNzZW1ibHkgewogICAgICAgICAgICAvLyByZXRyaWV2ZSB0aGUgc2l6ZSBvZiB0aGUgY29kZSwgdGhpcyBuZWVkcyBhc3NlbWJseQogICAgICAgICAgICBsZXQgc2l6ZSA6PSBleHRjb2Rlc2l6ZShhZGRyKQogICAgICAgICAgICAvLyBhbGxvY2F0ZSBvdXRwdXQgYnl0ZSBhcnJheSAtIHRoaXMgY291bGQgYWxzbyBiZSBkb25lIHdpdGhvdXQgYXNzZW1ibHkKICAgICAgICAgICAgLy8gYnkgdXNpbmcgY29kZSA9IG5ldyBieXRlcyhzaXplKQogICAgICAgICAgICBjb2RlIDo9IG1sb2FkKDB4NDApCiAgICAgICAgICAgIC8vIG5ldyAibWVtb3J5IGVuZCIgaW5jbHVkaW5nIHBhZGRpbmcKICAgICAgICAgICAgbXN0b3JlKDB4NDAsIGFkZChjb2RlLCBhbmQoYWRkKGFkZChzaXplLCAweDIwKSwgMHgxZiksIG5vdCgweDFmKSkpKQogICAgICAgICAgICAvLyBzdG9yZSBsZW5ndGggaW4gbWVtb3J5CiAgICAgICAgICAgIG1zdG9yZShjb2RlLCBzaXplKQogICAgICAgICAgICAvLyBhY3R1YWxseSByZXRyaWV2ZSB0aGUgY29kZSwgdGhpcyBuZWVkcyBhc3NlbWJseQogICAgICAgICAgICBleHRjb2RlY29weShhZGRyLCBhZGQoY29kZSwgMHgyMCksIDAsIHNpemUpCiAgICAgICAgfQogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

library GetCode {
    function at(address addr) public view returns (bytes memory code) {
        assembly {
            // retrieve the size of the code, this needs assembly
            let size := extcodesize(addr)
            // allocate output byte array - this could also be done without assembly
            // by using code = new bytes(size)
            code := mload(0x40)
            // new "memory end" including padding
            mstore(0x40, add(code, and(add(add(size, 0x20), 0x1f), not(0x1f))))
            // store length in memory
            mstore(code, size)
            // actually retrieve the code, this needs assembly
            extcodecopy(addr, add(code, 0x20), 0, size)
        }
    }
}

Inline assembly is also beneficial in cases where the optimizer fails to produce efficient code, for example:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCgpsaWJyYXJ5IFZlY3RvclN1bSB7CiAgICAvLyBUaGlzIGZ1bmN0aW9uIGlzIGxlc3MgZWZmaWNpZW50IGJlY2F1c2UgdGhlIG9wdGltaXplciBjdXJyZW50bHkgZmFpbHMgdG8KICAgIC8vIHJlbW92ZSB0aGUgYm91bmRzIGNoZWNrcyBpbiBhcnJheSBhY2Nlc3MuCiAgICBmdW5jdGlvbiBzdW1Tb2xpZGl0eSh1aW50W10gbWVtb3J5IGRhdGEpIHB1YmxpYyBwdXJlIHJldHVybnMgKHVpbnQgc3VtKSB7CiAgICAgICAgZm9yICh1aW50IGkgPSAwOyBpIDwgZGF0YS5sZW5ndGg7ICsraSkKICAgICAgICAgICAgc3VtICs9IGRhdGFbaV07CiAgICB9CgogICAgLy8gV2Uga25vdyB0aGF0IHdlIG9ubHkgYWNjZXNzIHRoZSBhcnJheSBpbiBib3VuZHMsIHNvIHdlIGNhbiBhdm9pZCB0aGUgY2hlY2suCiAgICAvLyAweDIwIG5lZWRzIHRvIGJlIGFkZGVkIHRvIGFuIGFycmF5IGJlY2F1c2UgdGhlIGZpcnN0IHNsb3QgY29udGFpbnMgdGhlCiAgICAvLyBhcnJheSBsZW5ndGguCiAgICBmdW5jdGlvbiBzdW1Bc20odWludFtdIG1lbW9yeSBkYXRhKSBwdWJsaWMgcHVyZSByZXR1cm5zICh1aW50IHN1bSkgewogICAgICAgIGZvciAodWludCBpID0gMDsgaSA8IGRhdGEubGVuZ3RoOyArK2kpIHsKICAgICAgICAgICAgYXNzZW1ibHkgewogICAgICAgICAgICAgICAgc3VtIDo9IGFkZChzdW0sIG1sb2FkKGFkZChhZGQoZGF0YSwgMHgyMCksIG11bChpLCAweDIwKSkpKQogICAgICAgICAgICB9CiAgICAgICAgfQogICAgfQoKICAgIC8vIFNhbWUgYXMgYWJvdmUsIGJ1dCBhY2NvbXBsaXNoIHRoZSBlbnRpcmUgY29kZSB3aXRoaW4gaW5saW5lIGFzc2VtYmx5LgogICAgZnVuY3Rpb24gc3VtUHVyZUFzbSh1aW50W10gbWVtb3J5IGRhdGEpIHB1YmxpYyBwdXJlIHJldHVybnMgKHVpbnQgc3VtKSB7CiAgICAgICAgYXNzZW1ibHkgewogICAgICAgICAgICAvLyBMb2FkIHRoZSBsZW5ndGggKGZpcnN0IDMyIGJ5dGVzKQogICAgICAgICAgICBsZXQgbGVuIDo9IG1sb2FkKGRhdGEpCgogICAgICAgICAgICAvLyBTa2lwIG92ZXIgdGhlIGxlbmd0aCBmaWVsZC4KICAgICAgICAgICAgLy8KICAgICAgICAgICAgLy8gS2VlcCB0ZW1wb3JhcnkgdmFyaWFibGUgc28gaXQgY2FuIGJlIGluY3JlbWVudGVkIGluIHBsYWNlLgogICAgICAgICAgICAvLwogICAgICAgICAgICAvLyBOT1RFOiBpbmNyZW1lbnRpbmcgZGF0YSB3b3VsZCByZXN1bHQgaW4gYW4gdW51c2FibGUKICAgICAgICAgICAgLy8gICAgICAgZGF0YSB2YXJpYWJsZSBhZnRlciB0aGlzIGFzc2VtYmx5IGJsb2NrCiAgICAgICAgICAgIGxldCBkYXRhRWxlbWVudExvY2F0aW9uIDo9IGFkZChkYXRhLCAweDIwKQoKICAgICAgICAgICAgLy8gSXRlcmF0ZSB1bnRpbCB0aGUgYm91bmQgaXMgbm90IG1ldC4KICAgICAgICAgICAgZm9yCiAgICAgICAgICAgICAgICB7IGxldCBlbmQgOj0gYWRkKGRhdGFFbGVtZW50TG9jYXRpb24sIG11bChsZW4sIDB4MjApKSB9CiAgICAgICAgICAgICAgICBsdChkYXRhRWxlbWVudExvY2F0aW9uLCBlbmQpCiAgICAgICAgICAgICAgICB7IGRhdGFFbGVtZW50TG9jYXRpb24gOj0gYWRkKGRhdGFFbGVtZW50TG9jYXRpb24sIDB4MjApIH0KICAgICAgICAgICAgewogICAgICAgICAgICAgICAgc3VtIDo9IGFkZChzdW0sIG1sb2FkKGRhdGFFbGVtZW50TG9jYXRpb24pKQogICAgICAgICAgICB9CiAgICAgICAgfQogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

library VectorSum {
    // This function is less efficient because the optimizer currently fails to
    // remove the bounds checks in array access.
    function sumSolidity(uint[] memory data) public pure returns (uint sum) {
        for (uint i = 0; i < data.length; ++i)
            sum += data[i];
    }

    // We know that we only access the array in bounds, so we can avoid the check.
    // 0x20 needs to be added to an array because the first slot contains the
    // array length.
    function sumAsm(uint[] memory data) public pure returns (uint sum) {
        for (uint i = 0; i < data.length; ++i) {
            assembly {
                sum := add(sum, mload(add(add(data, 0x20), mul(i, 0x20))))
            }
        }
    }

    // Same as above, but accomplish the entire code within inline assembly.
    function sumPureAsm(uint[] memory data) public pure returns (uint sum) {
        assembly {
            // Load the length (first 32 bytes)
            let len := mload(data)

            // Skip over the length field.
            //
            // Keep temporary variable so it can be incremented in place.
            //
            // NOTE: incrementing data would result in an unusable
            //       data variable after this assembly block
            let dataElementLocation := add(data, 0x20)

            // Iterate until the bound is not met.
            for
                { let end := add(dataElementLocation, mul(len, 0x20)) }
                lt(dataElementLocation, end)
                { dataElementLocation := add(dataElementLocation, 0x20) }
            {
                sum := add(sum, mload(dataElementLocation))
            }
        }
    }
}

## Access to External Variables, Functions and Libraries[](#access-to-external-variables-functions-and-libraries "Permalink to this heading")

You can access Solidity variables and other identifiers by using their name.

Local variables of value type are directly usable in inline assembly. They can both be read and assigned to.

Local variables that refer to memory evaluate to the address of the variable in memory, not the value itself. Such variables can also be assigned to, but note that an assignment will only change the pointer and not the data and that it is your responsibility to respect Solidity’s memory management. See [Conventions in Solidity](#conventions-in-solidity).

Similarly, local variables that refer to statically-sized calldata arrays or calldata structs evaluate to the address of the variable in calldata, not the value itself. The variable can also be assigned a new offset, but note that no validation is performed to ensure that the variable will not point beyond `calldatasize()`.

For external function pointers the address and the function selector can be accessed using `x.address` and `x.selector`. The selector consists of four right-aligned bytes. Both values can be assigned to. For example:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC44LjEwIDwwLjkuMDsKCmNvbnRyYWN0IEMgewogICAgLy8gQXNzaWducyBhIG5ldyBzZWxlY3RvciBhbmQgYWRkcmVzcyB0byB0aGUgcmV0dXJuIHZhcmlhYmxlIEBmdW4KICAgIGZ1bmN0aW9uIGNvbWJpbmVUb0Z1bmN0aW9uUG9pbnRlcihhZGRyZXNzIG5ld0FkZHJlc3MsIHVpbnQgbmV3U2VsZWN0b3IpIHB1YmxpYyBwdXJlIHJldHVybnMgKGZ1bmN0aW9uKCkgZXh0ZXJuYWwgZnVuKSB7CiAgICAgICAgYXNzZW1ibHkgewogICAgICAgICAgICBmdW4uc2VsZWN0b3IgOj0gbmV3U2VsZWN0b3IKICAgICAgICAgICAgZnVuLmFkZHJlc3MgIDo9IG5ld0FkZHJlc3MKICAgICAgICB9CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.8.10 <0.9.0;

contract C {
    // Assigns a new selector and address to the return variable @fun
    function combineToFunctionPointer(address newAddress, uint newSelector) public pure returns (function() external fun) {
        assembly {
            fun.selector := newSelector
            fun.address  := newAddress
        }
    }
}

For dynamic calldata arrays, you can access their calldata offset (in bytes) and length (number of elements) using `x.offset` and `x.length`. Both expressions can also be assigned to, but as for the static case, no validation will be performed to ensure that the resulting data area is within the bounds of `calldatasize()`.

For local storage variables or state variables, a single Yul identifier is not sufficient, since they do not necessarily occupy a single full storage slot. Therefore, their “address” is composed of a slot and a byte-offset inside that slot. To retrieve the slot pointed to by the variable `x`, you use `x.slot`, and to retrieve the byte-offset you use `x.offset`. Using `x` itself will result in an error.

You can also assign to the `.slot` part of a local storage variable pointer. For these (structs, arrays or mappings), the `.offset` part is always zero. It is not possible to assign to the `.slot` or `.offset` part of a state variable, though.

Local Solidity variables are available for assignments, for example:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwoKY29udHJhY3QgQyB7CiAgICB1aW50IGI7CiAgICBmdW5jdGlvbiBmKHVpbnQgeCkgcHVibGljIHZpZXcgcmV0dXJucyAodWludCByKSB7CiAgICAgICAgYXNzZW1ibHkgewogICAgICAgICAgICAvLyBXZSBpZ25vcmUgdGhlIHN0b3JhZ2Ugc2xvdCBvZmZzZXQsIHdlIGtub3cgaXQgaXMgemVybwogICAgICAgICAgICAvLyBpbiB0aGlzIHNwZWNpYWwgY2FzZS4KICAgICAgICAgICAgciA6PSBtdWwoeCwgc2xvYWQoYi5zbG90KSkKICAgICAgICB9CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

contract C {
    uint b;
    function f(uint x) public view returns (uint r) {
        assembly {
            // We ignore the storage slot offset, we know it is zero
            // in this special case.
            r := mul(x, sload(b.slot))
        }
    }
}

Warning

If you access variables of a type that spans less than 256 bits (for example `uint64`, `address`, or `bytes16`), you cannot make any assumptions about bits not part of the encoding of the type. Especially, do not assume them to be zero. To be safe, always clear the data properly before you use it in a context where this is important: `uint32 x = f(); assembly { x := and(x, 0xffffffff) /* now use x */ }` To clean signed types, you can use the `signextend` opcode: `assembly { signextend(<num_bytes_of_x_minus_one>, x) }`

Since Solidity 0.6.0, the name of a inline assembly variable may not shadow any declaration visible in the scope of the inline assembly block (including variable, contract and function declarations).

Since Solidity 0.7.0, variables and functions declared inside the inline assembly block may not contain `.`, but using `.` is valid to access Solidity variables from outside the inline assembly block.

## Things to Avoid[](#things-to-avoid "Permalink to this heading")

Inline assembly might have a quite high-level look, but it actually is extremely low-level. Function calls, loops, ifs and switches are converted by simple rewriting rules and after that, the only thing the assembler does for you is re-arranging functional-style opcodes, counting stack height for variable access and removing stack slots for assembly-local variables when the end of their block is reached.

## Conventions in Solidity[](#conventions-in-solidity "Permalink to this heading")

### Values of Typed Variables[](#values-of-typed-variables "Permalink to this heading")

In contrast to EVM assembly, Solidity has types which are narrower than 256 bits, e.g. `uint24`. For efficiency, most arithmetic operations ignore the fact that types can be shorter than 256 bits, and the higher-order bits are cleaned when necessary, i.e., shortly before they are written to memory or before comparisons are performed. This means that if you access such a variable from within inline assembly, you might have to manually clean the higher-order bits first.

### Memory Management[](#memory-management "Permalink to this heading")

Solidity manages memory in the following way. There is a “free memory pointer” at position `0x40` in memory. If you want to allocate memory, use the memory starting from where this pointer points at and update it. There is no guarantee that the memory has not been used before and thus you cannot assume that its contents are zero bytes. There is no built-in mechanism to release or free allocated memory. Here is an assembly snippet you can use for allocating memory that follows the process outlined above:

[open in Remix](https://remix.ethereum.org/?#language=yul&version=0.8.21&code=ZnVuY3Rpb24gYWxsb2NhdGUobGVuZ3RoKSAtPiBwb3MgewogIHBvcyA6PSBtbG9hZCgweDQwKQogIG1zdG9yZSgweDQwLCBhZGQocG9zLCBsZW5ndGgpKQp9)

function allocate(length) -> pos {
  pos := mload(0x40)
  mstore(0x40, add(pos, length))
}

The first 64 bytes of memory can be used as “scratch space” for short-term allocation. The 32 bytes after the free memory pointer (i.e., starting at `0x60`) are meant to be zero permanently and is used as the initial value for empty dynamic memory arrays. This means that the allocatable memory starts at `0x80`, which is the initial value of the free memory pointer.

Elements in memory arrays in Solidity always occupy multiples of 32 bytes (this is even true for `bytes1[]`, but not for `bytes` and `string`). Multi-dimensional memory arrays are pointers to memory arrays. The length of a dynamic array is stored at the first slot of the array and followed by the array elements.

Warning

Statically-sized memory arrays do not have a length field, but it might be added later to allow better convertibility between statically and dynamically-sized arrays; so, do not rely on this.

### Memory Safety[](#memory-safety "Permalink to this heading")

Without the use of inline assembly, the compiler can rely on memory to remain in a well-defined state at all times. This is especially relevant for [the new code generation pipeline via Yul IR](ir-breaking-changes.html#ir-breaking-changes): this code generation path can move local variables from stack to memory to avoid stack-too-deep errors and perform additional memory optimizations, if it can rely on certain assumptions about memory use.

While we recommend to always respect Solidity’s memory model, inline assembly allows you to use memory in an incompatible way. Therefore, moving stack variables to memory and additional memory optimizations are, by default, globally disabled in the presence of any inline assembly block that contains a memory operation or assigns to Solidity variables in memory.

However, you can specifically annotate an assembly block to indicate that it in fact respects Solidity’s memory model as follows:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=YXNzZW1ibHkgKCJtZW1vcnktc2FmZSIpIHsKICAgIC4uLgp9)

assembly ("memory-safe") {
    ...
}

In particular, a memory-safe assembly block may only access the following memory ranges:

- Memory allocated by yourself using a mechanism like the `allocate` function described above.
    
- Memory allocated by Solidity, e.g. memory within the bounds of a memory array you reference.
    
- The scratch space between memory offset 0 and 64 mentioned above.
    
- Temporary memory that is located _after_ the value of the free memory pointer at the beginning of the assembly block, i.e. memory that is “allocated” at the free memory pointer without updating the free memory pointer.
    

Furthermore, if the assembly block assigns to Solidity variables in memory, you need to assure that accesses to the Solidity variables only access these memory ranges.

Since this is mainly about the optimizer, these restrictions still need to be followed, even if the assembly block reverts or terminates. As an example, the following assembly snippet is not memory safe, because the value of `returndatasize()` may exceed the 64 byte scratch space:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=YXNzZW1ibHkgewogIHJldHVybmRhdGFjb3B5KDAsIDAsIHJldHVybmRhdGFzaXplKCkpCiAgcmV2ZXJ0KDAsIHJldHVybmRhdGFzaXplKCkpCn0=)

assembly {
  returndatacopy(0, 0, returndatasize())
  revert(0, returndatasize())
}

On the other hand, the following code _is_ memory safe, because memory beyond the location pointed to by the free memory pointer can safely be used as temporary scratch space:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=YXNzZW1ibHkgKCJtZW1vcnktc2FmZSIpIHsKICBsZXQgcCA6PSBtbG9hZCgweDQwKQogIHJldHVybmRhdGFjb3B5KHAsIDAsIHJldHVybmRhdGFzaXplKCkpCiAgcmV2ZXJ0KHAsIHJldHVybmRhdGFzaXplKCkpCn0=)

assembly ("memory-safe") {
  let p := mload(0x40)
  returndatacopy(p, 0, returndatasize())
  revert(p, returndatasize())
}

Note that you do not need to update the free memory pointer if there is no following allocation, but you can only use memory starting from the current offset given by the free memory pointer.

If the memory operations use a length of zero, it is also fine to just use any offset (not only if it falls into the scratch space):

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=YXNzZW1ibHkgKCJtZW1vcnktc2FmZSIpIHsKICByZXZlcnQoMCwgMCkKfQ==)

assembly ("memory-safe") {
  revert(0, 0)
}

Note that not only memory operations in inline assembly itself can be memory-unsafe, but also assignments to Solidity variables of reference type in memory. For example the following is not memory-safe:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ynl0ZXMgbWVtb3J5IHg7CmFzc2VtYmx5IHsKICB4IDo9IDB4NDAKfQp4WzB4MjBdID0gMHg0Mjs=)

bytes memory x;
assembly {
  x := 0x40
}
x[0x20] = 0x42;

Inline assembly that neither involves any operations that access memory nor assigns to any Solidity variables in memory is automatically considered memory-safe and does not need to be annotated.

Warning

It is your responsibility to make sure that the assembly actually satisfies the memory model. If you annotate an assembly block as memory-safe, but violate one of the memory assumptions, this **will** lead to incorrect and undefined behavior that cannot easily be discovered by testing.

In case you are developing a library that is meant to be compatible across multiple versions of Solidity, you can use a special comment to annotate an assembly block as memory-safe:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8vIEBzb2xpZGl0eSBtZW1vcnktc2FmZS1hc3NlbWJseQphc3NlbWJseSB7CiAgICAuLi4KfQ==)

/// @solidity memory-safe-assembly
assembly {
    ...
}

Note that we will disallow the annotation via comment in a future breaking release; so, if you are not concerned with backward-compatibility with older compiler versions, prefer using the dialect string.

[Previous](contracts.html "Contracts") [Next](cheatsheet.html "Cheatsheet")

---

© Copyright 2016-2023, The Solidity Authors. Revision `1acebf78`.

Customized with ❤️ by the [ethereum.org](https://ethereum.org/) team.

[Credits and attribution](credits-and-attribution.html).