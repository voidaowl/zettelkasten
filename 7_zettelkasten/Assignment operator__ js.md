# Meta
2025-01-30 18:12
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Assignment
The assignment operator `=` is listed in the precedence table with priority `2`.

When we assign a variable like `x = 2 * 2 + 1`, the calculations are done first and then the `=` is evaluated, storing the result in `x`.

## Assignment = returns a value
The call `x = value` writes `value` into `x` *and then returns it.*
```JavaScript title:example.js
let a = 1;
let b = 2;

let c = 3 - (a = b + 1);

alert(a); // 3
alert(c); // 0
```

In the example above, the result of `(a = b + 1)` is the value assigned to `a` (that is `3`). It is then used for further evaluations.

## Chaining assignments
```JavaScript title:example.js
let a, b, c;

a = b = c = 2 + 2;

alert( a ); // 4
alert( b ); // 4
alert( c ); // 4
```

Chained assignments evaluate from right to left. First, the rightmost expression `2 + 2` is evaluated and then assigned to the variables on the left: `c`, `b` and `a`. At the end, all the variables share a single value.

For readability, it’s best to split such code into new lines.

# 📑 → Further reading
[Assignment (=)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Assignment)
