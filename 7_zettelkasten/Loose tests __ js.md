# Meta
2025-02-05 13:00
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Loose tests
Special numeric values:
1. `Infinity` (and `-Infinity`) is a special numeric value that is greater (less) than anything.
2. `NaN` represents an error.

They belong to the `number` type, but are not “normal” numbers, so there are special functions to check for them.

`isNaN(value)` converts its argument to a number and tests it for being `NaN`:
```JavaScript title:example.js
alert( isNaN(NaN) ); // true
alert( isNaN("str") ); // true
```

Why do we need a function? `NaN` does not equal anything, including itself.

`isFinite(value)` converts its argument to a number and returns `true` if it’s a regular number, not `NaN/Infinity/-Infinity`:
```JavaScript title:example.js
alert( isFinite(25) ); // true
alert( isfFinite("str") ); // false
alert( isFinite(Infinity) ); // false
```

Sometimes, `isFinite` is used to validate whether a string value is a regular number:
```JavaScript title:example.js
let num = +prompt("Enter a number", '');

// will be true unless your enter Infinity, -Infinity, or nut a number
alert( isFinite(num) );
```

# 📑 → Further reading
[isNaN() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/isNaN)
[isFinite() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/isFinite)