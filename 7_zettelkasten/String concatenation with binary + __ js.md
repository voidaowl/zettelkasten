# Meta
2025-01-30 13:41
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# 📷 → What does it look like?
```JavaScript title:example.js
let s = "my" + "string";
alert(s); // mystring

alert( '1' + 2 ); // "12"
alert( 2 + '1' ); // "21"

alert( 2 + 2 + '1' ); // 41
alert( '1' + 2 + 2 ); // 122
```

# 🔍 → What does it do?
Usually, the [[Addition (+) operator __ js|addition operator]] `+` sums numbers. If the binary `+` is applied to strings, it merges (concatenates) them.

# ❓ → How it does it.
 If any of the operators is a string, the other one is converted to a string too. The binary `+` is the only operator that supports strings in such a way. Other arithmetic operators work only with numbers and always convert their operands to numbers.
 ```JavaScript title:example.js
alert( 6 - '2' ); // 4
alert( '6' / 2 ); // 3
```

# 📑 → Further reading / Sources
[[String conversion __ js]]
[[String coercion __ js]]
[String.prototype.concat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/concat)
