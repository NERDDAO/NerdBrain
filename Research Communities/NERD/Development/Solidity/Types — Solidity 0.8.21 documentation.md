[![Solidity logo](https://docs.soliditylang.org/en/v0.8.21/types.html_static/img/logo.svg)](https://soliditylang.org)[{ skip to content }](#content)

[Blog](https://soliditylang.org/blog)[Documentation](/)[Use cases](https://soliditylang.org/use-cases)[Contribute](/en/latest/contributing.html)[About](https://soliditylang.org/about)[Forum](https://forum.soliditylang.org/)

![Color mode toggle icon](https://docs.soliditylang.org/en/v0.8.21/types.html_static/img/moon.svg)![Toggle menu](https://docs.soliditylang.org/en/v0.8.21/types.html_static/img/hamburger-light.svg)

v0.8.21

  

Basics

- [Introduction to Smart Contracts](introduction-to-smart-contracts.html)
- [Solidity by Example](solidity-by-example.html)
- [Installing the Solidity Compiler](installing-solidity.html)

Language Description

- [Layout of a Solidity Source File](layout-of-source-files.html)
- [Structure of a Contract](structure-of-a-contract.html)
- [Types](#)
    - [Value Types](#value-types)
        - [Booleans](#booleans)
        - [Integers](#integers)
            - [Comparisons](#comparisons)
            - [Bit operations](#bit-operations)
            - [Shifts](#shifts)
            - [Addition, Subtraction and Multiplication](#addition-subtraction-and-multiplication)
            - [Division](#division)
            - [Modulo](#modulo)
            - [Exponentiation](#exponentiation)
        - [Fixed Point Numbers](#fixed-point-numbers)
        - [Address](#address)
            - [Members of Addresses](#members-of-addresses)
        - [Contract Types](#contract-types)
        - [Fixed-size byte arrays](#fixed-size-byte-arrays)
        - [Dynamically-sized byte array](#dynamically-sized-byte-array)
        - [Address Literals](#address-literals)
        - [Rational and Integer Literals](#rational-and-integer-literals)
        - [String Literals and Types](#string-literals-and-types)
        - [Unicode Literals](#unicode-literals)
        - [Hexadecimal Literals](#hexadecimal-literals)
        - [Enums](#enums)
        - [User-defined Value Types](#user-defined-value-types)
        - [Function Types](#function-types)
    - [Reference Types](#reference-types)
        - [Data location](#data-location)
            - [Data location and assignment behavior](#data-location-and-assignment-behavior)
        - [Arrays](#arrays)
            - [`bytes` and `string` as Arrays](#bytes-and-string-as-arrays)
            - [The functions `bytes.concat` and `string.concat`](#the-functions-bytes-concat-and-string-concat)
            - [Allocating Memory Arrays](#allocating-memory-arrays)
            - [Array Literals](#array-literals)
            - [Array Members](#array-members)
            - [Dangling References to Storage Array Elements](#dangling-references-to-storage-array-elements)
        - [Array Slices](#array-slices)
        - [Structs](#structs)
    - [Mapping Types](#mapping-types)
        - [Iterable Mappings](#iterable-mappings)
    - [Operators](#operators)
        - [Ternary Operator](#ternary-operator)
        - [Compound and Increment/Decrement Operators](#compound-and-increment-decrement-operators)
        - [delete](#delete)
        - [Order of Precedence of Operators](#order-of-precedence-of-operators)
    - [Conversions between Elementary Types](#conversions-between-elementary-types)
        - [Implicit Conversions](#implicit-conversions)
        - [Explicit Conversions](#explicit-conversions)
    - [Conversions between Literals and Elementary Types](#conversions-between-literals-and-elementary-types)
        - [Integer Types](#integer-types)
        - [Fixed-Size Byte Arrays](#index-34)
        - [Addresses](#addresses)
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

[en](https://docs.soliditylang.org/en/v0.8.21/types.html)

[zh](https://docs.soliditylang.org/zh/v0.8.19/types.html)

[fr](https://docs.soliditylang.org/fr/latest/types.html)

[tr](https://docs.soliditylang.org/tr/v0.8.16/types.html)

Versions

[latest](https://docs.soliditylang.org/en/latest/types.html)

[stable](https://docs.soliditylang.org/en/stable/types.html)

[v0.8.21](https://docs.soliditylang.org/en/v0.8.21/types.html)

[v0.8.20](https://docs.soliditylang.org/en/v0.8.20/types.html)

[v0.8.19](https://docs.soliditylang.org/en/v0.8.19/types.html)

[v0.8.18](https://docs.soliditylang.org/en/v0.8.18/types.html)

[v0.8.17](https://docs.soliditylang.org/en/v0.8.17/types.html)

[v0.8.16](https://docs.soliditylang.org/en/v0.8.16/types.html)

[v0.8.15](https://docs.soliditylang.org/en/v0.8.15/types.html)

[v0.8.14](https://docs.soliditylang.org/en/v0.8.14/types.html)

[v0.8.13](https://docs.soliditylang.org/en/v0.8.13/types.html)

[v0.8.12](https://docs.soliditylang.org/en/v0.8.12/types.html)

[v0.8.11](https://docs.soliditylang.org/en/v0.8.11/types.html)

[v0.8.10](https://docs.soliditylang.org/en/v0.8.10/types.html)

[v0.8.9](https://docs.soliditylang.org/en/v0.8.9/types.html)

[v0.8.8](https://docs.soliditylang.org/en/v0.8.8/types.html)

[v0.8.7](https://docs.soliditylang.org/en/v0.8.7/types.html)

[v0.8.6](https://docs.soliditylang.org/en/v0.8.6/types.html)

[v0.8.5](https://docs.soliditylang.org/en/v0.8.5/types.html)

[v0.8.4](https://docs.soliditylang.org/en/v0.8.4/types.html)

[v0.8.3](https://docs.soliditylang.org/en/v0.8.3/types.html)

[v0.8.2](https://docs.soliditylang.org/en/v0.8.2/types.html)

[v0.8.1](https://docs.soliditylang.org/en/v0.8.1/types.html)

[v0.8.0](https://docs.soliditylang.org/en/v0.8.0/types.html)

[v0.7.6](https://docs.soliditylang.org/en/v0.7.6/types.html)

[v0.7.5](https://docs.soliditylang.org/en/v0.7.5/types.html)

[v0.7.4](https://docs.soliditylang.org/en/v0.7.4/types.html)

[v0.7.3](https://docs.soliditylang.org/en/v0.7.3/types.html)

[v0.7.2](https://docs.soliditylang.org/en/v0.7.2/types.html)

[v0.7.1](https://docs.soliditylang.org/en/v0.7.1/types.html)

[v0.7.0](https://docs.soliditylang.org/en/v0.7.0/types.html)

[v0.6.12](https://docs.soliditylang.org/en/v0.6.12/types.html)

[v0.6.11](https://docs.soliditylang.org/en/v0.6.11/types.html)

[v0.6.10](https://docs.soliditylang.org/en/v0.6.10/types.html)

[v0.6.9](https://docs.soliditylang.org/en/v0.6.9/types.html)

[v0.6.8](https://docs.soliditylang.org/en/v0.6.8/types.html)

[v0.6.7](https://docs.soliditylang.org/en/v0.6.7/types.html)

[v0.6.6](https://docs.soliditylang.org/en/v0.6.6/types.html)

[v0.6.5](https://docs.soliditylang.org/en/v0.6.5/types.html)

[v0.6.4](https://docs.soliditylang.org/en/v0.6.4/types.html)

[v0.6.3](https://docs.soliditylang.org/en/v0.6.3/types.html)

[v0.6.2](https://docs.soliditylang.org/en/v0.6.2/types.html)

[v0.6.1](https://docs.soliditylang.org/en/v0.6.1/types.html)

[v0.6.0](https://docs.soliditylang.org/en/v0.6.0/types.html)

[v0.5.17](https://docs.soliditylang.org/en/v0.5.17/types.html)

[v0.5.16](https://docs.soliditylang.org/en/v0.5.16/types.html)

[v0.5.15](https://docs.soliditylang.org/en/v0.5.15/types.html)

[v0.5.14](https://docs.soliditylang.org/en/v0.5.14/types.html)

[v0.5.13](https://docs.soliditylang.org/en/v0.5.13/types.html)

[v0.5.12](https://docs.soliditylang.org/en/v0.5.12/types.html)

[v0.5.11](https://docs.soliditylang.org/en/v0.5.11/types.html)

[v0.5.10](https://docs.soliditylang.org/en/v0.5.10/types.html)

[v0.5.9](https://docs.soliditylang.org/en/v0.5.9/types.html)

[v0.5.8](https://docs.soliditylang.org/en/v0.5.8/types.html)

[v0.5.7](https://docs.soliditylang.org/en/v0.5.7/types.html)

[v0.5.6](https://docs.soliditylang.org/en/v0.5.6/types.html)

[v0.5.5](https://docs.soliditylang.org/en/v0.5.5/types.html)

[v0.5.4](https://docs.soliditylang.org/en/v0.5.4/types.html)

[v0.5.3](https://docs.soliditylang.org/en/v0.5.3/types.html)

[v0.5.2](https://docs.soliditylang.org/en/v0.5.2/types.html)

[v0.5.1](https://docs.soliditylang.org/en/v0.5.1/types.html)

[v0.5.0](https://docs.soliditylang.org/en/v0.5.0/types.html)

[v0.4.26](https://docs.soliditylang.org/en/v0.4.26/types.html)

[v0.4.25](https://docs.soliditylang.org/en/v0.4.25/types.html)

[v0.4.24](https://docs.soliditylang.org/en/v0.4.24/types.html)

[v0.4.23](https://docs.soliditylang.org/en/v0.4.23/types.html)

[v0.4.22](https://docs.soliditylang.org/en/v0.4.22/types.html)

[v0.4.21](https://docs.soliditylang.org/en/v0.4.21/types.html)

[v0.4.20](https://docs.soliditylang.org/en/v0.4.20/types.html)

[v0.4.19](https://docs.soliditylang.org/en/v0.4.19/types.html)

[v0.4.18](https://docs.soliditylang.org/en/v0.4.18/types.html)

[v0.4.17](https://docs.soliditylang.org/en/v0.4.17/types.html)

[v0.4.16](https://docs.soliditylang.org/en/v0.4.16/types.html)

[v0.4.15](https://docs.soliditylang.org/en/v0.4.15/types.html)

[v0.4.14](https://docs.soliditylang.org/en/v0.4.14/types.html)

[v0.4.13](https://docs.soliditylang.org/en/v0.4.13/types.html)

[v0.4.12](https://docs.soliditylang.org/en/v0.4.12/types.html)

[v0.4.11](https://docs.soliditylang.org/en/v0.4.11/types.html)

[v0.4.10](https://docs.soliditylang.org/en/v0.4.10/types.html)

[v0.4.9](https://docs.soliditylang.org/en/v0.4.9/types.html)

[v0.4.8](https://docs.soliditylang.org/en/v0.4.8/types.html)

[v0.4.7](https://docs.soliditylang.org/en/v0.4.7/types.html)

[v0.4.6](https://docs.soliditylang.org/en/v0.4.6/types.html)

[v0.4.5](https://docs.soliditylang.org/en/v0.4.5/types.html)

[v0.4.4](https://docs.soliditylang.org/en/v0.4.4/types.html)

[v0.4.3](https://docs.soliditylang.org/en/v0.4.3/types.html)

[v0.4.2](https://docs.soliditylang.org/en/v0.4.2/types.html)

[v0.4.1](https://docs.soliditylang.org/en/v0.4.1/types.html)

[v0.4.0](https://docs.soliditylang.org/en/v0.4.0/types.html)

[v0.3.6](https://docs.soliditylang.org/en/v0.3.6/types.html)

[v0.3.5](https://docs.soliditylang.org/en/v0.3.5/types.html)

[v0.3.4](https://docs.soliditylang.org/en/v0.3.4/types.html)

[v0.3.3](https://docs.soliditylang.org/en/v0.3.3/types.html)

[v0.3.2](https://docs.soliditylang.org/en/v0.3.2/types.html)

[v0.3.1](https://docs.soliditylang.org/en/v0.3.1/types.html)

[v0.3.0](https://docs.soliditylang.org/en/v0.3.0/types.html)

[v0.2.2](https://docs.soliditylang.org/en/v0.2.2/types.html)

[v0.2.1](https://docs.soliditylang.org/en/v0.2.1/types.html)

[v0.2.0](https://docs.soliditylang.org/en/v0.2.0/types.html)

[v0.1.7](https://docs.soliditylang.org/en/v0.1.7/types.html)

[v0.1.6](https://docs.soliditylang.org/en/v0.1.6/types.html)

[v0.1.5](https://docs.soliditylang.org/en/v0.1.5/types.html)

[v0.1.4](https://docs.soliditylang.org/en/v0.1.4/types.html)

[v0.1.3](https://docs.soliditylang.org/en/v0.1.3/types.html)

[v0.1.2](https://docs.soliditylang.org/en/v0.1.2/types.html)

[develop](https://docs.soliditylang.org/en/develop/types.html)

[breaking](https://docs.soliditylang.org/en/breaking/types.html)

Downloads

[PDF](//docs.soliditylang.org/_/downloads/en/v0.8.21/pdf/)

[Epub](//docs.soliditylang.org/_/downloads/en/v0.8.21/epub/)

On Read the Docs

[Project Home](//readthedocs.org/projects/solidity/)

[Builds](//readthedocs.org/projects/solidity/builds/)

[Downloads](//readthedocs.org/projects/solidity/downloads/)

On GitHub

[View](https://github.com/ethereum/solidity/blob/v0.8.21/docs/types.rst)

Search

---

Hosted by [Read the Docs](https://readthedocs.org) · [Privacy Policy](https://docs.readthedocs.io/page/privacy-policy.html)

- [](index.html)
- Types
- [Edit on GitHub](https://github.com/ethereum/solidity/blob/v0.8.21/docs/types.rst)

---

# Types[](#types "Permalink to this heading")

Solidity is a statically typed language, which means that the type of each variable (state and local) needs to be specified. Solidity provides several elementary types which can be combined to form complex types.

In addition, types can interact with each other in expressions containing operators. For a quick reference of the various operators, see [Order of Precedence of Operators](#order).

The concept of “undefined” or “null” values does not exist in Solidity, but newly declared variables always have a [default value](control-structures.html#default-value) dependent on its type. To handle any unexpected values, you should use the [revert function](control-structures.html#assert-and-require) to revert the whole transaction, or return a tuple with a second `bool` value denoting success.

## Value Types[](#value-types "Permalink to this heading")

The following are called value types because their variables will always be passed by value, i.e. they are always copied when they are used as function arguments or in assignments.

### Booleans[](#booleans "Permalink to this heading")

`bool`: The possible values are constants `true` and `false`.

Operators:

- `!` (logical negation)
    
- `&&` (logical conjunction, “and”)
    
- `||` (logical disjunction, “or”)
    
- `==` (equality)
    
- `!=` (inequality)
    

The operators `||` and `&&` apply the common short-circuiting rules. This means that in the expression `f(x) || g(y)`, if `f(x)` evaluates to `true`, `g(y)` will not be evaluated even if it may have side-effects.

### Integers[](#integers "Permalink to this heading")

`int` / `uint`: Signed and unsigned integers of various sizes. Keywords `uint8` to `uint256` in steps of `8` (unsigned of 8 up to 256 bits) and `int8` to `int256`. `uint` and `int` are aliases for `uint256` and `int256`, respectively.

Operators:

- Comparisons: `<=`, `<`, `==`, `!=`, `>=`, `>` (evaluate to `bool`)
    
- Bit operators: `&`, `|`, `^` (bitwise exclusive or), `~` (bitwise negation)
    
- Shift operators: `<<` (left shift), `>>` (right shift)
    
- Arithmetic operators: `+`, `-`, unary `-` (only for signed integers), `*`, `/`, `%` (modulo), `**` (exponentiation)
    

For an integer type `X`, you can use `type(X).min` and `type(X).max` to access the minimum and maximum value representable by the type.

Warning

Integers in Solidity are restricted to a certain range. For example, with `uint32`, this is `0` up to `2**32 - 1`. There are two modes in which arithmetic is performed on these types: The “wrapping” or “unchecked” mode and the “checked” mode. By default, arithmetic is always “checked”, meaning that if an operation’s result falls outside the value range of the type, the call is reverted through a [failing assertion](control-structures.html#assert-and-require). You can switch to “unchecked” mode using `unchecked { ... }`. More details can be found in the section about [unchecked](control-structures.html#unchecked).

#### Comparisons[](#comparisons "Permalink to this heading")

The value of a comparison is the one obtained by comparing the integer value.

#### Bit operations[](#bit-operations "Permalink to this heading")

Bit operations are performed on the two’s complement representation of the number. This means that, for example `~int256(0) == int256(-1)`.

#### Shifts[](#shifts "Permalink to this heading")

The result of a shift operation has the type of the left operand, truncating the result to match the type. The right operand must be of unsigned type, trying to shift by a signed type will produce a compilation error.

Shifts can be “simulated” using multiplication by powers of two in the following way. Note that the truncation to the type of the left operand is always performed at the end, but not mentioned explicitly.

- `x << y` is equivalent to the mathematical expression `x * 2**y`.
    
- `x >> y` is equivalent to the mathematical expression `x / 2**y`, rounded towards negative infinity.
    

Warning

Before version `0.5.0` a right shift `x >> y` for negative `x` was equivalent to the mathematical expression `x / 2**y` rounded towards zero, i.e., right shifts used rounding up (towards zero) instead of rounding down (towards negative infinity).

Note

Overflow checks are never performed for shift operations as they are done for arithmetic operations. Instead, the result is always truncated.

#### Addition, Subtraction and Multiplication[](#addition-subtraction-and-multiplication "Permalink to this heading")

Addition, subtraction and multiplication have the usual semantics, with two different modes in regard to over- and underflow:

By default, all arithmetic is checked for under- or overflow, but this can be disabled using the [unchecked block](control-structures.html#unchecked), resulting in wrapping arithmetic. More details can be found in that section.

The expression `-x` is equivalent to `(T(0) - x)` where `T` is the type of `x`. It can only be applied to signed types. The value of `-x` can be positive if `x` is negative. There is another caveat also resulting from two’s complement representation:

If you have `int x = type(int).min;`, then `-x` does not fit the positive range. This means that `unchecked { assert(-x == x); }` works, and the expression `-x` when used in checked mode will result in a failing assertion.

#### Division[](#division "Permalink to this heading")

Since the type of the result of an operation is always the type of one of the operands, division on integers always results in an integer. In Solidity, division rounds towards zero. This means that `int256(-5) / int256(2) == int256(-2)`.

Note that in contrast, division on [literals](#rational-literals) results in fractional values of arbitrary precision.

Note

Division by zero causes a [Panic error](control-structures.html#assert-and-require). This check can **not** be disabled through `unchecked { ... }`.

Note

The expression `type(int).min / (-1)` is the only case where division causes an overflow. In checked arithmetic mode, this will cause a failing assertion, while in wrapping mode, the value will be `type(int).min`.

#### Modulo[](#modulo "Permalink to this heading")

The modulo operation `a % n` yields the remainder `r` after the division of the operand `a` by the operand `n`, where `q = int(a / n)` and `r = a - (n * q)`. This means that modulo results in the same sign as its left operand (or zero) and `a % n == -(-a % n)` holds for negative `a`:

- `int256(5) % int256(2) == int256(1)`
    
- `int256(5) % int256(-2) == int256(1)`
    
- `int256(-5) % int256(2) == int256(-1)`
    
- `int256(-5) % int256(-2) == int256(-1)`
    

Note

Modulo with zero causes a [Panic error](control-structures.html#assert-and-require). This check can **not** be disabled through `unchecked { ... }`.

#### Exponentiation[](#exponentiation "Permalink to this heading")

Exponentiation is only available for unsigned types in the exponent. The resulting type of an exponentiation is always equal to the type of the base. Please take care that it is large enough to hold the result and prepare for potential assertion failures or wrapping behavior.

Note

In checked mode, exponentiation only uses the comparatively cheap `exp` opcode for small bases. For the cases of `x**3`, the expression `x*x*x` might be cheaper. In any case, gas cost tests and the use of the optimizer are advisable.

Note

Note that `0**0` is defined by the EVM as `1`.

### Fixed Point Numbers[](#fixed-point-numbers "Permalink to this heading")

Warning

Fixed point numbers are not fully supported by Solidity yet. They can be declared, but cannot be assigned to or from.

`fixed` / `ufixed`: Signed and unsigned fixed point number of various sizes. Keywords `ufixedMxN` and `fixedMxN`, where `M` represents the number of bits taken by the type and `N` represents how many decimal points are available. `M` must be divisible by 8 and goes from 8 to 256 bits. `N` must be between 0 and 80, inclusive. `ufixed` and `fixed` are aliases for `ufixed128x18` and `fixed128x18`, respectively.

Operators:

- Comparisons: `<=`, `<`, `==`, `!=`, `>=`, `>` (evaluate to `bool`)
    
- Arithmetic operators: `+`, `-`, unary `-`, `*`, `/`, `%` (modulo)
    

Note

The main difference between floating point (`float` and `double` in many languages, more precisely IEEE 754 numbers) and fixed point numbers is that the number of bits used for the integer and the fractional part (the part after the decimal dot) is flexible in the former, while it is strictly defined in the latter. Generally, in floating point almost the entire space is used to represent the number, while only a small number of bits define where the decimal point is.

### Address[](#address "Permalink to this heading")

The address type comes in two largely identical flavors:

- `address`: Holds a 20 byte value (size of an Ethereum address).
    
- `address payable`: Same as `address`, but with the additional members `transfer` and `send`.
    

The idea behind this distinction is that `address payable` is an address you can send Ether to, while you are not supposed to send Ether to a plain `address`, for example because it might be a smart contract that was not built to accept Ether.

Type conversions:

Implicit conversions from `address payable` to `address` are allowed, whereas conversions from `address` to `address payable` must be explicit via `payable(<address>)`.

Explicit conversions to and from `address` are allowed for `uint160`, integer literals, `bytes20` and contract types.

Only expressions of type `address` and contract-type can be converted to the type `address payable` via the explicit conversion `payable(...)`. For contract-type, this conversion is only allowed if the contract can receive Ether, i.e., the contract either has a [receive](contracts.html#receive-ether-function) or a payable fallback function. Note that `payable(0)` is valid and is an exception to this rule.

Note

If you need a variable of type `address` and plan to send Ether to it, then declare its type as `address payable` to make this requirement visible. Also, try to make this distinction or conversion as early as possible.

The distinction between `address` and `address payable` was introduced with version 0.5.0. Also starting from that version, contracts are not implicitly convertible to the `address` type, but can still be explicitly converted to `address` or to `address payable`, if they have a receive or payable fallback function.

Operators:

- `<=`, `<`, `==`, `!=`, `>=` and `>`
    

Warning

If you convert a type that uses a larger byte size to an `address`, for example `bytes32`, then the `address` is truncated. To reduce conversion ambiguity, starting with version 0.4.24, the compiler will force you to make the truncation explicit in the conversion. Take for example the 32-byte value `0x111122223333444455556666777788889999AAAABBBBCCCCDDDDEEEEFFFFCCCC`.

You can use `address(uint160(bytes20(b)))`, which results in `0x111122223333444455556666777788889999aAaa`, or you can use `address(uint160(uint256(b)))`, which results in `0x777788889999AaAAbBbbCcccddDdeeeEfFFfCcCc`.

Note

Mixed-case hexadecimal numbers conforming to [EIP-55](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-55.md) are automatically treated as literals of the `address` type. See [Address Literals](#address-literals).

#### Members of Addresses[](#members-of-addresses "Permalink to this heading")

For a quick reference of all members of address, see [Members of Address Types](units-and-global-variables.html#address-related).

- `balance` and `transfer`
    

It is possible to query the balance of an address using the property `balance` and to send Ether (in units of wei) to a payable address using the `transfer` function:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=YWRkcmVzcyBwYXlhYmxlIHggPSBwYXlhYmxlKDB4MTIzKTsKYWRkcmVzcyBteUFkZHJlc3MgPSBhZGRyZXNzKHRoaXMpOwppZiAoeC5iYWxhbmNlIDwgMTAgJiYgbXlBZGRyZXNzLmJhbGFuY2UgPj0gMTApIHgudHJhbnNmZXIoMTApOw==)

address payable x = payable(0x123);
address myAddress = address(this);
if (x.balance < 10 && myAddress.balance >= 10) x.transfer(10);

The `transfer` function fails if the balance of the current contract is not large enough or if the Ether transfer is rejected by the receiving account. The `transfer` function reverts on failure.

Note

If `x` is a contract address, its code (more specifically: its [Receive Ether Function](contracts.html#receive-ether-function), if present, or otherwise its [Fallback Function](contracts.html#fallback-function), if present) will be executed together with the `transfer` call (this is a feature of the EVM and cannot be prevented). If that execution runs out of gas or fails in any way, the Ether transfer will be reverted and the current contract will stop with an exception.

- `send`
    

`send` is the low-level counterpart of `transfer`. If the execution fails, the current contract will not stop with an exception, but `send` will return `false`.

Warning

There are some dangers in using `send`: The transfer fails if the call stack depth is at 1024 (this can always be forced by the caller) and it also fails if the recipient runs out of gas. So in order to make safe Ether transfers, always check the return value of `send`, use `transfer` or even better: use a pattern where the recipient withdraws the Ether.

- `call`, `delegatecall` and `staticcall`
    

In order to interface with contracts that do not adhere to the ABI, or to get more direct control over the encoding, the functions `call`, `delegatecall` and `staticcall` are provided. They all take a single `bytes memory` parameter and return the success condition (as a `bool`) and the returned data (`bytes memory`). The functions `abi.encode`, `abi.encodePacked`, `abi.encodeWithSelector` and `abi.encodeWithSignature` can be used to encode structured data.

Example:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ynl0ZXMgbWVtb3J5IHBheWxvYWQgPSBhYmkuZW5jb2RlV2l0aFNpZ25hdHVyZSgicmVnaXN0ZXIoc3RyaW5nKSIsICJNeU5hbWUiKTsKKGJvb2wgc3VjY2VzcywgYnl0ZXMgbWVtb3J5IHJldHVybkRhdGEpID0gYWRkcmVzcyhuYW1lUmVnKS5jYWxsKHBheWxvYWQpOwpyZXF1aXJlKHN1Y2Nlc3MpOw==)

bytes memory payload = abi.encodeWithSignature("register(string)", "MyName");
(bool success, bytes memory returnData) = address(nameReg).call(payload);
require(success);

Warning

All these functions are low-level functions and should be used with care. Specifically, any unknown contract might be malicious and if you call it, you hand over control to that contract which could in turn call back into your contract, so be prepared for changes to your state variables when the call returns. The regular way to interact with other contracts is to call a function on a contract object (`x.f()`).

Note

Previous versions of Solidity allowed these functions to receive arbitrary arguments and would also handle a first argument of type `bytes4` differently. These edge cases were removed in version 0.5.0.

It is possible to adjust the supplied gas with the `gas` modifier:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=YWRkcmVzcyhuYW1lUmVnKS5jYWxse2dhczogMTAwMDAwMH0oYWJpLmVuY29kZVdpdGhTaWduYXR1cmUoInJlZ2lzdGVyKHN0cmluZykiLCAiTXlOYW1lIikpOw==)

address(nameReg).call{gas: 1000000}(abi.encodeWithSignature("register(string)", "MyName"));

Similarly, the supplied Ether value can be controlled too:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=YWRkcmVzcyhuYW1lUmVnKS5jYWxse3ZhbHVlOiAxIGV0aGVyfShhYmkuZW5jb2RlV2l0aFNpZ25hdHVyZSgicmVnaXN0ZXIoc3RyaW5nKSIsICJNeU5hbWUiKSk7)

address(nameReg).call{value: 1 ether}(abi.encodeWithSignature("register(string)", "MyName"));

Lastly, these modifiers can be combined. Their order does not matter:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=YWRkcmVzcyhuYW1lUmVnKS5jYWxse2dhczogMTAwMDAwMCwgdmFsdWU6IDEgZXRoZXJ9KGFiaS5lbmNvZGVXaXRoU2lnbmF0dXJlKCJyZWdpc3RlcihzdHJpbmcpIiwgIk15TmFtZSIpKTs=)

address(nameReg).call{gas: 1000000, value: 1 ether}(abi.encodeWithSignature("register(string)", "MyName"));

In a similar way, the function `delegatecall` can be used: the difference is that only the code of the given address is used, all other aspects (storage, balance, …) are taken from the current contract. The purpose of `delegatecall` is to use library code which is stored in another contract. The user has to ensure that the layout of storage in both contracts is suitable for delegatecall to be used.

Note

Prior to homestead, only a limited variant called `callcode` was available that did not provide access to the original `msg.sender` and `msg.value` values. This function was removed in version 0.5.0.

Since byzantium `staticcall` can be used as well. This is basically the same as `call`, but will revert if the called function modifies the state in any way.

All three functions `call`, `delegatecall` and `staticcall` are very low-level functions and should only be used as a _last resort_ as they break the type-safety of Solidity.

The `gas` option is available on all three methods, while the `value` option is only available on `call`.

Note

It is best to avoid relying on hardcoded gas values in your smart contract code, regardless of whether state is read from or written to, as this can have many pitfalls. Also, access to gas might change in the future.

- `code` and `codehash`
    

You can query the deployed code for any smart contract. Use `.code` to get the EVM bytecode as a `bytes memory`, which might be empty. Use `.codehash` to get the Keccak-256 hash of that code (as a `bytes32`). Note that `addr.codehash` is cheaper than using `keccak256(addr.code)`.

Note

All contracts can be converted to `address` type, so it is possible to query the balance of the current contract using `address(this).balance`.

### Contract Types[](#contract-types "Permalink to this heading")

Every [contract](contracts.html#contracts) defines its own type. You can implicitly convert contracts to contracts they inherit from. Contracts can be explicitly converted to and from the `address` type.

Explicit conversion to and from the `address payable` type is only possible if the contract type has a receive or payable fallback function. The conversion is still performed using `address(x)`. If the contract type does not have a receive or payable fallback function, the conversion to `address payable` can be done using `payable(address(x))`. You can find more information in the section about the [address type](#address).

Note

Before version 0.5.0, contracts directly derived from the address type and there was no distinction between `address` and `address payable`.

If you declare a local variable of contract type (`MyContract c`), you can call functions on that contract. Take care to assign it from somewhere that is the same contract type.

You can also instantiate contracts (which means they are newly created). You can find more details in the [‘Contracts via new’](control-structures.html#creating-contracts) section.

The data representation of a contract is identical to that of the `address` type and this type is also used in the [ABI](abi-spec.html#abi).

Contracts do not support any operators.

The members of contract types are the external functions of the contract including any state variables marked as `public`.

For a contract `C` you can use `type(C)` to access [type information](units-and-global-variables.html#meta-type) about the contract.

### Fixed-size byte arrays[](#fixed-size-byte-arrays "Permalink to this heading")

The value types `bytes1`, `bytes2`, `bytes3`, …, `bytes32` hold a sequence of bytes from one to up to 32.

Operators:

- Comparisons: `<=`, `<`, `==`, `!=`, `>=`, `>` (evaluate to `bool`)
    
- Bit operators: `&`, `|`, `^` (bitwise exclusive or), `~` (bitwise negation)
    
- Shift operators: `<<` (left shift), `>>` (right shift)
    
- Index access: If `x` is of type `bytesI`, then `x[k]` for `0 <= k < I` returns the `k` th byte (read-only).
    

The shifting operator works with unsigned integer type as right operand (but returns the type of the left operand), which denotes the number of bits to shift by. Shifting by a signed type will produce a compilation error.

Members:

- `.length` yields the fixed length of the byte array (read-only).
    

Note

The type `bytes1[]` is an array of bytes, but due to padding rules, it wastes 31 bytes of space for each element (except in storage). It is better to use the `bytes` type instead.

Note

Prior to version 0.8.0, `byte` used to be an alias for `bytes1`.

### Dynamically-sized byte array[](#dynamically-sized-byte-array "Permalink to this heading")

`bytes`:

Dynamically-sized byte array, see [Arrays](#arrays). Not a value-type!

`string`:

Dynamically-sized UTF-8-encoded string, see [Arrays](#arrays). Not a value-type!

### Address Literals[](#address-literals "Permalink to this heading")

Hexadecimal literals that pass the address checksum test, for example `0xdCad3a6d3569DF655070DEd06cb7A1b2Ccd1D3AF` are of `address` type. Hexadecimal literals that are between 39 and 41 digits long and do not pass the checksum test produce an error. You can prepend (for integer types) or append (for bytesNN types) zeros to remove the error.

Note

The mixed-case address checksum format is defined in [EIP-55](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-55.md).

### Rational and Integer Literals[](#rational-and-integer-literals "Permalink to this heading")

Integer literals are formed from a sequence of digits in the range 0-9. They are interpreted as decimals. For example, `69` means sixty nine. Octal literals do not exist in Solidity and leading zeros are invalid.

Decimal fractional literals are formed by a `.` with at least one number after the decimal point. Examples include `.1` and `1.3` (but not `1.`).

Scientific notation in the form of `2e10` is also supported, where the mantissa can be fractional but the exponent has to be an integer. The literal `MeE` is equivalent to `M * 10**E`. Examples include `2e10`, `-2e10`, `2e-10`, `2.5e1`.

Underscores can be used to separate the digits of a numeric literal to aid readability. For example, decimal `123_000`, hexadecimal `0x2eff_abde`, scientific decimal notation `1_2e345_678` are all valid. Underscores are only allowed between two digits and only one consecutive underscore is allowed. There is no additional semantic meaning added to a number literal containing underscores, the underscores are ignored.

Number literal expressions retain arbitrary precision until they are converted to a non-literal type (i.e. by using them together with anything other than a number literal expression (like boolean literals) or by explicit conversion). This means that computations do not overflow and divisions do not truncate in number literal expressions.

For example, `(2**800 + 1) - 2**800` results in the constant `1` (of type `uint8`) although intermediate results would not even fit the machine word size. Furthermore, `.5 * 8` results in the integer `4` (although non-integers were used in between).

Warning

While most operators produce a literal expression when applied to literals, there are certain operators that do not follow this pattern:

- Ternary operator (`... ? ... : ...`),
    
- Array subscript (`<array>[<index>]`).
    

You might expect expressions like `255 + (true ? 1 : 0)` or `255 + [1, 2, 3][0]` to be equivalent to using the literal 256 directly, but in fact they are computed within the type `uint8` and can overflow.

Any operator that can be applied to integers can also be applied to number literal expressions as long as the operands are integers. If any of the two is fractional, bit operations are disallowed and exponentiation is disallowed if the exponent is fractional (because that might result in a non-rational number).

Shifts and exponentiation with literal numbers as left (or base) operand and integer types as the right (exponent) operand are always performed in the `uint256` (for non-negative literals) or `int256` (for a negative literals) type, regardless of the type of the right (exponent) operand.

Warning

Division on integer literals used to truncate in Solidity prior to version 0.4.0, but it now converts into a rational number, i.e. `5 / 2` is not equal to `2`, but to `2.5`.

Note

Solidity has a number literal type for each rational number. Integer literals and rational number literals belong to number literal types. Moreover, all number literal expressions (i.e. the expressions that contain only number literals and operators) belong to number literal types. So the number literal expressions `1 + 2` and `2 + 1` both belong to the same number literal type for the rational number three.

Note

Number literal expressions are converted into a non-literal type as soon as they are used with non-literal expressions. Disregarding types, the value of the expression assigned to `b` below evaluates to an integer. Because `a` is of type `uint128`, the expression `2.5 + a` has to have a proper type, though. Since there is no common type for the type of `2.5` and `uint128`, the Solidity compiler does not accept this code.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=dWludDEyOCBhID0gMTsKdWludDEyOCBiID0gMi41ICsgYSArIDAuNTs=)

uint128 a = 1;
uint128 b = 2.5 + a + 0.5;

### String Literals and Types[](#string-literals-and-types "Permalink to this heading")

String literals are written with either double or single-quotes (`"foo"` or `'bar'`), and they can also be split into multiple consecutive parts (`"foo" "bar"` is equivalent to `"foobar"`) which can be helpful when dealing with long strings. They do not imply trailing zeroes as in C; `"foo"` represents three bytes, not four. As with integer literals, their type can vary, but they are implicitly convertible to `bytes1`, …, `bytes32`, if they fit, to `bytes` and to `string`.

For example, with `bytes32 samevar = "stringliteral"` the string literal is interpreted in its raw byte form when assigned to a `bytes32` type.

String literals can only contain printable ASCII characters, which means the characters between and including 0x20 .. 0x7E.

Additionally, string literals also support the following escape characters:

- `\<newline>` (escapes an actual newline)
    
- `\\` (backslash)
    
- `\'` (single quote)
    
- `\"` (double quote)
    
- `\n` (newline)
    
- `\r` (carriage return)
    
- `\t` (tab)
    
- `\xNN` (hex escape, see below)
    
- `\uNNNN` (unicode escape, see below)
    

`\xNN` takes a hex value and inserts the appropriate byte, while `\uNNNN` takes a Unicode codepoint and inserts an UTF-8 sequence.

Note

Until version 0.8.0 there were three additional escape sequences: `\b`, `\f` and `\v`. They are commonly available in other languages but rarely needed in practice. If you do need them, they can still be inserted via hexadecimal escapes, i.e. `\x08`, `\x0c` and `\x0b`, respectively, just as any other ASCII character.

The string in the following example has a length of ten bytes. It starts with a newline byte, followed by a double quote, a single quote a backslash character and then (without separator) the character sequence `abcdef`.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=IlxuXCJcJ1xcYWJjXApkZWYi)

"\n\"\'\\abc\
def"

Any Unicode line terminator which is not a newline (i.e. LF, VF, FF, CR, NEL, LS, PS) is considered to terminate the string literal. Newline only terminates the string literal if it is not preceded by a `\`.

### Unicode Literals[](#unicode-literals "Permalink to this heading")

While regular string literals can only contain ASCII, Unicode literals – prefixed with the keyword `unicode` – can contain any valid UTF-8 sequence. They also support the very same escape sequences as regular string literals.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=c3RyaW5nIG1lbW9yeSBhID0gdW5pY29kZSJIZWxsbyDwn5iDIjs=)

string memory a = unicode"Hello 😃";

### Hexadecimal Literals[](#hexadecimal-literals "Permalink to this heading")

Hexadecimal literals are prefixed with the keyword `hex` and are enclosed in double or single-quotes (`hex"001122FF"`, `hex'0011_22_FF'`). Their content must be hexadecimal digits which can optionally use a single underscore as separator between byte boundaries. The value of the literal will be the binary representation of the hexadecimal sequence.

Multiple hexadecimal literals separated by whitespace are concatenated into a single literal: `hex"00112233" hex"44556677"` is equivalent to `hex"0011223344556677"`

Hexadecimal literals in some ways behave like [string literals](#string-literals) but are not implicitly convertible to the `string` type.

### Enums[](#enums "Permalink to this heading")

Enums are one way to create a user-defined type in Solidity. They are explicitly convertible to and from all integer types but implicit conversion is not allowed. The explicit conversion from integer checks at runtime that the value lies inside the range of the enum and causes a [Panic error](control-structures.html#assert-and-require) otherwise. Enums require at least one member, and its default value when declared is the first member. Enums cannot have more than 256 members.

The data representation is the same as for enums in C: The options are represented by subsequent unsigned integer values starting from `0`.

Using `type(NameOfEnum).min` and `type(NameOfEnum).max` you can get the smallest and respectively largest value of the given enum.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguODsKCmNvbnRyYWN0IHRlc3QgewogICAgZW51bSBBY3Rpb25DaG9pY2VzIHsgR29MZWZ0LCBHb1JpZ2h0LCBHb1N0cmFpZ2h0LCBTaXRTdGlsbCB9CiAgICBBY3Rpb25DaG9pY2VzIGNob2ljZTsKICAgIEFjdGlvbkNob2ljZXMgY29uc3RhbnQgZGVmYXVsdENob2ljZSA9IEFjdGlvbkNob2ljZXMuR29TdHJhaWdodDsKCiAgICBmdW5jdGlvbiBzZXRHb1N0cmFpZ2h0KCkgcHVibGljIHsKICAgICAgICBjaG9pY2UgPSBBY3Rpb25DaG9pY2VzLkdvU3RyYWlnaHQ7CiAgICB9CgogICAgLy8gU2luY2UgZW51bSB0eXBlcyBhcmUgbm90IHBhcnQgb2YgdGhlIEFCSSwgdGhlIHNpZ25hdHVyZSBvZiAiZ2V0Q2hvaWNlIgogICAgLy8gd2lsbCBhdXRvbWF0aWNhbGx5IGJlIGNoYW5nZWQgdG8gImdldENob2ljZSgpIHJldHVybnMgKHVpbnQ4KSIKICAgIC8vIGZvciBhbGwgbWF0dGVycyBleHRlcm5hbCB0byBTb2xpZGl0eS4KICAgIGZ1bmN0aW9uIGdldENob2ljZSgpIHB1YmxpYyB2aWV3IHJldHVybnMgKEFjdGlvbkNob2ljZXMpIHsKICAgICAgICByZXR1cm4gY2hvaWNlOwogICAgfQoKICAgIGZ1bmN0aW9uIGdldERlZmF1bHRDaG9pY2UoKSBwdWJsaWMgcHVyZSByZXR1cm5zICh1aW50KSB7CiAgICAgICAgcmV0dXJuIHVpbnQoZGVmYXVsdENob2ljZSk7CiAgICB9CgogICAgZnVuY3Rpb24gZ2V0TGFyZ2VzdFZhbHVlKCkgcHVibGljIHB1cmUgcmV0dXJucyAoQWN0aW9uQ2hvaWNlcykgewogICAgICAgIHJldHVybiB0eXBlKEFjdGlvbkNob2ljZXMpLm1heDsKICAgIH0KCiAgICBmdW5jdGlvbiBnZXRTbWFsbGVzdFZhbHVlKCkgcHVibGljIHB1cmUgcmV0dXJucyAoQWN0aW9uQ2hvaWNlcykgewogICAgICAgIHJldHVybiB0eXBlKEFjdGlvbkNob2ljZXMpLm1pbjsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.8;

contract test {
    enum ActionChoices { GoLeft, GoRight, GoStraight, SitStill }
    ActionChoices choice;
    ActionChoices constant defaultChoice = ActionChoices.GoStraight;

    function setGoStraight() public {
        choice = ActionChoices.GoStraight;
    }

    // Since enum types are not part of the ABI, the signature of "getChoice"
    // will automatically be changed to "getChoice() returns (uint8)"
    // for all matters external to Solidity.
    function getChoice() public view returns (ActionChoices) {
        return choice;
    }

    function getDefaultChoice() public pure returns (uint) {
        return uint(defaultChoice);
    }

    function getLargestValue() public pure returns (ActionChoices) {
        return type(ActionChoices).max;
    }

    function getSmallestValue() public pure returns (ActionChoices) {
        return type(ActionChoices).min;
    }
}

Note

Enums can also be declared on the file level, outside of contract or library definitions.

### User-defined Value Types[](#user-defined-value-types "Permalink to this heading")

A user-defined value type allows creating a zero cost abstraction over an elementary value type. This is similar to an alias, but with stricter type requirements.

A user-defined value type is defined using `type C is V`, where `C` is the name of the newly introduced type and `V` has to be a built-in value type (the “underlying type”). The function `C.wrap` is used to convert from the underlying type to the custom type. Similarly, the function `C.unwrap` is used to convert from the custom type to the underlying type.

The type `C` does not have any operators or attached member functions. In particular, even the operator `==` is not defined. Explicit and implicit conversions to and from other types are disallowed.

The data-representation of values of such types are inherited from the underlying type and the underlying type is also used in the ABI.

The following example illustrates a custom type `UFixed256x18` representing a decimal fixed point type with 18 decimals and a minimal library to do arithmetic operations on the type.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguODsKCi8vIFJlcHJlc2VudCBhIDE4IGRlY2ltYWwsIDI1NiBiaXQgd2lkZSBmaXhlZCBwb2ludCB0eXBlIHVzaW5nIGEgdXNlci1kZWZpbmVkIHZhbHVlIHR5cGUuCnR5cGUgVUZpeGVkMjU2eDE4IGlzIHVpbnQyNTY7CgovLy8gQSBtaW5pbWFsIGxpYnJhcnkgdG8gZG8gZml4ZWQgcG9pbnQgb3BlcmF0aW9ucyBvbiBVRml4ZWQyNTZ4MTguCmxpYnJhcnkgRml4ZWRNYXRoIHsKICAgIHVpbnQgY29uc3RhbnQgbXVsdGlwbGllciA9IDEwKioxODsKCiAgICAvLy8gQWRkcyB0d28gVUZpeGVkMjU2eDE4IG51bWJlcnMuIFJldmVydHMgb24gb3ZlcmZsb3csIHJlbHlpbmcgb24gY2hlY2tlZAogICAgLy8vIGFyaXRobWV0aWMgb24gdWludDI1Ni4KICAgIGZ1bmN0aW9uIGFkZChVRml4ZWQyNTZ4MTggYSwgVUZpeGVkMjU2eDE4IGIpIGludGVybmFsIHB1cmUgcmV0dXJucyAoVUZpeGVkMjU2eDE4KSB7CiAgICAgICAgcmV0dXJuIFVGaXhlZDI1NngxOC53cmFwKFVGaXhlZDI1NngxOC51bndyYXAoYSkgKyBVRml4ZWQyNTZ4MTgudW53cmFwKGIpKTsKICAgIH0KICAgIC8vLyBNdWx0aXBsaWVzIFVGaXhlZDI1NngxOCBhbmQgdWludDI1Ni4gUmV2ZXJ0cyBvbiBvdmVyZmxvdywgcmVseWluZyBvbiBjaGVja2VkCiAgICAvLy8gYXJpdGhtZXRpYyBvbiB1aW50MjU2LgogICAgZnVuY3Rpb24gbXVsKFVGaXhlZDI1NngxOCBhLCB1aW50MjU2IGIpIGludGVybmFsIHB1cmUgcmV0dXJucyAoVUZpeGVkMjU2eDE4KSB7CiAgICAgICAgcmV0dXJuIFVGaXhlZDI1NngxOC53cmFwKFVGaXhlZDI1NngxOC51bndyYXAoYSkgKiBiKTsKICAgIH0KICAgIC8vLyBUYWtlIHRoZSBmbG9vciBvZiBhIFVGaXhlZDI1NngxOCBudW1iZXIuCiAgICAvLy8gQHJldHVybiB0aGUgbGFyZ2VzdCBpbnRlZ2VyIHRoYXQgZG9lcyBub3QgZXhjZWVkIGBhYC4KICAgIGZ1bmN0aW9uIGZsb29yKFVGaXhlZDI1NngxOCBhKSBpbnRlcm5hbCBwdXJlIHJldHVybnMgKHVpbnQyNTYpIHsKICAgICAgICByZXR1cm4gVUZpeGVkMjU2eDE4LnVud3JhcChhKSAvIG11bHRpcGxpZXI7CiAgICB9CiAgICAvLy8gVHVybnMgYSB1aW50MjU2IGludG8gYSBVRml4ZWQyNTZ4MTggb2YgdGhlIHNhbWUgdmFsdWUuCiAgICAvLy8gUmV2ZXJ0cyBpZiB0aGUgaW50ZWdlciBpcyB0b28gbGFyZ2UuCiAgICBmdW5jdGlvbiB0b1VGaXhlZDI1NngxOCh1aW50MjU2IGEpIGludGVybmFsIHB1cmUgcmV0dXJucyAoVUZpeGVkMjU2eDE4KSB7CiAgICAgICAgcmV0dXJuIFVGaXhlZDI1NngxOC53cmFwKGEgKiBtdWx0aXBsaWVyKTsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.8;

// Represent a 18 decimal, 256 bit wide fixed point type using a user-defined value type.
type UFixed256x18 is uint256;

/// A minimal library to do fixed point operations on UFixed256x18.
library FixedMath {
    uint constant multiplier = 10**18;

    /// Adds two UFixed256x18 numbers. Reverts on overflow, relying on checked
    /// arithmetic on uint256.
    function add(UFixed256x18 a, UFixed256x18 b) internal pure returns (UFixed256x18) {
        return UFixed256x18.wrap(UFixed256x18.unwrap(a) + UFixed256x18.unwrap(b));
    }
    /// Multiplies UFixed256x18 and uint256. Reverts on overflow, relying on checked
    /// arithmetic on uint256.
    function mul(UFixed256x18 a, uint256 b) internal pure returns (UFixed256x18) {
        return UFixed256x18.wrap(UFixed256x18.unwrap(a) * b);
    }
    /// Take the floor of a UFixed256x18 number.
    /// @return the largest integer that does not exceed `a`.
    function floor(UFixed256x18 a) internal pure returns (uint256) {
        return UFixed256x18.unwrap(a) / multiplier;
    }
    /// Turns a uint256 into a UFixed256x18 of the same value.
    /// Reverts if the integer is too large.
    function toUFixed256x18(uint256 a) internal pure returns (UFixed256x18) {
        return UFixed256x18.wrap(a * multiplier);
    }
}

Notice how `UFixed256x18.wrap` and `FixedMath.toUFixed256x18` have the same signature but perform two very different operations: The `UFixed256x18.wrap` function returns a `UFixed256x18` that has the same data representation as the input, whereas `toUFixed256x18` returns a `UFixed256x18` that has the same numerical value.

### Function Types[](#function-types "Permalink to this heading")

Function types are the types of functions. Variables of function type can be assigned from functions and function parameters of function type can be used to pass functions to and return functions from function calls. Function types come in two flavours - _internal_ and _external_ functions:

Internal functions can only be called inside the current contract (more specifically, inside the current code unit, which also includes internal library functions and inherited functions) because they cannot be executed outside of the context of the current contract. Calling an internal function is realized by jumping to its entry label, just like when calling a function of the current contract internally.

External functions consist of an address and a function signature and they can be passed via and returned from external function calls.

Function types are notated as follows:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=ZnVuY3Rpb24gKDxwYXJhbWV0ZXIgdHlwZXM+KSB7aW50ZXJuYWx8ZXh0ZXJuYWx9IFtwdXJlfHZpZXd8cGF5YWJsZV0gW3JldHVybnMgKDxyZXR1cm4gdHlwZXM+KV0=)

function (<parameter types>) {internal|external} [pure|view|payable] [returns (<return types>)]

In contrast to the parameter types, the return types cannot be empty - if the function type should not return anything, the whole `returns (<return types>)` part has to be omitted.

By default, function types are internal, so the `internal` keyword can be omitted. Note that this only applies to function types. Visibility has to be specified explicitly for functions defined in contracts, they do not have a default.

Conversions:

A function type `A` is implicitly convertible to a function type `B` if and only if their parameter types are identical, their return types are identical, their internal/external property is identical and the state mutability of `A` is more restrictive than the state mutability of `B`. In particular:

- `pure` functions can be converted to `view` and `non-payable` functions
    
- `view` functions can be converted to `non-payable` functions
    
- `payable` functions can be converted to `non-payable` functions
    

No other conversions between function types are possible.

The rule about `payable` and `non-payable` might be a little confusing, but in essence, if a function is `payable`, this means that it also accepts a payment of zero Ether, so it also is `non-payable`. On the other hand, a `non-payable` function will reject Ether sent to it, so `non-payable` functions cannot be converted to `payable` functions. To clarify, rejecting ether is more restrictive than not rejecting ether. This means you can override a payable function with a non-payable but not the other way around.

Additionally, When you define a `non-payable` function pointer, the compiler does not enforce that the pointed function will actually reject ether. Instead, it enforces that the function pointer is never used to send ether. Which makes it possible to assign a `payable` function pointer to a `non-payable` function pointer ensuring both types behave the same way, i.e, both cannot be used to send ether.

If a function type variable is not initialised, calling it results in a [Panic error](control-structures.html#assert-and-require). The same happens if you call a function after using `delete` on it.

If external function types are used outside of the context of Solidity, they are treated as the `function` type, which encodes the address followed by the function identifier together in a single `bytes24` type.

Note that public functions of the current contract can be used both as an internal and as an external function. To use `f` as an internal function, just use `f`, if you want to use its external form, use `this.f`.

A function of an internal type can be assigned to a variable of an internal function type regardless of where it is defined. This includes private, internal and public functions of both contracts and libraries as well as free functions. External function types, on the other hand, are only compatible with public and external contract functions.

Note

External functions with `calldata` parameters are incompatible with external function types with `calldata` parameters. They are compatible with the corresponding types with `memory` parameters instead. For example, there is no function that can be pointed at by a value of type `function (string calldata) external` while `function (string memory) external` can point at both `function f(string memory) external {}` and `function g(string calldata) external {}`. This is because for both locations the arguments are passed to the function in the same way. The caller cannot pass its calldata directly to an external function and always ABI-encodes the arguments into memory. Marking the parameters as `calldata` only affects the implementation of the external function and is meaningless in a function pointer on the caller’s side.

Libraries are excluded because they require a `delegatecall` and use [a different ABI convention for their selectors](contracts.html#library-selectors). Functions declared in interfaces do not have definitions so pointing at them does not make sense either.

Members:

External (or public) functions have the following members:

- `.address` returns the address of the contract of the function.
    
- `.selector` returns the [ABI function selector](abi-spec.html#abi-function-selector)
    

Note

External (or public) functions used to have the additional members `.gas(uint)` and `.value(uint)`. These were deprecated in Solidity 0.6.2 and removed in Solidity 0.7.0. Instead use `{gas: ...}` and `{value: ...}` to specify the amount of gas or the amount of wei sent to a function, respectively. See [External Function Calls](control-structures.html#external-function-calls) for more information.

Example that shows how to use the members:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjQgPDAuOS4wOwoKY29udHJhY3QgRXhhbXBsZSB7CiAgICBmdW5jdGlvbiBmKCkgcHVibGljIHBheWFibGUgcmV0dXJucyAoYnl0ZXM0KSB7CiAgICAgICAgYXNzZXJ0KHRoaXMuZi5hZGRyZXNzID09IGFkZHJlc3ModGhpcykpOwogICAgICAgIHJldHVybiB0aGlzLmYuc2VsZWN0b3I7CiAgICB9CgogICAgZnVuY3Rpb24gZygpIHB1YmxpYyB7CiAgICAgICAgdGhpcy5me2dhczogMTAsIHZhbHVlOiA4MDB9KCk7CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.4 <0.9.0;

contract Example {
    function f() public payable returns (bytes4) {
        assert(this.f.address == address(this));
        return this.f.selector;
    }

    function g() public {
        this.f{gas: 10, value: 800}();
    }
}

Example that shows how to use internal function types:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmxpYnJhcnkgQXJyYXlVdGlscyB7CiAgICAvLyBpbnRlcm5hbCBmdW5jdGlvbnMgY2FuIGJlIHVzZWQgaW4gaW50ZXJuYWwgbGlicmFyeSBmdW5jdGlvbnMgYmVjYXVzZQogICAgLy8gdGhleSB3aWxsIGJlIHBhcnQgb2YgdGhlIHNhbWUgY29kZSBjb250ZXh0CiAgICBmdW5jdGlvbiBtYXAodWludFtdIG1lbW9yeSBzZWxmLCBmdW5jdGlvbiAodWludCkgcHVyZSByZXR1cm5zICh1aW50KSBmKQogICAgICAgIGludGVybmFsCiAgICAgICAgcHVyZQogICAgICAgIHJldHVybnMgKHVpbnRbXSBtZW1vcnkgcikKICAgIHsKICAgICAgICByID0gbmV3IHVpbnRbXShzZWxmLmxlbmd0aCk7CiAgICAgICAgZm9yICh1aW50IGkgPSAwOyBpIDwgc2VsZi5sZW5ndGg7IGkrKykgewogICAgICAgICAgICByW2ldID0gZihzZWxmW2ldKTsKICAgICAgICB9CiAgICB9CgogICAgZnVuY3Rpb24gcmVkdWNlKAogICAgICAgIHVpbnRbXSBtZW1vcnkgc2VsZiwKICAgICAgICBmdW5jdGlvbiAodWludCwgdWludCkgcHVyZSByZXR1cm5zICh1aW50KSBmCiAgICApCiAgICAgICAgaW50ZXJuYWwKICAgICAgICBwdXJlCiAgICAgICAgcmV0dXJucyAodWludCByKQogICAgewogICAgICAgIHIgPSBzZWxmWzBdOwogICAgICAgIGZvciAodWludCBpID0gMTsgaSA8IHNlbGYubGVuZ3RoOyBpKyspIHsKICAgICAgICAgICAgciA9IGYociwgc2VsZltpXSk7CiAgICAgICAgfQogICAgfQoKICAgIGZ1bmN0aW9uIHJhbmdlKHVpbnQgbGVuZ3RoKSBpbnRlcm5hbCBwdXJlIHJldHVybnMgKHVpbnRbXSBtZW1vcnkgcikgewogICAgICAgIHIgPSBuZXcgdWludFtdKGxlbmd0aCk7CiAgICAgICAgZm9yICh1aW50IGkgPSAwOyBpIDwgci5sZW5ndGg7IGkrKykgewogICAgICAgICAgICByW2ldID0gaTsKICAgICAgICB9CiAgICB9Cn0KCgpjb250cmFjdCBQeXJhbWlkIHsKICAgIHVzaW5nIEFycmF5VXRpbHMgZm9yICo7CgogICAgZnVuY3Rpb24gcHlyYW1pZCh1aW50IGwpIHB1YmxpYyBwdXJlIHJldHVybnMgKHVpbnQpIHsKICAgICAgICByZXR1cm4gQXJyYXlVdGlscy5yYW5nZShsKS5tYXAoc3F1YXJlKS5yZWR1Y2Uoc3VtKTsKICAgIH0KCiAgICBmdW5jdGlvbiBzcXVhcmUodWludCB4KSBpbnRlcm5hbCBwdXJlIHJldHVybnMgKHVpbnQpIHsKICAgICAgICByZXR1cm4geCAqIHg7CiAgICB9CgogICAgZnVuY3Rpb24gc3VtKHVpbnQgeCwgdWludCB5KSBpbnRlcm5hbCBwdXJlIHJldHVybnMgKHVpbnQpIHsKICAgICAgICByZXR1cm4geCArIHk7CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

library ArrayUtils {
    // internal functions can be used in internal library functions because
    // they will be part of the same code context
    function map(uint[] memory self, function (uint) pure returns (uint) f)
        internal
        pure
        returns (uint[] memory r)
    {
        r = new uint[](self.length);
        for (uint i = 0; i < self.length; i++) {
            r[i] = f(self[i]);
        }
    }

    function reduce(
        uint[] memory self,
        function (uint, uint) pure returns (uint) f
    )
        internal
        pure
        returns (uint r)
    {
        r = self[0];
        for (uint i = 1; i < self.length; i++) {
            r = f(r, self[i]);
        }
    }

    function range(uint length) internal pure returns (uint[] memory r) {
        r = new uint[](length);
        for (uint i = 0; i < r.length; i++) {
            r[i] = i;
        }
    }
}

contract Pyramid {
    using ArrayUtils for *;

    function pyramid(uint l) public pure returns (uint) {
        return ArrayUtils.range(l).map(square).reduce(sum);
    }

    function square(uint x) internal pure returns (uint) {
        return x * x;
    }

    function sum(uint x, uint y) internal pure returns (uint) {
        return x + y;
    }
}

Another example that uses external function types:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjIyIDwwLjkuMDsKCgpjb250cmFjdCBPcmFjbGUgewogICAgc3RydWN0IFJlcXVlc3QgewogICAgICAgIGJ5dGVzIGRhdGE7CiAgICAgICAgZnVuY3Rpb24odWludCkgZXh0ZXJuYWwgY2FsbGJhY2s7CiAgICB9CgogICAgUmVxdWVzdFtdIHByaXZhdGUgcmVxdWVzdHM7CiAgICBldmVudCBOZXdSZXF1ZXN0KHVpbnQpOwoKICAgIGZ1bmN0aW9uIHF1ZXJ5KGJ5dGVzIG1lbW9yeSBkYXRhLCBmdW5jdGlvbih1aW50KSBleHRlcm5hbCBjYWxsYmFjaykgcHVibGljIHsKICAgICAgICByZXF1ZXN0cy5wdXNoKFJlcXVlc3QoZGF0YSwgY2FsbGJhY2spKTsKICAgICAgICBlbWl0IE5ld1JlcXVlc3QocmVxdWVzdHMubGVuZ3RoIC0gMSk7CiAgICB9CgogICAgZnVuY3Rpb24gcmVwbHkodWludCByZXF1ZXN0SUQsIHVpbnQgcmVzcG9uc2UpIHB1YmxpYyB7CiAgICAgICAgLy8gSGVyZSBnb2VzIHRoZSBjaGVjayB0aGF0IHRoZSByZXBseSBjb21lcyBmcm9tIGEgdHJ1c3RlZCBzb3VyY2UKICAgICAgICByZXF1ZXN0c1tyZXF1ZXN0SURdLmNhbGxiYWNrKHJlc3BvbnNlKTsKICAgIH0KfQoKCmNvbnRyYWN0IE9yYWNsZVVzZXIgewogICAgT3JhY2xlIGNvbnN0YW50IHByaXZhdGUgT1JBQ0xFX0NPTlNUID0gT3JhY2xlKGFkZHJlc3MoMHgwMDAwMDAwMDIxOWFiNTQwMzU2Y0JCODM5Q2JlMDUzMDNkNzcwNUZhKSk7IC8vIGtub3duIGNvbnRyYWN0CiAgICB1aW50IHByaXZhdGUgZXhjaGFuZ2VSYXRlOwoKICAgIGZ1bmN0aW9uIGJ1eVNvbWV0aGluZygpIHB1YmxpYyB7CiAgICAgICAgT1JBQ0xFX0NPTlNULnF1ZXJ5KCJVU0QiLCB0aGlzLm9yYWNsZVJlc3BvbnNlKTsKICAgIH0KCiAgICBmdW5jdGlvbiBvcmFjbGVSZXNwb25zZSh1aW50IHJlc3BvbnNlKSBwdWJsaWMgewogICAgICAgIHJlcXVpcmUoCiAgICAgICAgICAgIG1zZy5zZW5kZXIgPT0gYWRkcmVzcyhPUkFDTEVfQ09OU1QpLAogICAgICAgICAgICAiT25seSBvcmFjbGUgY2FuIGNhbGwgdGhpcy4iCiAgICAgICAgKTsKICAgICAgICBleGNoYW5nZVJhdGUgPSByZXNwb25zZTsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.22 <0.9.0;

contract Oracle {
    struct Request {
        bytes data;
        function(uint) external callback;
    }

    Request[] private requests;
    event NewRequest(uint);

    function query(bytes memory data, function(uint) external callback) public {
        requests.push(Request(data, callback));
        emit NewRequest(requests.length - 1);
    }

    function reply(uint requestID, uint response) public {
        // Here goes the check that the reply comes from a trusted source
        requests[requestID].callback(response);
    }
}

contract OracleUser {
    Oracle constant private ORACLE_CONST = Oracle(address(0x00000000219ab540356cBB839Cbe05303d7705Fa)); // known contract
    uint private exchangeRate;

    function buySomething() public {
        ORACLE_CONST.query("USD", this.oracleResponse);
    }

    function oracleResponse(uint response) public {
        require(
            msg.sender == address(ORACLE_CONST),
            "Only oracle can call this."
        );
        exchangeRate = response;
    }
}

Note

Lambda or inline functions are planned but not yet supported.

## Reference Types[](#reference-types "Permalink to this heading")

Values of reference type can be modified through multiple different names. Contrast this with value types where you get an independent copy whenever a variable of value type is used. Because of that, reference types have to be handled more carefully than value types. Currently, reference types comprise structs, arrays and mappings. If you use a reference type, you always have to explicitly provide the data area where the type is stored: `memory` (whose lifetime is limited to an external function call), `storage` (the location where the state variables are stored, where the lifetime is limited to the lifetime of a contract) or `calldata` (special data location that contains the function arguments).

An assignment or type conversion that changes the data location will always incur an automatic copy operation, while assignments inside the same data location only copy in some cases for storage types.

### Data location[](#data-location "Permalink to this heading")

Every reference type has an additional annotation, the “data location”, about where it is stored. There are three data locations: `memory`, `storage` and `calldata`. Calldata is a non-modifiable, non-persistent area where function arguments are stored, and behaves mostly like memory.

Note

If you can, try to use `calldata` as data location because it will avoid copies and also makes sure that the data cannot be modified. Arrays and structs with `calldata` data location can also be returned from functions, but it is not possible to allocate such types.

Note

Prior to version 0.6.9 data location for reference-type arguments was limited to `calldata` in external functions, `memory` in public functions and either `memory` or `storage` in internal and private ones. Now `memory` and `calldata` are allowed in all functions regardless of their visibility.

Note

Prior to version 0.5.0 the data location could be omitted, and would default to different locations depending on the kind of variable, function type, etc., but all complex types must now give an explicit data location.

#### Data location and assignment behavior[](#data-location-and-assignment-behavior "Permalink to this heading")

Data locations are not only relevant for persistency of data, but also for the semantics of assignments:

- Assignments between `storage` and `memory` (or from `calldata`) always create an independent copy.
    
- Assignments from `memory` to `memory` only create references. This means that changes to one memory variable are also visible in all other memory variables that refer to the same data.
    
- Assignments from `storage` to a **local** storage variable also only assign a reference.
    
- All other assignments to `storage` always copy. Examples for this case are assignments to state variables or to members of local variables of storage struct type, even if the local variable itself is just a reference.
    

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC41LjAgPDAuOS4wOwoKY29udHJhY3QgQyB7CiAgICAvLyBUaGUgZGF0YSBsb2NhdGlvbiBvZiB4IGlzIHN0b3JhZ2UuCiAgICAvLyBUaGlzIGlzIHRoZSBvbmx5IHBsYWNlIHdoZXJlIHRoZQogICAgLy8gZGF0YSBsb2NhdGlvbiBjYW4gYmUgb21pdHRlZC4KICAgIHVpbnRbXSB4OwoKICAgIC8vIFRoZSBkYXRhIGxvY2F0aW9uIG9mIG1lbW9yeUFycmF5IGlzIG1lbW9yeS4KICAgIGZ1bmN0aW9uIGYodWludFtdIG1lbW9yeSBtZW1vcnlBcnJheSkgcHVibGljIHsKICAgICAgICB4ID0gbWVtb3J5QXJyYXk7IC8vIHdvcmtzLCBjb3BpZXMgdGhlIHdob2xlIGFycmF5IHRvIHN0b3JhZ2UKICAgICAgICB1aW50W10gc3RvcmFnZSB5ID0geDsgLy8gd29ya3MsIGFzc2lnbnMgYSBwb2ludGVyLCBkYXRhIGxvY2F0aW9uIG9mIHkgaXMgc3RvcmFnZQogICAgICAgIHlbN107IC8vIGZpbmUsIHJldHVybnMgdGhlIDh0aCBlbGVtZW50CiAgICAgICAgeS5wb3AoKTsgLy8gZmluZSwgbW9kaWZpZXMgeCB0aHJvdWdoIHkKICAgICAgICBkZWxldGUgeDsgLy8gZmluZSwgY2xlYXJzIHRoZSBhcnJheSwgYWxzbyBtb2RpZmllcyB5CiAgICAgICAgLy8gVGhlIGZvbGxvd2luZyBkb2VzIG5vdCB3b3JrOyBpdCB3b3VsZCBuZWVkIHRvIGNyZWF0ZSBhIG5ldyB0ZW1wb3JhcnkgLwogICAgICAgIC8vIHVubmFtZWQgYXJyYXkgaW4gc3RvcmFnZSwgYnV0IHN0b3JhZ2UgaXMgInN0YXRpY2FsbHkiIGFsbG9jYXRlZDoKICAgICAgICAvLyB5ID0gbWVtb3J5QXJyYXk7CiAgICAgICAgLy8gU2ltaWxhcmx5LCAiZGVsZXRlIHkiIGlzIG5vdCB2YWxpZCwgYXMgYXNzaWdubWVudHMgdG8gbG9jYWwgdmFyaWFibGVzCiAgICAgICAgLy8gcmVmZXJlbmNpbmcgc3RvcmFnZSBvYmplY3RzIGNhbiBvbmx5IGJlIG1hZGUgZnJvbSBleGlzdGluZyBzdG9yYWdlIG9iamVjdHMuCiAgICAgICAgLy8gSXQgd291bGQgInJlc2V0IiB0aGUgcG9pbnRlciwgYnV0IHRoZXJlIGlzIG5vIHNlbnNpYmxlIGxvY2F0aW9uIGl0IGNvdWxkIHBvaW50IHRvLgogICAgICAgIC8vIEZvciBtb3JlIGRldGFpbHMgc2VlIHRoZSBkb2N1bWVudGF0aW9uIG9mIHRoZSAiZGVsZXRlIiBvcGVyYXRvci4KICAgICAgICAvLyBkZWxldGUgeTsKICAgICAgICBnKHgpOyAvLyBjYWxscyBnLCBoYW5kaW5nIG92ZXIgYSByZWZlcmVuY2UgdG8geAogICAgICAgIGgoeCk7IC8vIGNhbGxzIGggYW5kIGNyZWF0ZXMgYW4gaW5kZXBlbmRlbnQsIHRlbXBvcmFyeSBjb3B5IGluIG1lbW9yeQogICAgfQoKICAgIGZ1bmN0aW9uIGcodWludFtdIHN0b3JhZ2UpIGludGVybmFsIHB1cmUge30KICAgIGZ1bmN0aW9uIGgodWludFtdIG1lbW9yeSkgcHVibGljIHB1cmUge30KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.5.0 <0.9.0;

contract C {
    // The data location of x is storage.
    // This is the only place where the
    // data location can be omitted.
    uint[] x;

    // The data location of memoryArray is memory.
    function f(uint[] memory memoryArray) public {
        x = memoryArray; // works, copies the whole array to storage
        uint[] storage y = x; // works, assigns a pointer, data location of y is storage
        y[7]; // fine, returns the 8th element
        y.pop(); // fine, modifies x through y
        delete x; // fine, clears the array, also modifies y
        // The following does not work; it would need to create a new temporary /
        // unnamed array in storage, but storage is "statically" allocated:
        // y = memoryArray;
        // Similarly, "delete y" is not valid, as assignments to local variables
        // referencing storage objects can only be made from existing storage objects.
        // It would "reset" the pointer, but there is no sensible location it could point to.
        // For more details see the documentation of the "delete" operator.
        // delete y;
        g(x); // calls g, handing over a reference to x
        h(x); // calls h and creates an independent, temporary copy in memory
    }

    function g(uint[] storage) internal pure {}
    function h(uint[] memory) public pure {}
}

### Arrays[](#arrays "Permalink to this heading")

Arrays can have a compile-time fixed size, or they can have a dynamic size.

The type of an array of fixed size `k` and element type `T` is written as `T[k]`, and an array of dynamic size as `T[]`.

For example, an array of 5 dynamic arrays of `uint` is written as `uint[][5]`. The notation is reversed compared to some other languages. In Solidity, `X[3]` is always an array containing three elements of type `X`, even if `X` is itself an array. This is not the case in other languages such as C.

Indices are zero-based, and access is in the opposite direction of the declaration.

For example, if you have a variable `uint[][5] memory x`, you access the seventh `uint` in the third dynamic array using `x[2][6]`, and to access the third dynamic array, use `x[2]`. Again, if you have an array `T[5] a` for a type `T` that can also be an array, then `a[2]` always has type `T`.

Array elements can be of any type, including mapping or struct. The general restrictions for types apply, in that mappings can only be stored in the `storage` data location and publicly-visible functions need parameters that are [ABI types](abi-spec.html#abi).

It is possible to mark state variable arrays `public` and have Solidity create a [getter](contracts.html#visibility-and-getters). The numeric index becomes a required parameter for the getter.

Accessing an array past its end causes a failing assertion. Methods `.push()` and `.push(value)` can be used to append a new element at the end of a dynamically-sized array, where `.push()` appends a zero-initialized element and returns a reference to it.

Note

Dynamically-sized arrays can only be resized in storage. In memory, such arrays can be of arbitrary size but the size cannot be changed once an array is allocated.

#### `bytes` and `string` as Arrays[](#bytes-and-string-as-arrays "Permalink to this heading")

Variables of type `bytes` and `string` are special arrays. The `bytes` type is similar to `bytes1[]`, but it is packed tightly in calldata and memory. `string` is equal to `bytes` but does not allow length or index access.

Solidity does not have string manipulation functions, but there are third-party string libraries. You can also compare two strings by their keccak256-hash using `keccak256(abi.encodePacked(s1)) == keccak256(abi.encodePacked(s2))` and concatenate two strings using `string.concat(s1, s2)`.

You should use `bytes` over `bytes1[]` because it is cheaper, since using `bytes1[]` in `memory` adds 31 padding bytes between the elements. Note that in `storage`, the padding is absent due to tight packing, see [bytes and string](internals/layout_in_storage.html#bytes-and-string). As a general rule, use `bytes` for arbitrary-length raw byte data and `string` for arbitrary-length string (UTF-8) data. If you can limit the length to a certain number of bytes, always use one of the value types `bytes1` to `bytes32` because they are much cheaper.

Note

If you want to access the byte-representation of a string `s`, use `bytes(s).length` / `bytes(s)[7] = 'x';`. Keep in mind that you are accessing the low-level bytes of the UTF-8 representation, and not the individual characters.

#### The functions `bytes.concat` and `string.concat`[](#the-functions-bytes-concat-and-string-concat "Permalink to this heading")

You can concatenate an arbitrary number of `string` values using `string.concat`. The function returns a single `string memory` array that contains the contents of the arguments without padding. If you want to use parameters of other types that are not implicitly convertible to `string`, you need to convert them to `string` first.

Analogously, the `bytes.concat` function can concatenate an arbitrary number of `bytes` or `bytes1 ... bytes32` values. The function returns a single `bytes memory` array that contains the contents of the arguments without padding. If you want to use string parameters or other types that are not implicitly convertible to `bytes`, you need to convert them to `bytes` or `bytes1`/…/`bytes32` first.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguMTI7Cgpjb250cmFjdCBDIHsKICAgIHN0cmluZyBzID0gIlN0b3JhZ2UiOwogICAgZnVuY3Rpb24gZihieXRlcyBjYWxsZGF0YSBiYywgc3RyaW5nIG1lbW9yeSBzbSwgYnl0ZXMxNiBiKSBwdWJsaWMgdmlldyB7CiAgICAgICAgc3RyaW5nIG1lbW9yeSBjb25jYXRTdHJpbmcgPSBzdHJpbmcuY29uY2F0KHMsIHN0cmluZyhiYyksICJMaXRlcmFsIiwgc20pOwogICAgICAgIGFzc2VydCgoYnl0ZXMocykubGVuZ3RoICsgYmMubGVuZ3RoICsgNyArIGJ5dGVzKHNtKS5sZW5ndGgpID09IGJ5dGVzKGNvbmNhdFN0cmluZykubGVuZ3RoKTsKCiAgICAgICAgYnl0ZXMgbWVtb3J5IGNvbmNhdEJ5dGVzID0gYnl0ZXMuY29uY2F0KGJ5dGVzKHMpLCBiYywgYmNbOjJdLCAiTGl0ZXJhbCIsIGJ5dGVzKHNtKSwgYik7CiAgICAgICAgYXNzZXJ0KChieXRlcyhzKS5sZW5ndGggKyBiYy5sZW5ndGggKyAyICsgNyArIGJ5dGVzKHNtKS5sZW5ndGggKyBiLmxlbmd0aCkgPT0gY29uY2F0Qnl0ZXMubGVuZ3RoKTsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.12;

contract C {
    string s = "Storage";
    function f(bytes calldata bc, string memory sm, bytes16 b) public view {
        string memory concatString = string.concat(s, string(bc), "Literal", sm);
        assert((bytes(s).length + bc.length + 7 + bytes(sm).length) == bytes(concatString).length);

        bytes memory concatBytes = bytes.concat(bytes(s), bc, bc[:2], "Literal", bytes(sm), b);
        assert((bytes(s).length + bc.length + 2 + 7 + bytes(sm).length + b.length) == concatBytes.length);
    }
}

If you call `string.concat` or `bytes.concat` without arguments they return an empty array.

#### Allocating Memory Arrays[](#allocating-memory-arrays "Permalink to this heading")

Memory arrays with dynamic length can be created using the `new` operator. As opposed to storage arrays, it is **not** possible to resize memory arrays (e.g. the `.push` member functions are not available). You either have to calculate the required size in advance or create a new memory array and copy every element.

As all variables in Solidity, the elements of newly allocated arrays are always initialized with the [default value](control-structures.html#default-value).

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IEMgewogICAgZnVuY3Rpb24gZih1aW50IGxlbikgcHVibGljIHB1cmUgewogICAgICAgIHVpbnRbXSBtZW1vcnkgYSA9IG5ldyB1aW50W10oNyk7CiAgICAgICAgYnl0ZXMgbWVtb3J5IGIgPSBuZXcgYnl0ZXMobGVuKTsKICAgICAgICBhc3NlcnQoYS5sZW5ndGggPT0gNyk7CiAgICAgICAgYXNzZXJ0KGIubGVuZ3RoID09IGxlbik7CiAgICAgICAgYVs2XSA9IDg7CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract C {
    function f(uint len) public pure {
        uint[] memory a = new uint[](7);
        bytes memory b = new bytes(len);
        assert(a.length == 7);
        assert(b.length == len);
        a[6] = 8;
    }
}

#### Array Literals[](#array-literals "Permalink to this heading")

An array literal is a comma-separated list of one or more expressions, enclosed in square brackets (`[...]`). For example `[1, a, f(3)]`. The type of the array literal is determined as follows:

It is always a statically-sized memory array whose length is the number of expressions.

The base type of the array is the type of the first expression on the list such that all other expressions can be implicitly converted to it. It is a type error if this is not possible.

It is not enough that there is a type all the elements can be converted to. One of the elements has to be of that type.

In the example below, the type of `[1, 2, 3]` is `uint8[3] memory`, because the type of each of these constants is `uint8`. If you want the result to be a `uint[3] memory` type, you need to convert the first element to `uint`.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IEMgewogICAgZnVuY3Rpb24gZigpIHB1YmxpYyBwdXJlIHsKICAgICAgICBnKFt1aW50KDEpLCAyLCAzXSk7CiAgICB9CiAgICBmdW5jdGlvbiBnKHVpbnRbM10gbWVtb3J5KSBwdWJsaWMgcHVyZSB7CiAgICAgICAgLy8gLi4uCiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract C {
    function f() public pure {
        g([uint(1), 2, 3]);
    }
    function g(uint[3] memory) public pure {
        // ...
    }
}

The array literal `[1, -1]` is invalid because the type of the first expression is `uint8` while the type of the second is `int8` and they cannot be implicitly converted to each other. To make it work, you can use `[int8(1), -1]`, for example.

Since fixed-size memory arrays of different type cannot be converted into each other (even if the base types can), you always have to specify a common base type explicitly if you want to use two-dimensional array literals:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IEMgewogICAgZnVuY3Rpb24gZigpIHB1YmxpYyBwdXJlIHJldHVybnMgKHVpbnQyNFsyXVs0XSBtZW1vcnkpIHsKICAgICAgICB1aW50MjRbMl1bNF0gbWVtb3J5IHggPSBbW3VpbnQyNCgweDEpLCAxXSwgWzB4ZmZmZmZmLCAyXSwgW3VpbnQyNCgweGZmKSwgM10sIFt1aW50MjQoMHhmZmZmKSwgNF1dOwogICAgICAgIC8vIFRoZSBmb2xsb3dpbmcgZG9lcyBub3Qgd29yaywgYmVjYXVzZSBzb21lIG9mIHRoZSBpbm5lciBhcnJheXMgYXJlIG5vdCBvZiB0aGUgcmlnaHQgdHlwZS4KICAgICAgICAvLyB1aW50WzJdWzRdIG1lbW9yeSB4ID0gW1sweDEsIDFdLCBbMHhmZmZmZmYsIDJdLCBbMHhmZiwgM10sIFsweGZmZmYsIDRdXTsKICAgICAgICByZXR1cm4geDsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract C {
    function f() public pure returns (uint24[2][4] memory) {
        uint24[2][4] memory x = [[uint24(0x1), 1], [0xffffff, 2], [uint24(0xff), 3], [uint24(0xffff), 4]];
        // The following does not work, because some of the inner arrays are not of the right type.
        // uint[2][4] memory x = [[0x1, 1], [0xffffff, 2], [0xff, 3], [0xffff, 4]];
        return x;
    }
}

Fixed size memory arrays cannot be assigned to dynamically-sized memory arrays, i.e. the following is not possible:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKLy8gVGhpcyB3aWxsIG5vdCBjb21waWxlLgpjb250cmFjdCBDIHsKICAgIGZ1bmN0aW9uIGYoKSBwdWJsaWMgewogICAgICAgIC8vIFRoZSBuZXh0IGxpbmUgY3JlYXRlcyBhIHR5cGUgZXJyb3IgYmVjYXVzZSB1aW50WzNdIG1lbW9yeQogICAgICAgIC8vIGNhbm5vdCBiZSBjb252ZXJ0ZWQgdG8gdWludFtdIG1lbW9yeS4KICAgICAgICB1aW50W10gbWVtb3J5IHggPSBbdWludCgxKSwgMywgNF07CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

// This will not compile.
contract C {
    function f() public {
        // The next line creates a type error because uint[3] memory
        // cannot be converted to uint[] memory.
        uint[] memory x = [uint(1), 3, 4];
    }
}

It is planned to remove this restriction in the future, but it creates some complications because of how arrays are passed in the ABI.

If you want to initialize dynamically-sized arrays, you have to assign the individual elements:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCmNvbnRyYWN0IEMgewogICAgZnVuY3Rpb24gZigpIHB1YmxpYyBwdXJlIHsKICAgICAgICB1aW50W10gbWVtb3J5IHggPSBuZXcgdWludFtdKDMpOwogICAgICAgIHhbMF0gPSAxOwogICAgICAgIHhbMV0gPSAzOwogICAgICAgIHhbMl0gPSA0OwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

contract C {
    function f() public pure {
        uint[] memory x = new uint[](3);
        x[0] = 1;
        x[1] = 3;
        x[2] = 4;
    }
}

#### Array Members[](#array-members "Permalink to this heading")

**length**:

Arrays have a `length` member that contains their number of elements. The length of memory arrays is fixed (but dynamic, i.e. it can depend on runtime parameters) once they are created.

**push()**:

Dynamic storage arrays and `bytes` (not `string`) have a member function called `push()` that you can use to append a zero-initialised element at the end of the array. It returns a reference to the element, so that it can be used like `x.push().t = 2` or `x.push() = b`.

**push(x)**:

Dynamic storage arrays and `bytes` (not `string`) have a member function called `push(x)` that you can use to append a given element at the end of the array. The function returns nothing.

**pop()**:

Dynamic storage arrays and `bytes` (not `string`) have a member function called `pop()` that you can use to remove an element from the end of the array. This also implicitly calls [delete](#delete) on the removed element. The function returns nothing.

Note

Increasing the length of a storage array by calling `push()` has constant gas costs because storage is zero-initialised, while decreasing the length by calling `pop()` has a cost that depends on the “size” of the element being removed. If that element is an array, it can be very costly, because it includes explicitly clearing the removed elements similar to calling [delete](#delete) on them.

Note

To use arrays of arrays in external (instead of public) functions, you need to activate ABI coder v2.

Note

In EVM versions before Byzantium, it was not possible to access dynamic arrays return from function calls. If you call functions that return dynamic arrays, make sure to use an EVM that is set to Byzantium mode.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKY29udHJhY3QgQXJyYXlDb250cmFjdCB7CiAgICB1aW50WzIqKjIwXSBhTG90T2ZJbnRlZ2VyczsKICAgIC8vIE5vdGUgdGhhdCB0aGUgZm9sbG93aW5nIGlzIG5vdCBhIHBhaXIgb2YgZHluYW1pYyBhcnJheXMgYnV0IGEKICAgIC8vIGR5bmFtaWMgYXJyYXkgb2YgcGFpcnMgKGkuZS4gb2YgZml4ZWQgc2l6ZSBhcnJheXMgb2YgbGVuZ3RoIHR3bykuCiAgICAvLyBJbiBTb2xpZGl0eSwgVFtrXSBhbmQgVFtdIGFyZSBhbHdheXMgYXJyYXlzIHdpdGggZWxlbWVudHMgb2YgdHlwZSBULAogICAgLy8gZXZlbiBpZiBUIGl0c2VsZiBpcyBhbiBhcnJheS4KICAgIC8vIEJlY2F1c2Ugb2YgdGhhdCwgYm9vbFsyXVtdIGlzIGEgZHluYW1pYyBhcnJheSBvZiBlbGVtZW50cwogICAgLy8gdGhhdCBhcmUgYm9vbFsyXS4gVGhpcyBpcyBkaWZmZXJlbnQgZnJvbSBvdGhlciBsYW5ndWFnZXMsIGxpa2UgQy4KICAgIC8vIERhdGEgbG9jYXRpb24gZm9yIGFsbCBzdGF0ZSB2YXJpYWJsZXMgaXMgc3RvcmFnZS4KICAgIGJvb2xbMl1bXSBwYWlyc09mRmxhZ3M7CgogICAgLy8gbmV3UGFpcnMgaXMgc3RvcmVkIGluIG1lbW9yeSAtIHRoZSBvbmx5IHBvc3NpYmlsaXR5CiAgICAvLyBmb3IgcHVibGljIGNvbnRyYWN0IGZ1bmN0aW9uIGFyZ3VtZW50cwogICAgZnVuY3Rpb24gc2V0QWxsRmxhZ1BhaXJzKGJvb2xbMl1bXSBtZW1vcnkgbmV3UGFpcnMpIHB1YmxpYyB7CiAgICAgICAgLy8gYXNzaWdubWVudCB0byBhIHN0b3JhZ2UgYXJyYXkgcGVyZm9ybXMgYSBjb3B5IG9mIGBgbmV3UGFpcnNgYCBhbmQKICAgICAgICAvLyByZXBsYWNlcyB0aGUgY29tcGxldGUgYXJyYXkgYGBwYWlyc09mRmxhZ3NgYC4KICAgICAgICBwYWlyc09mRmxhZ3MgPSBuZXdQYWlyczsKICAgIH0KCiAgICBzdHJ1Y3QgU3RydWN0VHlwZSB7CiAgICAgICAgdWludFtdIGNvbnRlbnRzOwogICAgICAgIHVpbnQgbW9yZUluZm87CiAgICB9CiAgICBTdHJ1Y3RUeXBlIHM7CgogICAgZnVuY3Rpb24gZih1aW50W10gbWVtb3J5IGMpIHB1YmxpYyB7CiAgICAgICAgLy8gc3RvcmVzIGEgcmVmZXJlbmNlIHRvIGBgc2BgIGluIGBgZ2BgCiAgICAgICAgU3RydWN0VHlwZSBzdG9yYWdlIGcgPSBzOwogICAgICAgIC8vIGFsc28gY2hhbmdlcyBgYHMubW9yZUluZm9gYC4KICAgICAgICBnLm1vcmVJbmZvID0gMjsKICAgICAgICAvLyBhc3NpZ25zIGEgY29weSBiZWNhdXNlIGBgZy5jb250ZW50c2BgCiAgICAgICAgLy8gaXMgbm90IGEgbG9jYWwgdmFyaWFibGUsIGJ1dCBhIG1lbWJlciBvZgogICAgICAgIC8vIGEgbG9jYWwgdmFyaWFibGUuCiAgICAgICAgZy5jb250ZW50cyA9IGM7CiAgICB9CgogICAgZnVuY3Rpb24gc2V0RmxhZ1BhaXIodWludCBpbmRleCwgYm9vbCBmbGFnQSwgYm9vbCBmbGFnQikgcHVibGljIHsKICAgICAgICAvLyBhY2Nlc3MgdG8gYSBub24tZXhpc3RpbmcgaW5kZXggd2lsbCB0aHJvdyBhbiBleGNlcHRpb24KICAgICAgICBwYWlyc09mRmxhZ3NbaW5kZXhdWzBdID0gZmxhZ0E7CiAgICAgICAgcGFpcnNPZkZsYWdzW2luZGV4XVsxXSA9IGZsYWdCOwogICAgfQoKICAgIGZ1bmN0aW9uIGNoYW5nZUZsYWdBcnJheVNpemUodWludCBuZXdTaXplKSBwdWJsaWMgewogICAgICAgIC8vIHVzaW5nIHB1c2ggYW5kIHBvcCBpcyB0aGUgb25seSB3YXkgdG8gY2hhbmdlIHRoZQogICAgICAgIC8vIGxlbmd0aCBvZiBhbiBhcnJheQogICAgICAgIGlmIChuZXdTaXplIDwgcGFpcnNPZkZsYWdzLmxlbmd0aCkgewogICAgICAgICAgICB3aGlsZSAocGFpcnNPZkZsYWdzLmxlbmd0aCA+IG5ld1NpemUpCiAgICAgICAgICAgICAgICBwYWlyc09mRmxhZ3MucG9wKCk7CiAgICAgICAgfSBlbHNlIGlmIChuZXdTaXplID4gcGFpcnNPZkZsYWdzLmxlbmd0aCkgewogICAgICAgICAgICB3aGlsZSAocGFpcnNPZkZsYWdzLmxlbmd0aCA8IG5ld1NpemUpCiAgICAgICAgICAgICAgICBwYWlyc09mRmxhZ3MucHVzaCgpOwogICAgICAgIH0KICAgIH0KCiAgICBmdW5jdGlvbiBjbGVhcigpIHB1YmxpYyB7CiAgICAgICAgLy8gdGhlc2UgY2xlYXIgdGhlIGFycmF5cyBjb21wbGV0ZWx5CiAgICAgICAgZGVsZXRlIHBhaXJzT2ZGbGFnczsKICAgICAgICBkZWxldGUgYUxvdE9mSW50ZWdlcnM7CiAgICAgICAgLy8gaWRlbnRpY2FsIGVmZmVjdCBoZXJlCiAgICAgICAgcGFpcnNPZkZsYWdzID0gbmV3IGJvb2xbMl1bXSgwKTsKICAgIH0KCiAgICBieXRlcyBieXRlRGF0YTsKCiAgICBmdW5jdGlvbiBieXRlQXJyYXlzKGJ5dGVzIG1lbW9yeSBkYXRhKSBwdWJsaWMgewogICAgICAgIC8vIGJ5dGUgYXJyYXlzICgiYnl0ZXMiKSBhcmUgZGlmZmVyZW50IGFzIHRoZXkgYXJlIHN0b3JlZCB3aXRob3V0IHBhZGRpbmcsCiAgICAgICAgLy8gYnV0IGNhbiBiZSB0cmVhdGVkIGlkZW50aWNhbCB0byAidWludDhbXSIKICAgICAgICBieXRlRGF0YSA9IGRhdGE7CiAgICAgICAgZm9yICh1aW50IGkgPSAwOyBpIDwgNzsgaSsrKQogICAgICAgICAgICBieXRlRGF0YS5wdXNoKCk7CiAgICAgICAgYnl0ZURhdGFbM10gPSAweDA4OwogICAgICAgIGRlbGV0ZSBieXRlRGF0YVsyXTsKICAgIH0KCiAgICBmdW5jdGlvbiBhZGRGbGFnKGJvb2xbMl0gbWVtb3J5IGZsYWcpIHB1YmxpYyByZXR1cm5zICh1aW50KSB7CiAgICAgICAgcGFpcnNPZkZsYWdzLnB1c2goZmxhZyk7CiAgICAgICAgcmV0dXJuIHBhaXJzT2ZGbGFncy5sZW5ndGg7CiAgICB9CgogICAgZnVuY3Rpb24gY3JlYXRlTWVtb3J5QXJyYXkodWludCBzaXplKSBwdWJsaWMgcHVyZSByZXR1cm5zIChieXRlcyBtZW1vcnkpIHsKICAgICAgICAvLyBEeW5hbWljIG1lbW9yeSBhcnJheXMgYXJlIGNyZWF0ZWQgdXNpbmcgYG5ld2A6CiAgICAgICAgdWludFsyXVtdIG1lbW9yeSBhcnJheU9mUGFpcnMgPSBuZXcgdWludFsyXVtdKHNpemUpOwoKICAgICAgICAvLyBJbmxpbmUgYXJyYXlzIGFyZSBhbHdheXMgc3RhdGljYWxseS1zaXplZCBhbmQgaWYgeW91IG9ubHkKICAgICAgICAvLyB1c2UgbGl0ZXJhbHMsIHlvdSBoYXZlIHRvIHByb3ZpZGUgYXQgbGVhc3Qgb25lIHR5cGUuCiAgICAgICAgYXJyYXlPZlBhaXJzWzBdID0gW3VpbnQoMSksIDJdOwoKICAgICAgICAvLyBDcmVhdGUgYSBkeW5hbWljIGJ5dGUgYXJyYXk6CiAgICAgICAgYnl0ZXMgbWVtb3J5IGIgPSBuZXcgYnl0ZXMoMjAwKTsKICAgICAgICBmb3IgKHVpbnQgaSA9IDA7IGkgPCBiLmxlbmd0aDsgaSsrKQogICAgICAgICAgICBiW2ldID0gYnl0ZXMxKHVpbnQ4KGkpKTsKICAgICAgICByZXR1cm4gYjsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

contract ArrayContract {
    uint[2**20] aLotOfIntegers;
    // Note that the following is not a pair of dynamic arrays but a
    // dynamic array of pairs (i.e. of fixed size arrays of length two).
    // In Solidity, T[k] and T[] are always arrays with elements of type T,
    // even if T itself is an array.
    // Because of that, bool[2][] is a dynamic array of elements
    // that are bool[2]. This is different from other languages, like C.
    // Data location for all state variables is storage.
    bool[2][] pairsOfFlags;

    // newPairs is stored in memory - the only possibility
    // for public contract function arguments
    function setAllFlagPairs(bool[2][] memory newPairs) public {
        // assignment to a storage array performs a copy of ``newPairs`` and
        // replaces the complete array ``pairsOfFlags``.
        pairsOfFlags = newPairs;
    }

    struct StructType {
        uint[] contents;
        uint moreInfo;
    }
    StructType s;

    function f(uint[] memory c) public {
        // stores a reference to ``s`` in ``g``
        StructType storage g = s;
        // also changes ``s.moreInfo``.
        g.moreInfo = 2;
        // assigns a copy because ``g.contents``
        // is not a local variable, but a member of
        // a local variable.
        g.contents = c;
    }

    function setFlagPair(uint index, bool flagA, bool flagB) public {
        // access to a non-existing index will throw an exception
        pairsOfFlags[index][0] = flagA;
        pairsOfFlags[index][1] = flagB;
    }

    function changeFlagArraySize(uint newSize) public {
        // using push and pop is the only way to change the
        // length of an array
        if (newSize < pairsOfFlags.length) {
            while (pairsOfFlags.length > newSize)
                pairsOfFlags.pop();
        } else if (newSize > pairsOfFlags.length) {
            while (pairsOfFlags.length < newSize)
                pairsOfFlags.push();
        }
    }

    function clear() public {
        // these clear the arrays completely
        delete pairsOfFlags;
        delete aLotOfIntegers;
        // identical effect here
        pairsOfFlags = new bool[2][](0);
    }

    bytes byteData;

    function byteArrays(bytes memory data) public {
        // byte arrays ("bytes") are different as they are stored without padding,
        // but can be treated identical to "uint8[]"
        byteData = data;
        for (uint i = 0; i < 7; i++)
            byteData.push();
        byteData[3] = 0x08;
        delete byteData[2];
    }

    function addFlag(bool[2] memory flag) public returns (uint) {
        pairsOfFlags.push(flag);
        return pairsOfFlags.length;
    }

    function createMemoryArray(uint size) public pure returns (bytes memory) {
        // Dynamic memory arrays are created using `new`:
        uint[2][] memory arrayOfPairs = new uint[2][](size);

        // Inline arrays are always statically-sized and if you only
        // use literals, you have to provide at least one type.
        arrayOfPairs[0] = [uint(1), 2];

        // Create a dynamic byte array:
        bytes memory b = new bytes(200);
        for (uint i = 0; i < b.length; i++)
            b[i] = bytes1(uint8(i));
        return b;
    }
}

#### Dangling References to Storage Array Elements[](#dangling-references-to-storage-array-elements "Permalink to this heading")

When working with storage arrays, you need to take care to avoid dangling references. A dangling reference is a reference that points to something that no longer exists or has been moved without updating the reference. A dangling reference can for example occur, if you store a reference to an array element in a local variable and then `.pop()` from the containing array:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC44LjAgPDAuOS4wOwoKY29udHJhY3QgQyB7CiAgICB1aW50W11bXSBzOwoKICAgIGZ1bmN0aW9uIGYoKSBwdWJsaWMgewogICAgICAgIC8vIFN0b3JlcyBhIHBvaW50ZXIgdG8gdGhlIGxhc3QgYXJyYXkgZWxlbWVudCBvZiBzLgogICAgICAgIHVpbnRbXSBzdG9yYWdlIHB0ciA9IHNbcy5sZW5ndGggLSAxXTsKICAgICAgICAvLyBSZW1vdmVzIHRoZSBsYXN0IGFycmF5IGVsZW1lbnQgb2Ygcy4KICAgICAgICBzLnBvcCgpOwogICAgICAgIC8vIFdyaXRlcyB0byB0aGUgYXJyYXkgZWxlbWVudCB0aGF0IGlzIG5vIGxvbmdlciB3aXRoaW4gdGhlIGFycmF5LgogICAgICAgIHB0ci5wdXNoKDB4NDIpOwogICAgICAgIC8vIEFkZGluZyBhIG5ldyBlbGVtZW50IHRvIGBgc2BgIG5vdyB3aWxsIG5vdCBhZGQgYW4gZW1wdHkgYXJyYXksIGJ1dAogICAgICAgIC8vIHdpbGwgcmVzdWx0IGluIGFuIGFycmF5IG9mIGxlbmd0aCAxIHdpdGggYGAweDQyYGAgYXMgZWxlbWVudC4KICAgICAgICBzLnB1c2goKTsKICAgICAgICBhc3NlcnQoc1tzLmxlbmd0aCAtIDFdWzBdID09IDB4NDIpOwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.8.0 <0.9.0;

contract C {
    uint[][] s;

    function f() public {
        // Stores a pointer to the last array element of s.
        uint[] storage ptr = s[s.length - 1];
        // Removes the last array element of s.
        s.pop();
        // Writes to the array element that is no longer within the array.
        ptr.push(0x42);
        // Adding a new element to ``s`` now will not add an empty array, but
        // will result in an array of length 1 with ``0x42`` as element.
        s.push();
        assert(s[s.length - 1][0] == 0x42);
    }
}

The write in `ptr.push(0x42)` will **not** revert, despite the fact that `ptr` no longer refers to a valid element of `s`. Since the compiler assumes that unused storage is always zeroed, a subsequent `s.push()` will not explicitly write zeroes to storage, so the last element of `s` after that `push()` will have length `1` and contain `0x42` as its first element.

Note that Solidity does not allow to declare references to value types in storage. These kinds of explicit dangling references are restricted to nested reference types. However, dangling references can also occur temporarily when using complex expressions in tuple assignments:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC44LjAgPDAuOS4wOwoKY29udHJhY3QgQyB7CiAgICB1aW50W10gczsKICAgIHVpbnRbXSB0OwogICAgY29uc3RydWN0b3IoKSB7CiAgICAgICAgLy8gUHVzaCBzb21lIGluaXRpYWwgdmFsdWVzIHRvIHRoZSBzdG9yYWdlIGFycmF5cy4KICAgICAgICBzLnB1c2goMHgwNyk7CiAgICAgICAgdC5wdXNoKDB4MDMpOwogICAgfQoKICAgIGZ1bmN0aW9uIGcoKSBpbnRlcm5hbCByZXR1cm5zICh1aW50W10gc3RvcmFnZSkgewogICAgICAgIHMucG9wKCk7CiAgICAgICAgcmV0dXJuIHQ7CiAgICB9CgogICAgZnVuY3Rpb24gZigpIHB1YmxpYyByZXR1cm5zICh1aW50W10gbWVtb3J5KSB7CiAgICAgICAgLy8gVGhlIGZvbGxvd2luZyB3aWxsIGZpcnN0IGV2YWx1YXRlIGBgcy5wdXNoKClgYCB0byBhIHJlZmVyZW5jZSB0byBhIG5ldyBlbGVtZW50CiAgICAgICAgLy8gYXQgaW5kZXggMS4gQWZ0ZXJ3YXJkcywgdGhlIGNhbGwgdG8gYGBnYGAgcG9wcyB0aGlzIG5ldyBlbGVtZW50LCByZXN1bHRpbmcgaW4KICAgICAgICAvLyB0aGUgbGVmdC1tb3N0IHR1cGxlIGVsZW1lbnQgdG8gYmVjb21lIGEgZGFuZ2xpbmcgcmVmZXJlbmNlLiBUaGUgYXNzaWdubWVudCBzdGlsbAogICAgICAgIC8vIHRha2VzIHBsYWNlIGFuZCB3aWxsIHdyaXRlIG91dHNpZGUgdGhlIGRhdGEgYXJlYSBvZiBgYHNgYC4KICAgICAgICAocy5wdXNoKCksIGcoKVswXSkgPSAoMHg0MiwgMHgxNyk7CiAgICAgICAgLy8gQSBzdWJzZXF1ZW50IHB1c2ggdG8gYGBzYGAgd2lsbCByZXZlYWwgdGhlIHZhbHVlIHdyaXR0ZW4gYnkgdGhlIHByZXZpb3VzCiAgICAgICAgLy8gc3RhdGVtZW50LCBpLmUuIHRoZSBsYXN0IGVsZW1lbnQgb2YgYGBzYGAgYXQgdGhlIGVuZCBvZiB0aGlzIGZ1bmN0aW9uIHdpbGwgaGF2ZQogICAgICAgIC8vIHRoZSB2YWx1ZSBgYDB4NDJgYC4KICAgICAgICBzLnB1c2goKTsKICAgICAgICByZXR1cm4gczsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.8.0 <0.9.0;

contract C {
    uint[] s;
    uint[] t;
    constructor() {
        // Push some initial values to the storage arrays.
        s.push(0x07);
        t.push(0x03);
    }

    function g() internal returns (uint[] storage) {
        s.pop();
        return t;
    }

    function f() public returns (uint[] memory) {
        // The following will first evaluate ``s.push()`` to a reference to a new element
        // at index 1. Afterwards, the call to ``g`` pops this new element, resulting in
        // the left-most tuple element to become a dangling reference. The assignment still
        // takes place and will write outside the data area of ``s``.
        (s.push(), g()[0]) = (0x42, 0x17);
        // A subsequent push to ``s`` will reveal the value written by the previous
        // statement, i.e. the last element of ``s`` at the end of this function will have
        // the value ``0x42``.
        s.push();
        return s;
    }
}

It is always safer to only assign to storage once per statement and to avoid complex expressions on the left-hand-side of an assignment.

You need to take particular care when dealing with references to elements of `bytes` arrays, since a `.push()` on a bytes array may switch [from short to long layout in storage](internals/layout_in_storage.html#bytes-and-string).

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC44LjAgPDAuOS4wOwoKLy8gVGhpcyB3aWxsIHJlcG9ydCBhIHdhcm5pbmcKY29udHJhY3QgQyB7CiAgICBieXRlcyB4ID0gIjAxMjM0NTY3ODkwMTIzNDU2Nzg5MDEyMzQ1Njc4OSI7CgogICAgZnVuY3Rpb24gdGVzdCgpIGV4dGVybmFsIHJldHVybnModWludCkgewogICAgICAgICh4LnB1c2goKSwgeC5wdXNoKCkpID0gKDB4MDEsIDB4MDIpOwogICAgICAgIHJldHVybiB4Lmxlbmd0aDsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.8.0 <0.9.0;

// This will report a warning
contract C {
    bytes x = "012345678901234567890123456789";

    function test() external returns(uint) {
        (x.push(), x.push()) = (0x01, 0x02);
        return x.length;
    }
}

Here, when the first `x.push()` is evaluated, `x` is still stored in short layout, thereby `x.push()` returns a reference to an element in the first storage slot of `x`. However, the second `x.push()` switches the bytes array to large layout. Now the element that `x.push()` referred to is in the data area of the array while the reference still points at its original location, which is now a part of the length field and the assignment will effectively garble the length of `x`. To be safe, only enlarge bytes arrays by at most one element during a single assignment and do not simultaneously index-access the array in the same statement.

While the above describes the behavior of dangling storage references in the current version of the compiler, any code with dangling references should be considered to have _undefined behavior_. In particular, this means that any future version of the compiler may change the behavior of code that involves dangling references.

Be sure to avoid dangling references in your code!

### Array Slices[](#array-slices "Permalink to this heading")

Array slices are a view on a contiguous portion of an array. They are written as `x[start:end]`, where `start` and `end` are expressions resulting in a uint256 type (or implicitly convertible to it). The first element of the slice is `x[start]` and the last element is `x[end - 1]`.

If `start` is greater than `end` or if `end` is greater than the length of the array, an exception is thrown.

Both `start` and `end` are optional: `start` defaults to `0` and `end` defaults to the length of the array.

Array slices do not have any members. They are implicitly convertible to arrays of their underlying type and support index access. Index access is not absolute in the underlying array, but relative to the start of the slice.

Array slices do not have a type name which means no variable can have an array slices as type, they only exist in intermediate expressions.

Note

As of now, array slices are only implemented for calldata arrays.

Array slices are useful to ABI-decode secondary data passed in function parameters:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC44LjUgPDAuOS4wOwpjb250cmFjdCBQcm94eSB7CiAgICAvLy8gQGRldiBBZGRyZXNzIG9mIHRoZSBjbGllbnQgY29udHJhY3QgbWFuYWdlZCBieSBwcm94eSBpLmUuLCB0aGlzIGNvbnRyYWN0CiAgICBhZGRyZXNzIGNsaWVudDsKCiAgICBjb25zdHJ1Y3RvcihhZGRyZXNzIGNsaWVudF8pIHsKICAgICAgICBjbGllbnQgPSBjbGllbnRfOwogICAgfQoKICAgIC8vLyBGb3J3YXJkIGNhbGwgdG8gInNldE93bmVyKGFkZHJlc3MpIiB0aGF0IGlzIGltcGxlbWVudGVkIGJ5IGNsaWVudAogICAgLy8vIGFmdGVyIGRvaW5nIGJhc2ljIHZhbGlkYXRpb24gb24gdGhlIGFkZHJlc3MgYXJndW1lbnQuCiAgICBmdW5jdGlvbiBmb3J3YXJkKGJ5dGVzIGNhbGxkYXRhIHBheWxvYWQpIGV4dGVybmFsIHsKICAgICAgICBieXRlczQgc2lnID0gYnl0ZXM0KHBheWxvYWRbOjRdKTsKICAgICAgICAvLyBEdWUgdG8gdHJ1bmNhdGluZyBiZWhhdmlvciwgYnl0ZXM0KHBheWxvYWQpIHBlcmZvcm1zIGlkZW50aWNhbGx5LgogICAgICAgIC8vIGJ5dGVzNCBzaWcgPSBieXRlczQocGF5bG9hZCk7CiAgICAgICAgaWYgKHNpZyA9PSBieXRlczQoa2VjY2FrMjU2KCJzZXRPd25lcihhZGRyZXNzKSIpKSkgewogICAgICAgICAgICBhZGRyZXNzIG93bmVyID0gYWJpLmRlY29kZShwYXlsb2FkWzQ6XSwgKGFkZHJlc3MpKTsKICAgICAgICAgICAgcmVxdWlyZShvd25lciAhPSBhZGRyZXNzKDApLCAiQWRkcmVzcyBvZiBvd25lciBjYW5ub3QgYmUgemVyby4iKTsKICAgICAgICB9CiAgICAgICAgKGJvb2wgc3RhdHVzLCkgPSBjbGllbnQuZGVsZWdhdGVjYWxsKHBheWxvYWQpOwogICAgICAgIHJlcXVpcmUoc3RhdHVzLCAiRm9yd2FyZGVkIGNhbGwgZmFpbGVkLiIpOwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.8.5 <0.9.0;
contract Proxy {
    /// @dev Address of the client contract managed by proxy i.e., this contract
    address client;

    constructor(address client_) {
        client = client_;
    }

    /// Forward call to "setOwner(address)" that is implemented by client
    /// after doing basic validation on the address argument.
    function forward(bytes calldata payload) external {
        bytes4 sig = bytes4(payload[:4]);
        // Due to truncating behavior, bytes4(payload) performs identically.
        // bytes4 sig = bytes4(payload);
        if (sig == bytes4(keccak256("setOwner(address)"))) {
            address owner = abi.decode(payload[4:], (address));
            require(owner != address(0), "Address of owner cannot be zero.");
        }
        (bool status,) = client.delegatecall(payload);
        require(status, "Forwarded call failed.");
    }
}

### Structs[](#structs "Permalink to this heading")

Solidity provides a way to define new types in the form of structs, which is shown in the following example:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKLy8gRGVmaW5lcyBhIG5ldyB0eXBlIHdpdGggdHdvIGZpZWxkcy4KLy8gRGVjbGFyaW5nIGEgc3RydWN0IG91dHNpZGUgb2YgYSBjb250cmFjdCBhbGxvd3MKLy8gaXQgdG8gYmUgc2hhcmVkIGJ5IG11bHRpcGxlIGNvbnRyYWN0cy4KLy8gSGVyZSwgdGhpcyBpcyBub3QgcmVhbGx5IG5lZWRlZC4Kc3RydWN0IEZ1bmRlciB7CiAgICBhZGRyZXNzIGFkZHI7CiAgICB1aW50IGFtb3VudDsKfQoKY29udHJhY3QgQ3Jvd2RGdW5kaW5nIHsKICAgIC8vIFN0cnVjdHMgY2FuIGFsc28gYmUgZGVmaW5lZCBpbnNpZGUgY29udHJhY3RzLCB3aGljaCBtYWtlcyB0aGVtCiAgICAvLyB2aXNpYmxlIG9ubHkgdGhlcmUgYW5kIGluIGRlcml2ZWQgY29udHJhY3RzLgogICAgc3RydWN0IENhbXBhaWduIHsKICAgICAgICBhZGRyZXNzIHBheWFibGUgYmVuZWZpY2lhcnk7CiAgICAgICAgdWludCBmdW5kaW5nR29hbDsKICAgICAgICB1aW50IG51bUZ1bmRlcnM7CiAgICAgICAgdWludCBhbW91bnQ7CiAgICAgICAgbWFwcGluZyh1aW50ID0+IEZ1bmRlcikgZnVuZGVyczsKICAgIH0KCiAgICB1aW50IG51bUNhbXBhaWduczsKICAgIG1hcHBpbmcodWludCA9PiBDYW1wYWlnbikgY2FtcGFpZ25zOwoKICAgIGZ1bmN0aW9uIG5ld0NhbXBhaWduKGFkZHJlc3MgcGF5YWJsZSBiZW5lZmljaWFyeSwgdWludCBnb2FsKSBwdWJsaWMgcmV0dXJucyAodWludCBjYW1wYWlnbklEKSB7CiAgICAgICAgY2FtcGFpZ25JRCA9IG51bUNhbXBhaWducysrOyAvLyBjYW1wYWlnbklEIGlzIHJldHVybiB2YXJpYWJsZQogICAgICAgIC8vIFdlIGNhbm5vdCB1c2UgImNhbXBhaWduc1tjYW1wYWlnbklEXSA9IENhbXBhaWduKGJlbmVmaWNpYXJ5LCBnb2FsLCAwLCAwKSIKICAgICAgICAvLyBiZWNhdXNlIHRoZSByaWdodCBoYW5kIHNpZGUgY3JlYXRlcyBhIG1lbW9yeS1zdHJ1Y3QgIkNhbXBhaWduIiB0aGF0IGNvbnRhaW5zIGEgbWFwcGluZy4KICAgICAgICBDYW1wYWlnbiBzdG9yYWdlIGMgPSBjYW1wYWlnbnNbY2FtcGFpZ25JRF07CiAgICAgICAgYy5iZW5lZmljaWFyeSA9IGJlbmVmaWNpYXJ5OwogICAgICAgIGMuZnVuZGluZ0dvYWwgPSBnb2FsOwogICAgfQoKICAgIGZ1bmN0aW9uIGNvbnRyaWJ1dGUodWludCBjYW1wYWlnbklEKSBwdWJsaWMgcGF5YWJsZSB7CiAgICAgICAgQ2FtcGFpZ24gc3RvcmFnZSBjID0gY2FtcGFpZ25zW2NhbXBhaWduSURdOwogICAgICAgIC8vIENyZWF0ZXMgYSBuZXcgdGVtcG9yYXJ5IG1lbW9yeSBzdHJ1Y3QsIGluaXRpYWxpc2VkIHdpdGggdGhlIGdpdmVuIHZhbHVlcwogICAgICAgIC8vIGFuZCBjb3BpZXMgaXQgb3ZlciB0byBzdG9yYWdlLgogICAgICAgIC8vIE5vdGUgdGhhdCB5b3UgY2FuIGFsc28gdXNlIEZ1bmRlcihtc2cuc2VuZGVyLCBtc2cudmFsdWUpIHRvIGluaXRpYWxpc2UuCiAgICAgICAgYy5mdW5kZXJzW2MubnVtRnVuZGVycysrXSA9IEZ1bmRlcih7YWRkcjogbXNnLnNlbmRlciwgYW1vdW50OiBtc2cudmFsdWV9KTsKICAgICAgICBjLmFtb3VudCArPSBtc2cudmFsdWU7CiAgICB9CgogICAgZnVuY3Rpb24gY2hlY2tHb2FsUmVhY2hlZCh1aW50IGNhbXBhaWduSUQpIHB1YmxpYyByZXR1cm5zIChib29sIHJlYWNoZWQpIHsKICAgICAgICBDYW1wYWlnbiBzdG9yYWdlIGMgPSBjYW1wYWlnbnNbY2FtcGFpZ25JRF07CiAgICAgICAgaWYgKGMuYW1vdW50IDwgYy5mdW5kaW5nR29hbCkKICAgICAgICAgICAgcmV0dXJuIGZhbHNlOwogICAgICAgIHVpbnQgYW1vdW50ID0gYy5hbW91bnQ7CiAgICAgICAgYy5hbW91bnQgPSAwOwogICAgICAgIGMuYmVuZWZpY2lhcnkudHJhbnNmZXIoYW1vdW50KTsKICAgICAgICByZXR1cm4gdHJ1ZTsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

// Defines a new type with two fields.
// Declaring a struct outside of a contract allows
// it to be shared by multiple contracts.
// Here, this is not really needed.
struct Funder {
    address addr;
    uint amount;
}

contract CrowdFunding {
    // Structs can also be defined inside contracts, which makes them
    // visible only there and in derived contracts.
    struct Campaign {
        address payable beneficiary;
        uint fundingGoal;
        uint numFunders;
        uint amount;
        mapping(uint => Funder) funders;
    }

    uint numCampaigns;
    mapping(uint => Campaign) campaigns;

    function newCampaign(address payable beneficiary, uint goal) public returns (uint campaignID) {
        campaignID = numCampaigns++; // campaignID is return variable
        // We cannot use "campaigns[campaignID] = Campaign(beneficiary, goal, 0, 0)"
        // because the right hand side creates a memory-struct "Campaign" that contains a mapping.
        Campaign storage c = campaigns[campaignID];
        c.beneficiary = beneficiary;
        c.fundingGoal = goal;
    }

    function contribute(uint campaignID) public payable {
        Campaign storage c = campaigns[campaignID];
        // Creates a new temporary memory struct, initialised with the given values
        // and copies it over to storage.
        // Note that you can also use Funder(msg.sender, msg.value) to initialise.
        c.funders[c.numFunders++] = Funder({addr: msg.sender, amount: msg.value});
        c.amount += msg.value;
    }

    function checkGoalReached(uint campaignID) public returns (bool reached) {
        Campaign storage c = campaigns[campaignID];
        if (c.amount < c.fundingGoal)
            return false;
        uint amount = c.amount;
        c.amount = 0;
        c.beneficiary.transfer(amount);
        return true;
    }
}

The contract does not provide the full functionality of a crowdfunding contract, but it contains the basic concepts necessary to understand structs. Struct types can be used inside mappings and arrays and they can themselves contain mappings and arrays.

It is not possible for a struct to contain a member of its own type, although the struct itself can be the value type of a mapping member or it can contain a dynamically-sized array of its type. This restriction is necessary, as the size of the struct has to be finite.

Note how in all the functions, a struct type is assigned to a local variable with data location `storage`. This does not copy the struct but only stores a reference so that assignments to members of the local variable actually write to the state.

Of course, you can also directly access the members of the struct without assigning it to a local variable, as in `campaigns[campaignID].amount = 0`.

Note

Until Solidity 0.7.0, memory-structs containing members of storage-only types (e.g. mappings) were allowed and assignments like `campaigns[campaignID] = Campaign(beneficiary, goal, 0, 0)` in the example above would work and just silently skip those members.

## Mapping Types[](#mapping-types "Permalink to this heading")

Mapping types use the syntax `mapping(KeyType KeyName? => ValueType ValueName?)` and variables of mapping type are declared using the syntax `mapping(KeyType KeyName? => ValueType ValueName?) VariableName`. The `KeyType` can be any built-in value type, `bytes`, `string`, or any contract or enum type. Other user-defined or complex types, such as mappings, structs or array types are not allowed. `ValueType` can be any type, including mappings, arrays and structs. `KeyName` and `ValueName` are optional (so `mapping(KeyType => ValueType)` works as well) and can be any valid identifier that is not a type.

You can think of mappings as [hash tables](https://en.wikipedia.org/wiki/Hash_table), which are virtually initialised such that every possible key exists and is mapped to a value whose byte-representation is all zeros, a type’s [default value](control-structures.html#default-value). The similarity ends there, the key data is not stored in a mapping, only its `keccak256` hash is used to look up the value.

Because of this, mappings do not have a length or a concept of a key or value being set, and therefore cannot be erased without extra information regarding the assigned keys (see [Clearing Mappings](security-considerations.html#clearing-mappings)).

Mappings can only have a data location of `storage` and thus are allowed for state variables, as storage reference types in functions, or as parameters for library functions. They cannot be used as parameters or return parameters of contract functions that are publicly visible. These restrictions are also true for arrays and structs that contain mappings.

You can mark state variables of mapping type as `public` and Solidity creates a [getter](contracts.html#visibility-and-getters) for you. The `KeyType` becomes a parameter with name `KeyName` (if specified) for the getter. If `ValueType` is a value type or a struct, the getter returns `ValueType` with name `ValueName` (if specified). If `ValueType` is an array or a mapping, the getter has one parameter for each `KeyType`, recursively.

In the example below, the `MappingExample` contract defines a public `balances` mapping, with the key type an `address`, and a value type a `uint`, mapping an Ethereum address to an unsigned integer value. As `uint` is a value type, the getter returns a value that matches the type, which you can see in the `MappingUser` contract that returns the value at the specified address.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKY29udHJhY3QgTWFwcGluZ0V4YW1wbGUgewogICAgbWFwcGluZyhhZGRyZXNzID0+IHVpbnQpIHB1YmxpYyBiYWxhbmNlczsKCiAgICBmdW5jdGlvbiB1cGRhdGUodWludCBuZXdCYWxhbmNlKSBwdWJsaWMgewogICAgICAgIGJhbGFuY2VzW21zZy5zZW5kZXJdID0gbmV3QmFsYW5jZTsKICAgIH0KfQoKY29udHJhY3QgTWFwcGluZ1VzZXIgewogICAgZnVuY3Rpb24gZigpIHB1YmxpYyByZXR1cm5zICh1aW50KSB7CiAgICAgICAgTWFwcGluZ0V4YW1wbGUgbSA9IG5ldyBNYXBwaW5nRXhhbXBsZSgpOwogICAgICAgIG0udXBkYXRlKDEwMCk7CiAgICAgICAgcmV0dXJuIG0uYmFsYW5jZXMoYWRkcmVzcyh0aGlzKSk7CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract MappingExample {
    mapping(address => uint) public balances;

    function update(uint newBalance) public {
        balances[msg.sender] = newBalance;
    }
}

contract MappingUser {
    function f() public returns (uint) {
        MappingExample m = new MappingExample();
        m.update(100);
        return m.balances(address(this));
    }
}

The example below is a simplified version of an [ERC20 token](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol). `_allowances` is an example of a mapping type inside another mapping type.

In the example below, the optional `KeyName` and `ValueName` are provided for the mapping. It does not affect any contract functionality or bytecode, it only sets the `name` field for the inputs and outputs in the ABI for the mapping’s getter.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguMTg7Cgpjb250cmFjdCBNYXBwaW5nRXhhbXBsZVdpdGhOYW1lcyB7CiAgICBtYXBwaW5nKGFkZHJlc3MgdXNlciA9PiB1aW50IGJhbGFuY2UpIHB1YmxpYyBiYWxhbmNlczsKCiAgICBmdW5jdGlvbiB1cGRhdGUodWludCBuZXdCYWxhbmNlKSBwdWJsaWMgewogICAgICAgIGJhbGFuY2VzW21zZy5zZW5kZXJdID0gbmV3QmFsYW5jZTsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.18;

contract MappingExampleWithNames {
    mapping(address user => uint balance) public balances;

    function update(uint newBalance) public {
        balances[msg.sender] = newBalance;
    }
}

The example below uses `_allowances` to record the amount someone else is allowed to withdraw from your account.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjIyIDwwLjkuMDsKCmNvbnRyYWN0IE1hcHBpbmdFeGFtcGxlIHsKCiAgICBtYXBwaW5nKGFkZHJlc3MgPT4gdWludDI1NikgcHJpdmF0ZSBfYmFsYW5jZXM7CiAgICBtYXBwaW5nKGFkZHJlc3MgPT4gbWFwcGluZyhhZGRyZXNzID0+IHVpbnQyNTYpKSBwcml2YXRlIF9hbGxvd2FuY2VzOwoKICAgIGV2ZW50IFRyYW5zZmVyKGFkZHJlc3MgaW5kZXhlZCBmcm9tLCBhZGRyZXNzIGluZGV4ZWQgdG8sIHVpbnQyNTYgdmFsdWUpOwogICAgZXZlbnQgQXBwcm92YWwoYWRkcmVzcyBpbmRleGVkIG93bmVyLCBhZGRyZXNzIGluZGV4ZWQgc3BlbmRlciwgdWludDI1NiB2YWx1ZSk7CgogICAgZnVuY3Rpb24gYWxsb3dhbmNlKGFkZHJlc3Mgb3duZXIsIGFkZHJlc3Mgc3BlbmRlcikgcHVibGljIHZpZXcgcmV0dXJucyAodWludDI1NikgewogICAgICAgIHJldHVybiBfYWxsb3dhbmNlc1tvd25lcl1bc3BlbmRlcl07CiAgICB9CgogICAgZnVuY3Rpb24gdHJhbnNmZXJGcm9tKGFkZHJlc3Mgc2VuZGVyLCBhZGRyZXNzIHJlY2lwaWVudCwgdWludDI1NiBhbW91bnQpIHB1YmxpYyByZXR1cm5zIChib29sKSB7CiAgICAgICAgcmVxdWlyZShfYWxsb3dhbmNlc1tzZW5kZXJdW21zZy5zZW5kZXJdID49IGFtb3VudCwgIkVSQzIwOiBBbGxvd2FuY2Ugbm90IGhpZ2ggZW5vdWdoLiIpOwogICAgICAgIF9hbGxvd2FuY2VzW3NlbmRlcl1bbXNnLnNlbmRlcl0gLT0gYW1vdW50OwogICAgICAgIF90cmFuc2ZlcihzZW5kZXIsIHJlY2lwaWVudCwgYW1vdW50KTsKICAgICAgICByZXR1cm4gdHJ1ZTsKICAgIH0KCiAgICBmdW5jdGlvbiBhcHByb3ZlKGFkZHJlc3Mgc3BlbmRlciwgdWludDI1NiBhbW91bnQpIHB1YmxpYyByZXR1cm5zIChib29sKSB7CiAgICAgICAgcmVxdWlyZShzcGVuZGVyICE9IGFkZHJlc3MoMCksICJFUkMyMDogYXBwcm92ZSB0byB0aGUgemVybyBhZGRyZXNzIik7CgogICAgICAgIF9hbGxvd2FuY2VzW21zZy5zZW5kZXJdW3NwZW5kZXJdID0gYW1vdW50OwogICAgICAgIGVtaXQgQXBwcm92YWwobXNnLnNlbmRlciwgc3BlbmRlciwgYW1vdW50KTsKICAgICAgICByZXR1cm4gdHJ1ZTsKICAgIH0KCiAgICBmdW5jdGlvbiBfdHJhbnNmZXIoYWRkcmVzcyBzZW5kZXIsIGFkZHJlc3MgcmVjaXBpZW50LCB1aW50MjU2IGFtb3VudCkgaW50ZXJuYWwgewogICAgICAgIHJlcXVpcmUoc2VuZGVyICE9IGFkZHJlc3MoMCksICJFUkMyMDogdHJhbnNmZXIgZnJvbSB0aGUgemVybyBhZGRyZXNzIik7CiAgICAgICAgcmVxdWlyZShyZWNpcGllbnQgIT0gYWRkcmVzcygwKSwgIkVSQzIwOiB0cmFuc2ZlciB0byB0aGUgemVybyBhZGRyZXNzIik7CiAgICAgICAgcmVxdWlyZShfYmFsYW5jZXNbc2VuZGVyXSA+PSBhbW91bnQsICJFUkMyMDogTm90IGVub3VnaCBmdW5kcy4iKTsKCiAgICAgICAgX2JhbGFuY2VzW3NlbmRlcl0gLT0gYW1vdW50OwogICAgICAgIF9iYWxhbmNlc1tyZWNpcGllbnRdICs9IGFtb3VudDsKICAgICAgICBlbWl0IFRyYW5zZmVyKHNlbmRlciwgcmVjaXBpZW50LCBhbW91bnQpOwogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.22 <0.9.0;

contract MappingExample {

    mapping(address => uint256) private _balances;
    mapping(address => mapping(address => uint256)) private _allowances;

    event Transfer(address indexed from, address indexed to, uint256 value);
    event Approval(address indexed owner, address indexed spender, uint256 value);

    function allowance(address owner, address spender) public view returns (uint256) {
        return _allowances[owner][spender];
    }

    function transferFrom(address sender, address recipient, uint256 amount) public returns (bool) {
        require(_allowances[sender][msg.sender] >= amount, "ERC20: Allowance not high enough.");
        _allowances[sender][msg.sender] -= amount;
        _transfer(sender, recipient, amount);
        return true;
    }

    function approve(address spender, uint256 amount) public returns (bool) {
        require(spender != address(0), "ERC20: approve to the zero address");

        _allowances[msg.sender][spender] = amount;
        emit Approval(msg.sender, spender, amount);
        return true;
    }

    function _transfer(address sender, address recipient, uint256 amount) internal {
        require(sender != address(0), "ERC20: transfer from the zero address");
        require(recipient != address(0), "ERC20: transfer to the zero address");
        require(_balances[sender] >= amount, "ERC20: Not enough funds.");

        _balances[sender] -= amount;
        _balances[recipient] += amount;
        emit Transfer(sender, recipient, amount);
    }
}

### Iterable Mappings[](#iterable-mappings "Permalink to this heading")

You cannot iterate over mappings, i.e. you cannot enumerate their keys. It is possible, though, to implement a data structure on top of them and iterate over that. For example, the code below implements an `IterableMapping` library that the `User` contract then adds data to, and the `sum` function iterates over to sum all the values.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguODsKCnN0cnVjdCBJbmRleFZhbHVlIHsgdWludCBrZXlJbmRleDsgdWludCB2YWx1ZTsgfQpzdHJ1Y3QgS2V5RmxhZyB7IHVpbnQga2V5OyBib29sIGRlbGV0ZWQ7IH0KCnN0cnVjdCBpdG1hcCB7CiAgICBtYXBwaW5nKHVpbnQgPT4gSW5kZXhWYWx1ZSkgZGF0YTsKICAgIEtleUZsYWdbXSBrZXlzOwogICAgdWludCBzaXplOwp9Cgp0eXBlIEl0ZXJhdG9yIGlzIHVpbnQ7CgpsaWJyYXJ5IEl0ZXJhYmxlTWFwcGluZyB7CiAgICBmdW5jdGlvbiBpbnNlcnQoaXRtYXAgc3RvcmFnZSBzZWxmLCB1aW50IGtleSwgdWludCB2YWx1ZSkgaW50ZXJuYWwgcmV0dXJucyAoYm9vbCByZXBsYWNlZCkgewogICAgICAgIHVpbnQga2V5SW5kZXggPSBzZWxmLmRhdGFba2V5XS5rZXlJbmRleDsKICAgICAgICBzZWxmLmRhdGFba2V5XS52YWx1ZSA9IHZhbHVlOwogICAgICAgIGlmIChrZXlJbmRleCA+IDApCiAgICAgICAgICAgIHJldHVybiB0cnVlOwogICAgICAgIGVsc2UgewogICAgICAgICAgICBrZXlJbmRleCA9IHNlbGYua2V5cy5sZW5ndGg7CiAgICAgICAgICAgIHNlbGYua2V5cy5wdXNoKCk7CiAgICAgICAgICAgIHNlbGYuZGF0YVtrZXldLmtleUluZGV4ID0ga2V5SW5kZXggKyAxOwogICAgICAgICAgICBzZWxmLmtleXNba2V5SW5kZXhdLmtleSA9IGtleTsKICAgICAgICAgICAgc2VsZi5zaXplKys7CiAgICAgICAgICAgIHJldHVybiBmYWxzZTsKICAgICAgICB9CiAgICB9CgogICAgZnVuY3Rpb24gcmVtb3ZlKGl0bWFwIHN0b3JhZ2Ugc2VsZiwgdWludCBrZXkpIGludGVybmFsIHJldHVybnMgKGJvb2wgc3VjY2VzcykgewogICAgICAgIHVpbnQga2V5SW5kZXggPSBzZWxmLmRhdGFba2V5XS5rZXlJbmRleDsKICAgICAgICBpZiAoa2V5SW5kZXggPT0gMCkKICAgICAgICAgICAgcmV0dXJuIGZhbHNlOwogICAgICAgIGRlbGV0ZSBzZWxmLmRhdGFba2V5XTsKICAgICAgICBzZWxmLmtleXNba2V5SW5kZXggLSAxXS5kZWxldGVkID0gdHJ1ZTsKICAgICAgICBzZWxmLnNpemUgLS07CiAgICB9CgogICAgZnVuY3Rpb24gY29udGFpbnMoaXRtYXAgc3RvcmFnZSBzZWxmLCB1aW50IGtleSkgaW50ZXJuYWwgdmlldyByZXR1cm5zIChib29sKSB7CiAgICAgICAgcmV0dXJuIHNlbGYuZGF0YVtrZXldLmtleUluZGV4ID4gMDsKICAgIH0KCiAgICBmdW5jdGlvbiBpdGVyYXRlU3RhcnQoaXRtYXAgc3RvcmFnZSBzZWxmKSBpbnRlcm5hbCB2aWV3IHJldHVybnMgKEl0ZXJhdG9yKSB7CiAgICAgICAgcmV0dXJuIGl0ZXJhdG9yU2tpcERlbGV0ZWQoc2VsZiwgMCk7CiAgICB9CgogICAgZnVuY3Rpb24gaXRlcmF0ZVZhbGlkKGl0bWFwIHN0b3JhZ2Ugc2VsZiwgSXRlcmF0b3IgaXRlcmF0b3IpIGludGVybmFsIHZpZXcgcmV0dXJucyAoYm9vbCkgewogICAgICAgIHJldHVybiBJdGVyYXRvci51bndyYXAoaXRlcmF0b3IpIDwgc2VsZi5rZXlzLmxlbmd0aDsKICAgIH0KCiAgICBmdW5jdGlvbiBpdGVyYXRlTmV4dChpdG1hcCBzdG9yYWdlIHNlbGYsIEl0ZXJhdG9yIGl0ZXJhdG9yKSBpbnRlcm5hbCB2aWV3IHJldHVybnMgKEl0ZXJhdG9yKSB7CiAgICAgICAgcmV0dXJuIGl0ZXJhdG9yU2tpcERlbGV0ZWQoc2VsZiwgSXRlcmF0b3IudW53cmFwKGl0ZXJhdG9yKSArIDEpOwogICAgfQoKICAgIGZ1bmN0aW9uIGl0ZXJhdGVHZXQoaXRtYXAgc3RvcmFnZSBzZWxmLCBJdGVyYXRvciBpdGVyYXRvcikgaW50ZXJuYWwgdmlldyByZXR1cm5zICh1aW50IGtleSwgdWludCB2YWx1ZSkgewogICAgICAgIHVpbnQga2V5SW5kZXggPSBJdGVyYXRvci51bndyYXAoaXRlcmF0b3IpOwogICAgICAgIGtleSA9IHNlbGYua2V5c1trZXlJbmRleF0ua2V5OwogICAgICAgIHZhbHVlID0gc2VsZi5kYXRhW2tleV0udmFsdWU7CiAgICB9CgogICAgZnVuY3Rpb24gaXRlcmF0b3JTa2lwRGVsZXRlZChpdG1hcCBzdG9yYWdlIHNlbGYsIHVpbnQga2V5SW5kZXgpIHByaXZhdGUgdmlldyByZXR1cm5zIChJdGVyYXRvcikgewogICAgICAgIHdoaWxlIChrZXlJbmRleCA8IHNlbGYua2V5cy5sZW5ndGggJiYgc2VsZi5rZXlzW2tleUluZGV4XS5kZWxldGVkKQogICAgICAgICAgICBrZXlJbmRleCsrOwogICAgICAgIHJldHVybiBJdGVyYXRvci53cmFwKGtleUluZGV4KTsKICAgIH0KfQoKLy8gSG93IHRvIHVzZSBpdApjb250cmFjdCBVc2VyIHsKICAgIC8vIEp1c3QgYSBzdHJ1Y3QgaG9sZGluZyBvdXIgZGF0YS4KICAgIGl0bWFwIGRhdGE7CiAgICAvLyBBcHBseSBsaWJyYXJ5IGZ1bmN0aW9ucyB0byB0aGUgZGF0YSB0eXBlLgogICAgdXNpbmcgSXRlcmFibGVNYXBwaW5nIGZvciBpdG1hcDsKCiAgICAvLyBJbnNlcnQgc29tZXRoaW5nCiAgICBmdW5jdGlvbiBpbnNlcnQodWludCBrLCB1aW50IHYpIHB1YmxpYyByZXR1cm5zICh1aW50IHNpemUpIHsKICAgICAgICAvLyBUaGlzIGNhbGxzIEl0ZXJhYmxlTWFwcGluZy5pbnNlcnQoZGF0YSwgaywgdikKICAgICAgICBkYXRhLmluc2VydChrLCB2KTsKICAgICAgICAvLyBXZSBjYW4gc3RpbGwgYWNjZXNzIG1lbWJlcnMgb2YgdGhlIHN0cnVjdCwKICAgICAgICAvLyBidXQgd2Ugc2hvdWxkIHRha2UgY2FyZSBub3QgdG8gbWVzcyB3aXRoIHRoZW0uCiAgICAgICAgcmV0dXJuIGRhdGEuc2l6ZTsKICAgIH0KCiAgICAvLyBDb21wdXRlcyB0aGUgc3VtIG9mIGFsbCBzdG9yZWQgZGF0YS4KICAgIGZ1bmN0aW9uIHN1bSgpIHB1YmxpYyB2aWV3IHJldHVybnMgKHVpbnQgcykgewogICAgICAgIGZvciAoCiAgICAgICAgICAgIEl0ZXJhdG9yIGkgPSBkYXRhLml0ZXJhdGVTdGFydCgpOwogICAgICAgICAgICBkYXRhLml0ZXJhdGVWYWxpZChpKTsKICAgICAgICAgICAgaSA9IGRhdGEuaXRlcmF0ZU5leHQoaSkKICAgICAgICApIHsKICAgICAgICAgICAgKCwgdWludCB2YWx1ZSkgPSBkYXRhLml0ZXJhdGVHZXQoaSk7CiAgICAgICAgICAgIHMgKz0gdmFsdWU7CiAgICAgICAgfQogICAgfQp9)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.8;

struct IndexValue { uint keyIndex; uint value; }
struct KeyFlag { uint key; bool deleted; }

struct itmap {
    mapping(uint => IndexValue) data;
    KeyFlag[] keys;
    uint size;
}

type Iterator is uint;

library IterableMapping {
    function insert(itmap storage self, uint key, uint value) internal returns (bool replaced) {
        uint keyIndex = self.data[key].keyIndex;
        self.data[key].value = value;
        if (keyIndex > 0)
            return true;
        else {
            keyIndex = self.keys.length;
            self.keys.push();
            self.data[key].keyIndex = keyIndex + 1;
            self.keys[keyIndex].key = key;
            self.size++;
            return false;
        }
    }

    function remove(itmap storage self, uint key) internal returns (bool success) {
        uint keyIndex = self.data[key].keyIndex;
        if (keyIndex == 0)
            return false;
        delete self.data[key];
        self.keys[keyIndex - 1].deleted = true;
        self.size --;
    }

    function contains(itmap storage self, uint key) internal view returns (bool) {
        return self.data[key].keyIndex > 0;
    }

    function iterateStart(itmap storage self) internal view returns (Iterator) {
        return iteratorSkipDeleted(self, 0);
    }

    function iterateValid(itmap storage self, Iterator iterator) internal view returns (bool) {
        return Iterator.unwrap(iterator) < self.keys.length;
    }

    function iterateNext(itmap storage self, Iterator iterator) internal view returns (Iterator) {
        return iteratorSkipDeleted(self, Iterator.unwrap(iterator) + 1);
    }

    function iterateGet(itmap storage self, Iterator iterator) internal view returns (uint key, uint value) {
        uint keyIndex = Iterator.unwrap(iterator);
        key = self.keys[keyIndex].key;
        value = self.data[key].value;
    }

    function iteratorSkipDeleted(itmap storage self, uint keyIndex) private view returns (Iterator) {
        while (keyIndex < self.keys.length && self.keys[keyIndex].deleted)
            keyIndex++;
        return Iterator.wrap(keyIndex);
    }
}

// How to use it
contract User {
    // Just a struct holding our data.
    itmap data;
    // Apply library functions to the data type.
    using IterableMapping for itmap;

    // Insert something
    function insert(uint k, uint v) public returns (uint size) {
        // This calls IterableMapping.insert(data, k, v)
        data.insert(k, v);
        // We can still access members of the struct,
        // but we should take care not to mess with them.
        return data.size;
    }

    // Computes the sum of all stored data.
    function sum() public view returns (uint s) {
        for (
            Iterator i = data.iterateStart();
            data.iterateValid(i);
            i = data.iterateNext(i)
        ) {
            (, uint value) = data.iterateGet(i);
            s += value;
        }
    }
}

## Operators[](#operators "Permalink to this heading")

Arithmetic and bit operators can be applied even if the two operands do not have the same type. For example, you can compute `y = x + z`, where `x` is a `uint8` and `z` has the type `uint32`. In these cases, the following mechanism will be used to determine the type in which the operation is computed (this is important in case of overflow) and the type of the operator’s result:

1. If the type of the right operand can be implicitly converted to the type of the left operand, use the type of the left operand,
    
2. if the type of the left operand can be implicitly converted to the type of the right operand, use the type of the right operand,
    
3. otherwise, the operation is not allowed.
    

In case one of the operands is a [literal number](#rational-literals) it is first converted to its “mobile type”, which is the smallest type that can hold the value (unsigned types of the same bit-width are considered “smaller” than the signed types). If both are literal numbers, the operation is computed with effectively unlimited precision in that the expression is evaluated to whatever precision is necessary so that none is lost when the result is used with a non-literal type.

The operator’s result type is the same as the type the operation is performed in, except for comparison operators where the result is always `bool`.

The operators `**` (exponentiation), `<<` and `>>` use the type of the left operand for the operation and the result.

### Ternary Operator[](#ternary-operator "Permalink to this heading")

The ternary operator is used in expressions of the form `<expression> ? <trueExpression> : <falseExpression>`. It evaluates one of the latter two given expressions depending upon the result of the evaluation of the main `<expression>`. If `<expression>` evaluates to `true`, then `<trueExpression>` will be evaluated, otherwise `<falseExpression>` is evaluated.

The result of the ternary operator does not have a rational number type, even if all of its operands are rational number literals. The result type is determined from the types of the two operands in the same way as above, converting to their mobile type first if required.

As a consequence, `255 + (true ? 1 : 0)` will revert due to arithmetic overflow. The reason is that `(true ? 1 : 0)` is of `uint8` type, which forces the addition to be performed in `uint8` as well, and 256 exceeds the range allowed for this type.

Another consequence is that an expression like `1.5 + 1.5` is valid but `1.5 + (true ? 1.5 : 2.5)` is not. This is because the former is a rational expression evaluated in unlimited precision and only its final value matters. The latter involves a conversion of a fractional rational number to an integer, which is currently disallowed.

### Compound and Increment/Decrement Operators[](#compound-and-increment-decrement-operators "Permalink to this heading")

If `a` is an LValue (i.e. a variable or something that can be assigned to), the following operators are available as shorthands:

`a += e` is equivalent to `a = a + e`. The operators `-=`, `*=`, `/=`, `%=`, `|=`, `&=`, `^=`, `<<=` and `>>=` are defined accordingly. `a++` and `a--` are equivalent to `a += 1` / `a -= 1` but the expression itself still has the previous value of `a`. In contrast, `--a` and `++a` have the same effect on `a` but return the value after the change.

### delete[](#delete "Permalink to this heading")

`delete a` assigns the initial value for the type to `a`. I.e. for integers it is equivalent to `a = 0`, but it can also be used on arrays, where it assigns a dynamic array of length zero or a static array of the same length with all elements set to their initial value. `delete a[x]` deletes the item at index `x` of the array and leaves all other elements and the length of the array untouched. This especially means that it leaves a gap in the array. If you plan to remove items, a [mapping](#mapping-types) is probably a better choice.

For structs, it assigns a struct with all members reset. In other words, the value of `a` after `delete a` is the same as if `a` would be declared without assignment, with the following caveat:

`delete` has no effect on mappings (as the keys of mappings may be arbitrary and are generally unknown). So if you delete a struct, it will reset all members that are not mappings and also recurse into the members unless they are mappings. However, individual keys and what they map to can be deleted: If `a` is a mapping, then `delete a[x]` will delete the value stored at `x`.

It is important to note that `delete a` really behaves like an assignment to `a`, i.e. it stores a new object in `a`. This distinction is visible when `a` is reference variable: It will only reset `a` itself, not the value it referred to previously.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKY29udHJhY3QgRGVsZXRlRXhhbXBsZSB7CiAgICB1aW50IGRhdGE7CiAgICB1aW50W10gZGF0YUFycmF5OwoKICAgIGZ1bmN0aW9uIGYoKSBwdWJsaWMgewogICAgICAgIHVpbnQgeCA9IGRhdGE7CiAgICAgICAgZGVsZXRlIHg7IC8vIHNldHMgeCB0byAwLCBkb2VzIG5vdCBhZmZlY3QgZGF0YQogICAgICAgIGRlbGV0ZSBkYXRhOyAvLyBzZXRzIGRhdGEgdG8gMCwgZG9lcyBub3QgYWZmZWN0IHgKICAgICAgICB1aW50W10gc3RvcmFnZSB5ID0gZGF0YUFycmF5OwogICAgICAgIGRlbGV0ZSBkYXRhQXJyYXk7IC8vIHRoaXMgc2V0cyBkYXRhQXJyYXkubGVuZ3RoIHRvIHplcm8sIGJ1dCBhcyB1aW50W10gaXMgYSBjb21wbGV4IG9iamVjdCwgYWxzbwogICAgICAgIC8vIHkgaXMgYWZmZWN0ZWQgd2hpY2ggaXMgYW4gYWxpYXMgdG8gdGhlIHN0b3JhZ2Ugb2JqZWN0CiAgICAgICAgLy8gT24gdGhlIG90aGVyIGhhbmQ6ICJkZWxldGUgeSIgaXMgbm90IHZhbGlkLCBhcyBhc3NpZ25tZW50cyB0byBsb2NhbCB2YXJpYWJsZXMKICAgICAgICAvLyByZWZlcmVuY2luZyBzdG9yYWdlIG9iamVjdHMgY2FuIG9ubHkgYmUgbWFkZSBmcm9tIGV4aXN0aW5nIHN0b3JhZ2Ugb2JqZWN0cy4KICAgICAgICBhc3NlcnQoeS5sZW5ndGggPT0gMCk7CiAgICB9Cn0=)

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract DeleteExample {
    uint data;
    uint[] dataArray;

    function f() public {
        uint x = data;
        delete x; // sets x to 0, does not affect data
        delete data; // sets data to 0, does not affect x
        uint[] storage y = dataArray;
        delete dataArray; // this sets dataArray.length to zero, but as uint[] is a complex object, also
        // y is affected which is an alias to the storage object
        // On the other hand: "delete y" is not valid, as assignments to local variables
        // referencing storage objects can only be made from existing storage objects.
        assert(y.length == 0);
    }
}

### Order of Precedence of Operators[](#order-of-precedence-of-operators "Permalink to this heading")

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

## Conversions between Elementary Types[](#conversions-between-elementary-types "Permalink to this heading")

### Implicit Conversions[](#implicit-conversions "Permalink to this heading")

An implicit type conversion is automatically applied by the compiler in some cases during assignments, when passing arguments to functions and when applying operators. In general, an implicit conversion between value-types is possible if it makes sense semantically and no information is lost.

For example, `uint8` is convertible to `uint16` and `int128` to `int256`, but `int8` is not convertible to `uint256`, because `uint256` cannot hold values such as `-1`.

If an operator is applied to different types, the compiler tries to implicitly convert one of the operands to the type of the other (the same is true for assignments). This means that operations are always performed in the type of one of the operands.

For more details about which implicit conversions are possible, please consult the sections about the types themselves.

In the example below, `y` and `z`, the operands of the addition, do not have the same type, but `uint8` can be implicitly converted to `uint16` and not vice-versa. Because of that, `y` is converted to the type of `z` before the addition is performed in the `uint16` type. The resulting type of the expression `y + z` is `uint16`. Because it is assigned to a variable of type `uint32` another implicit conversion is performed after the addition.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=dWludDggeTsKdWludDE2IHo7CnVpbnQzMiB4ID0geSArIHo7)

uint8 y;
uint16 z;
uint32 x = y + z;

### Explicit Conversions[](#explicit-conversions "Permalink to this heading")

If the compiler does not allow implicit conversion but you are confident a conversion will work, an explicit type conversion is sometimes possible. This may result in unexpected behavior and allows you to bypass some security features of the compiler, so be sure to test that the result is what you want and expect!

Take the following example that converts a negative `int` to a `uint`:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=aW50ICB5ID0gLTM7CnVpbnQgeCA9IHVpbnQoeSk7)

int  y = -3;
uint x = uint(y);

At the end of this code snippet, `x` will have the value `0xfffff..fd` (64 hex characters), which is -3 in the two’s complement representation of 256 bits.

If an integer is explicitly converted to a smaller type, higher-order bits are cut off:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=dWludDMyIGEgPSAweDEyMzQ1Njc4Owp1aW50MTYgYiA9IHVpbnQxNihhKTsgLy8gYiB3aWxsIGJlIDB4NTY3OCBub3c=)

uint32 a = 0x12345678;
uint16 b = uint16(a); // b will be 0x5678 now

If an integer is explicitly converted to a larger type, it is padded on the left (i.e., at the higher order end). The result of the conversion will compare equal to the original integer:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=dWludDE2IGEgPSAweDEyMzQ7CnVpbnQzMiBiID0gdWludDMyKGEpOyAvLyBiIHdpbGwgYmUgMHgwMDAwMTIzNCBub3cKYXNzZXJ0KGEgPT0gYik7)

uint16 a = 0x1234;
uint32 b = uint32(a); // b will be 0x00001234 now
assert(a == b);

Fixed-size bytes types behave differently during conversions. They can be thought of as sequences of individual bytes and converting to a smaller type will cut off the sequence:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ynl0ZXMyIGEgPSAweDEyMzQ7CmJ5dGVzMSBiID0gYnl0ZXMxKGEpOyAvLyBiIHdpbGwgYmUgMHgxMg==)

bytes2 a = 0x1234;
bytes1 b = bytes1(a); // b will be 0x12

If a fixed-size bytes type is explicitly converted to a larger type, it is padded on the right. Accessing the byte at a fixed index will result in the same value before and after the conversion (if the index is still in range):

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ynl0ZXMyIGEgPSAweDEyMzQ7CmJ5dGVzNCBiID0gYnl0ZXM0KGEpOyAvLyBiIHdpbGwgYmUgMHgxMjM0MDAwMAphc3NlcnQoYVswXSA9PSBiWzBdKTsKYXNzZXJ0KGFbMV0gPT0gYlsxXSk7)

bytes2 a = 0x1234;
bytes4 b = bytes4(a); // b will be 0x12340000
assert(a[0] == b[0]);
assert(a[1] == b[1]);

Since integers and fixed-size byte arrays behave differently when truncating or padding, explicit conversions between integers and fixed-size byte arrays are only allowed, if both have the same size. If you want to convert between integers and fixed-size byte arrays of different size, you have to use intermediate conversions that make the desired truncation and padding rules explicit:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ynl0ZXMyIGEgPSAweDEyMzQ7CnVpbnQzMiBiID0gdWludDE2KGEpOyAvLyBiIHdpbGwgYmUgMHgwMDAwMTIzNAp1aW50MzIgYyA9IHVpbnQzMihieXRlczQoYSkpOyAvLyBjIHdpbGwgYmUgMHgxMjM0MDAwMAp1aW50OCBkID0gdWludDgodWludDE2KGEpKTsgLy8gZCB3aWxsIGJlIDB4MzQKdWludDggZSA9IHVpbnQ4KGJ5dGVzMShhKSk7IC8vIGUgd2lsbCBiZSAweDEy)

bytes2 a = 0x1234;
uint32 b = uint16(a); // b will be 0x00001234
uint32 c = uint32(bytes4(a)); // c will be 0x12340000
uint8 d = uint8(uint16(a)); // d will be 0x34
uint8 e = uint8(bytes1(a)); // e will be 0x12

`bytes` arrays and `bytes` calldata slices can be converted explicitly to fixed bytes types (`bytes1`/…/`bytes32`). In case the array is longer than the target fixed bytes type, truncation at the end will happen. If the array is shorter than the target type, it will be padded with zeros at the end.

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjguNTsKCmNvbnRyYWN0IEMgewogICAgYnl0ZXMgcyA9ICJhYmNkZWZnaCI7CiAgICBmdW5jdGlvbiBmKGJ5dGVzIGNhbGxkYXRhIGMsIGJ5dGVzIG1lbW9yeSBtKSBwdWJsaWMgdmlldyByZXR1cm5zIChieXRlczE2LCBieXRlczMpIHsKICAgICAgICByZXF1aXJlKGMubGVuZ3RoID09IDE2LCAiIik7CiAgICAgICAgYnl0ZXMxNiBiID0gYnl0ZXMxNihtKTsgIC8vIGlmIGxlbmd0aCBvZiBtIGlzIGdyZWF0ZXIgdGhhbiAxNiwgdHJ1bmNhdGlvbiB3aWxsIGhhcHBlbgogICAgICAgIGIgPSBieXRlczE2KHMpOyAgLy8gcGFkZGVkIG9uIHRoZSByaWdodCwgc28gcmVzdWx0IGlzICJhYmNkZWZnaFwwXDBcMFwwXDBcMFwwXDAiCiAgICAgICAgYnl0ZXMzIGIxID0gYnl0ZXMzKHMpOyAvLyB0cnVuY2F0ZWQsIGIxIGVxdWFscyB0byAiYWJjIgogICAgICAgIGIgPSBieXRlczE2KGNbOjhdKTsgIC8vIGFsc28gcGFkZGVkIHdpdGggemVyb3MKICAgICAgICByZXR1cm4gKGIsIGIxKTsKICAgIH0KfQ==)

// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.5;

contract C {
    bytes s = "abcdefgh";
    function f(bytes calldata c, bytes memory m) public view returns (bytes16, bytes3) {
        require(c.length == 16, "");
        bytes16 b = bytes16(m);  // if length of m is greater than 16, truncation will happen
        b = bytes16(s);  // padded on the right, so result is "abcdefgh\0\0\0\0\0\0\0\0"
        bytes3 b1 = bytes3(s); // truncated, b1 equals to "abc"
        b = bytes16(c[:8]);  // also padded with zeros
        return (b, b1);
    }
}

## Conversions between Literals and Elementary Types[](#conversions-between-literals-and-elementary-types "Permalink to this heading")

### Integer Types[](#integer-types "Permalink to this heading")

Decimal and hexadecimal number literals can be implicitly converted to any integer type that is large enough to represent it without truncation:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=dWludDggYSA9IDEyOyAvLyBmaW5lCnVpbnQzMiBiID0gMTIzNDsgLy8gZmluZQp1aW50MTYgYyA9IDB4MTIzNDU2OyAvLyBmYWlscywgc2luY2UgaXQgd291bGQgaGF2ZSB0byB0cnVuY2F0ZSB0byAweDM0NTY=)

uint8 a = 12; // fine
uint32 b = 1234; // fine
uint16 c = 0x123456; // fails, since it would have to truncate to 0x3456

Note

Prior to version 0.8.0, any decimal or hexadecimal number literals could be explicitly converted to an integer type. From 0.8.0, such explicit conversions are as strict as implicit conversions, i.e., they are only allowed if the literal fits in the resulting range.

### Fixed-Size Byte Arrays[](#index-34 "Permalink to this heading")

Decimal number literals cannot be implicitly converted to fixed-size byte arrays. Hexadecimal number literals can be, but only if the number of hex digits exactly fits the size of the bytes type. As an exception both decimal and hexadecimal literals which have a value of zero can be converted to any fixed-size bytes type:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ynl0ZXMyIGEgPSA1NDMyMTsgLy8gbm90IGFsbG93ZWQKYnl0ZXMyIGIgPSAweDEyOyAvLyBub3QgYWxsb3dlZApieXRlczIgYyA9IDB4MTIzOyAvLyBub3QgYWxsb3dlZApieXRlczIgZCA9IDB4MTIzNDsgLy8gZmluZQpieXRlczIgZSA9IDB4MDAxMjsgLy8gZmluZQpieXRlczQgZiA9IDA7IC8vIGZpbmUKYnl0ZXM0IGcgPSAweDA7IC8vIGZpbmU=)

bytes2 a = 54321; // not allowed
bytes2 b = 0x12; // not allowed
bytes2 c = 0x123; // not allowed
bytes2 d = 0x1234; // fine
bytes2 e = 0x0012; // fine
bytes4 f = 0; // fine
bytes4 g = 0x0; // fine

String literals and hex string literals can be implicitly converted to fixed-size byte arrays, if their number of characters matches the size of the bytes type:

[open in Remix](https://remix.ethereum.org/?#language=solidity&version=0.8.21&code=Ynl0ZXMyIGEgPSBoZXgiMTIzNCI7IC8vIGZpbmUKYnl0ZXMyIGIgPSAieHkiOyAvLyBmaW5lCmJ5dGVzMiBjID0gaGV4IjEyIjsgLy8gbm90IGFsbG93ZWQKYnl0ZXMyIGQgPSBoZXgiMTIzIjsgLy8gbm90IGFsbG93ZWQKYnl0ZXMyIGUgPSAieCI7IC8vIG5vdCBhbGxvd2VkCmJ5dGVzMiBmID0gInh5eiI7IC8vIG5vdCBhbGxvd2Vk)

bytes2 a = hex"1234"; // fine
bytes2 b = "xy"; // fine
bytes2 c = hex"12"; // not allowed
bytes2 d = hex"123"; // not allowed
bytes2 e = "x"; // not allowed
bytes2 f = "xyz"; // not allowed

### Addresses[](#addresses "Permalink to this heading")

As described in [Address Literals](#address-literals), hex literals of the correct size that pass the checksum test are of `address` type. No other literals can be implicitly converted to the `address` type.

Explicit conversions to `address` are allowed only from `bytes20` and `uint160`.

An `address a` can be converted explicitly to `address payable` via `payable(a)`.

Note

Prior to version 0.8.0, it was possible to explicitly convert from any integer type (of any size, signed or unsigned) to `address` or `address payable`. Starting with in 0.8.0 only conversion from `uint160` is allowed.

[Previous](structure-of-a-contract.html "Structure of a Contract") [Next](units-and-global-variables.html "Units and Globally Available Variables")

---

© Copyright 2016-2023, The Solidity Authors. Revision `1acebf78`.

Customized with ❤️ by the [ethereum.org](https://ethereum.org/) team.

[Credits and attribution](credits-and-attribution.html).