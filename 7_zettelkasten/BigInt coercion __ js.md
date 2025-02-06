# Meta
2025-01-30 12:27
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# BigInt Coercion
The operation can be summarized as follows:
1. BigInts are returned as-is.
2. `undefined` and `null` throw a `TypeError`.
3. `true` turns `1n`; `false` turns into `0n`.
4. Strings are converted by parsing them as if they contain an integer literal. Any parsing failure results in a `SyntaxError`. The syntax isa subset of [[Number coercion __ js|string numeric literals]], where decimal points or exponent indicators are not allowed.
5. [[Number __ js|Numbers]] throw a `TypeError`.
6. Objects are first [[Primitive coercion __ js|converted to a primitive]] by calling their `[Symbol.toPrimitive]()` (with `"number"` as hint), `valueOf`, and `toString()` methods, in that order. The resulting primitive is then converted to BigInt.

# Alternatives
The best way to achieve nearly the same effect in JavaScript is through the `BigInt()` function: `BigInt(x)` uses the same algorithm to convert `x` except that [[Number __ js|Numbers]] don’t allow `TypeError`, but are converted to BigInts if they are integers.

Note that built-in operations expecting BigInts often truncate the BigInt to a fixed width after coercion. This includes [`BigInt.asIntN()`](BigInt.asIntN()), [`BigInt.asUintN()`](BigInt.asUintN()), and methods of [`BigInt64Array`](BigInt64Array) and [`BigUint64Array`](BigUint64Array).