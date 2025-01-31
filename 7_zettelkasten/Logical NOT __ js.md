# Meta
2025-01-31 09:13
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# ! (NOT)
The boolean NOT operator is represented with an exclamation sign `!`. The syntax is:
```JavaScript title:example.js
result = !value;
```

The operator accepts a single argument and does the following:
1. Converts the operand to boolean type: `true` or `false`.
2. Returns the inverse value.

```JavaScript title:example.js
alert( !true ); // false
alert( !0 ); // true
```

A double NOT `!!` is sometimes used for converting a value to boolean type:
```JavaScript title:example.js
alert( !!"not-empty-string" ); // true
alert( !!null ); // false
```

The first NOT converts the value to a boolean and returns the inverse, and the second NOT inverses it again.

The verbose approach:
```JavaScript title:example.js
alert( Boolean("non-empty string") ); // true
alert( Boolean(null) ); // false
```

The precedence of NOT `!` is the highest of all logical operators, so it always executes first, before `&&` or `||`.

# 📑 → Further reading
[Logical NOT (`!`) - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_NOT)
[`Boolean()` constructor - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean/Boolean)