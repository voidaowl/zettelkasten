# Meta
2025-01-30 12:37
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Primitive coercion
The primitive coercion process is used where a primitive value is expected, but there’s no strong preference for what the actual type should be. This is usually when a *string*, a *number*, or a *BigInt* are equally acceptable. For example:

1. The [[Date() constructor __ js|date constructor]] `Date()` when it receives one argument that’s not a `Date` instance – strings represent date strings, while numbers represent timestamps.
2. The [[Addition (+) operator __ js|addition]] `+` operator – if one operand is a string, string concatenations is preformed; otherwise, numeric addition is performed.
4. The [[Equality operator (==) __ js|equality operator]] `==` – if one operand is a primitive while the other is an object, the object is converted to a primitive value with no preferred type.

This operation does not do any conversion if the value is already a primitive. Objects are converted to primitives by calling its [`[Symbol.toPrimitive]()`]([Symbol.toPrimitive]()) (with `"default"` as hint), `valueOf()`, and `toString()` methods, in that order.

Note that primitive conversion calls `valueOf()` before `toString()`, which is similar to the behaviour of [[Number coercion __ js|number coercion]] but different from [[String coercion __ js|string coercion]].

The `[Symbol.toPrimitive]()` method, if present, must return a primitive – returning an object results in a `TypeError`. For `valueOf()` and `toString()`, if one returns an object, the return value is ignored and the other’s return value is used instead; if neither is present, or neither returns a primitive, a `TypeError` is thrown.