# Meta
2025-02-05 12:52
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Imprecise calculations
If a number is really large, it may overflow the 64-bit storage and become `Infinity`:
```JavaScript title:example.js
alert( 1e500 ); // Infinity
```

Less obvious, but more frequent, is loss of precision:
```JavaScript title:example.js
alert( 0.1 + 0.2 == 0.3 ); // false
```

What’s going on?
```JavaScript title:example.js
alert( 0.1 + 0.2 ); // 0.30000000000000004
```

Why? A number is stored in memory in its binary form. Fractions like `0.1` or `0.2` in the decimal numeric system are actually unending fractions in binary form.
```JavaScript title:example.js
alert(0.1.toString(2)); // 0.0001100110011001100110011001100110011001100110011001101
alert(0.2.toString(2)); // 0.001100110011001100110011001100110011001100110011001101
alert((0.1 + 0.2).toString(2)); // 0.0100110011001100110011001100110011001100110011001101
```

`0.1` is `1/10`. In decimal, such numbers are easily representable. By comparison, `1/3` is not: `0.33333(3)`.

Division by powers `10` is guaranteed to work well in the decimal system, but division by `3` is not. Similarly, in binary, the division by powers `2` is guaranteed to work, but division by powers `10` becomes an endless binary fraction.

Workaround with `toFixed(n)`:
```JavaScript title:example.js
let sum = 0.1 + 0.2;
alert( sum.toFixed(2) ); // "0.30"
```

Remember that `toFixed` always returns a string. Use unary `+` or `Number()` to convert to number type.