# Meta
2025-01-30 10:52
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# Number coercion
The operation can be summarized as follows:
1. Numbers are returned as-is.
2. `undefined` turns into `NaN`.
3. `null` turns into `0`.
4. `true` turns into `1`, `false` into `0`.
5. Strings are converted by parsing them as if they contain a [number literal](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#numeric_literals). Parsing failure results in `NaN`. There are some minor differences compared to an actual number literal:
	- Leading and trailing whitespace/line terminators are ignored.
	- A leading `0` digit doesn’t cause the number to become an octal literal (or get rejected in strict mode).
	- `+` and `-` are allowed at the start of the string to indicate its sign. However, the sign can only appear once, and must not be followed by whitespace.
	- `Infinity` and `-Infinity` are recognized as literals. In actual code, they are global variables.
	- Empty or whitespace-only strings are converted to `0`.
	- [Numeric separator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#numeric_separators) aren’t allowed.
6. [[Data types __ js#BigInt|BigInts]] throw a `TypeError` to prevent unintended implicit coercion causing loss of precision.
7. [Symbols](Symbol __ js) throw a `TypeError`.
8. Objects are first [[Primitive coercion __ js|converted to a primitive]] by calling their [`[Symbol.toPrimitive]()`]([Symbol.toPrimitive]()) (with `"number"` as hint), `valueOf()`, and `toString()` methods, in that order. The resulting primitive is then converted to a number.

# Other methods
1. [[Unary plus (+) __ js|Unary plus (+)]]: `+x` does exactly the number coercion steps explained above to convert `x`.
2. The [`Number()`](Number() constructor __ js) function: `Number(x)` uses the same algorithm to convert `x`, except that [[Data types __ js#BigInt|BigInts]] don’t throw a `TypeError`, but return their number value, with possible loss of precision.

[`Number.parseFloat()`](Number.parseFloat() __ js) and [`Number.parseInt()`](Number.parseInt() __ js) are similar to `Number()` but only convert strings, and have slightly different parsing rules. For example, `parseInt()` doesn’t recognize the decimal point, and `parseFloat()` doesn’t recognize the `0x` prefix.