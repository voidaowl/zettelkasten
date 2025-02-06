# Meta
2025-01-30 21:34
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Comparison operators
In JavaScript, comparison operators are written as follows:
1. Greater/lesser than: `a > b`, `a < b`.
2. Greater/less than or equals: `a >= b`, `a <= b`.
3. Equals: `a == b`.
4. Not equals: `a != b`.

# Boolean is the result
All comparison operators return a boolean value:
1. `true` – means “yes”, “correct”, or “the truth”.
2. `false` – means “no”, “wrong”, or “not the truth”.

```JavaScript title:example.js
alert( 2 > 1 ); // true
alert( 2 == 1 ); // false
alert( 2 != 1 ); // true 
```

A comparison result can be assigned to a variable, just like any other value:
```JavaScript title:example.js
let result = 5 > 4;
alert( result ); // true
```