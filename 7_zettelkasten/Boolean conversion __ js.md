# Meta
2025-01-30 10:27
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# 📷 → What does it look like?
```JavaScript title:example.js
alert( Boolean(1) ); // true
alert( Boolean(0) ); // false

alert( Boolean("hello") ); // true
alert( Boolean("") ); // false
```

# 🔍 → What does it do?
Converts a value into `true` or `false`.

# ❓ → How it does it.
The conversion rules:
1. Values that are intuitivelyu “empty”, like `0`, `""`, `null`, `undefined`, and `NaN`, become `false`.
2. Other values become `true`.

# 📑 → Further reading / Sources
[Boolean - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)