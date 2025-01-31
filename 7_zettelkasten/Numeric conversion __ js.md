# Meta
2025-01-30 10:20
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# 📷 → What does it look like?
```JavaScript title:example.js
// Implicit conversion
alert("6" / "2"); // 3, strings are converted to numbers

// Explicit conversion
let str = "123";
alert(typeof str); // string

let num = Number(str); // 123

alert(typeof num); // number

// NaN
let age = Number("an arbitrary string")

alert(age); // NaN
```

# 🔍 → What does it do?
Converts strings and Booleans into numbers.

# ❓ → How it does it.
Rules:
1. `undefined` becomes `NaN`
2. `null` becomes `0`
3. `true` and `false` become `1` and `0`, respectively.
4. In the case of a `string`, whitespace (`\t`, `\n`, etc.) from the start and end are removed. If the remaining string is empty, the result is `0`. Otherwise, the number is “read” from the string. An error gives `NaN`.

# 📑 → Further reading / Sources
[Number - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)