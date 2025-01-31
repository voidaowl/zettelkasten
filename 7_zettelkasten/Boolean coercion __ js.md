# Meta
2025-01-30 13:23
**Tags:** [[JavaScript Learning]]
**Activity:** #learning
**Status:** #completed 

# Boolean Coercion
The operation can be summarized as follows:

1. Booleans are returned as-is.
2. `undefined` turns into `false`.
3. `null` turns into `false`.
4. `0`, `-0`, and `NaN` turn into `false`; other numbers turn into `true`.
5. `0n` turns into `false`; other [[BigInt() __ js|BigInts]] turn into `true`.
6. The empty string `""` turns into `false`; other strings turn into `true`.
7. [[Symbol __ js|Symbols]] turn into `true`.
8. All objects become `true`.

> [!info] **Note:** Unlike other type conversions like [[String coercion __ js|string coercion]] or [[Number coercion __ js|number coercion]], boolean coercion does not attempt to [[Primitive coercion __ js|convert objects to primitives]] by calling user methods.

In other words, there are only a handful of values that get coerced to `false` – these are called [[Falsy __ js|falsy]] values. All other values are called [[Truthy __ js|truthy]] values. A value’s truthiness is important when used with logical operators, conditional statements, or any other boolean context.

# Alternatives
1. [[Double Not (!!) __js|Double Not (!!)]]: `!!x` negates `x` twice, which converts `x` to a boolean using the same algorithm as above.
2. The [[Boolean() constructor __ js|boolean function]]: `Boolean(x)` uses the same algorithm as above to convert `x`.