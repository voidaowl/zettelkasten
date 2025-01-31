# Meta
2025-01-30 10:32
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# String coercion
Many built-in operations that expect strings first coerce their arguments to strings. The operation can be summarized as follows:
1. Strings are returned as-is.
2. `undefined` turns into `"undefined"`.
3. `null` turns into `"null"`.
4. `true` turns into `"true"`, `false` into `"false"`.
5. Numbers are converted with the same algorithm as [`toString(10)`](Number.prototype.toString()).
6. [[Data types __ js#BigInt|BigInts]] are converted with the same algorithm as [`toString(10)`](Number.prototype.toString()).
7. Objects are first [[Primitive coercion __ js|converted to a primitive]] by calling its [[[Symbol.toPrimitive]() __ js|[Symbol.toPrimitive]()]] (with “string” as hint), `toString()`, and `valueOf()` methods, in that order. The resulting primitive is them converted to a string.

# Other methods
1. [[Template literals __ js ()|Template literal]]: `${x}` does exactly the string coercion steps explained above for the embedded expression.
2. The [`String()`](String() constructor __ js) function: `String(x)` uses the same algorithm to convert `x`, except that [Symbols](Symbol __ js) don’t throw a `TypeError` but return `"Symbol(description)"`, where `description` is the [description](Symbol.prototype.description _ js) of the Symbol.
3. Using the [[Addition (+) operator __ js|addition operator]] `+` coerces its operand to a *primitive* instead of a *string*, and, for some objects, has entirely different behaviours from normal string coercion.

Depending on your use case, you may want to use `${x}` (to mimic built-in behaviour) or `String(x)` (to handle symbol values without throwing an error), but you shouldn’t use `"" + x`.