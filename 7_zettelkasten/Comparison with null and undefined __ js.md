# Meta
2025-01-30 22:17
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Comparison with null and undefined
There’s a non-intuitive behaviour when `null` and `undefined` are compared to other values.

```JavaScript title:example.js
// Strict equality
alert( null === undefined ); // false

// Non-strict equality
alert( null == undefined ); // true
```

For maths and other comparisons, `null/undefined` are converted to numbers: `null` becomes `0` and `undefined` becomes `NaN`.

## Strange result: null vs 0
```JavaScript title:example.js
alert( null > 0 ); // false
alert( null == 0 ); // false
alert( null >= 0 ); // true
```

Comparisons convert `null` to a number, treating it as `0`, while the equality check `==` for `undefined` and `null` is defined such that, without any conversions, they equal each other and don’t equal anything else. That’s why `null == 0` is `false`.

## An incomparable undefined
The value `undefined` shouldn’t be compared to other values:
```JavaScript title:example.js
alert( undefined > 0 ); // false
alert( undefined < 0 ); // false
alert( undefined == 0 ); // false
```

Comparisons return `false` because `undefined` is converted to `NaN`, which returns `false` for all comparisons.

The equality check returns `false` because `undefined` only equals `null`, `undefined`, and no other value.

## Avoid problems
1. Treat any comparison with `undefined/null` except the strict equality`===` with exceptional care.
2. Don’t use comparisons with a variable which may be `null/undefined`, unless you’re sure of what you’re doing.