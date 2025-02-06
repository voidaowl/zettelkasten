# Meta
2025-02-05 12:42
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Rounding
There are several built-in functions for rounding:

`Math.floor`
Rounds down: `3.1` becomes `3`, and `-1.1` becomes `-2`.

`Math.ceil`
Rounds up: `3.1` becomes `4`, and `-1.1` becomes `-1`.

`Math.round`
Rounds to the nearest integer: `3.1` becomes `3`, `3.6` becomes `4`. In the middle cases, `3.5` rounds up to `4`, and `-3.5` rounds up to `-3`.

`Math.trunc`
Removes anything after the decimal point without rounding: `3.1` becomes `3`, `-1.1` becomes `-1`.

What if we want to round the number to the `n-th` digit after the decimal point?

Multiply and divide:
```JavaScript title:example.js
let num = 1.23456;

alert( Math.round(num * 100) / 100 ); // 1.23456 -> 123.456 -> 123 -> 1.23
```

…or use `toFixed(n)`, which rounds the number to `n` digits after the decimal point and returns a **string** representation of the result:
```JavaScript title:example.js
let num = 12.34;
alert( num.toFixed(1) ); // "12.3"
```

This rounds up or down to the nearest value, similar to `Math.round`:
```JavaScript title:example.js
let num = 12.36;
alert( num.toFixed(1) ); // "12.4"
```

Note that the result of `toFixed` is a string. We can convert it with `Number` or unary plus, e.g. `+num.toFixed(5)`.

# 📑 → Further reading
[Math.floor() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor)
[Math.ceil() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/ceil)
[Math.round() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/round)
[Math.trunc() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/trunc)
[Number.prototype.toFixed() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed)
