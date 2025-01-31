# Meta
2025-01-30 21:47
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# Comparison of different types
When comparing values of different types, JavaScript converts the values to numbers.

For example:
```JavaScript title:example.js
alert( '2' > 1 ); // true
alert( '01' == 1 ); // true
```

For boolean values, `true` becomes `1` and `false` becomes `0`.

> [!info] **A funny consequence**
> It is possible at the same time:
> 	- Two values are equal.
> 	- One of them is `true` as a boolean and the other one is `false` as a boolean.
> 

For example:
```JavaScript title:example.js
let a = 0;
alert( Boolean(a) ); // false

let b = "0";
alert( Boolean(b) ); // true

alert(a == b); // true
```

From JavaScript’s standpoint, the result is normal. An equality check converts values using the numeric conversion (hence `"0"` becomes `0`), while the explicit `Boolean` conversion uses another set of rules.

# 📑 → Further reading
[Loose equality using `==`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness#loose_equality_using)
