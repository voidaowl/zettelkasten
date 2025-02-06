# Meta
2025-02-05 13:09
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Strict tests

`Number.isNaN` and `Number.isFinite` are the more “strict” versions of the previous two. They don’t auto-convert their argument into a number, but check if it belongs to the `number` type instead.

`Number.isNaN(value)` returns `true` if the argument belongs to the `number` type and it is `NaN`. In any other case, it returns `false`.

```JavaScript title:example.js
alert( Number.isNaN(NaN) ); // true
alert( Number.isNaN("str" / 2) ); // true

// Note the difference:
alert( Number.isNaN("str") ); // false
alert( isNaN("str") ); // true
```

`Number.isFinite(value)` returns `true` if the argument belongs to the `number` type and it is not `NaN/Infinity/-Infinity`. In any other case, it returns `false`.

```JavaScript title:example.js
alert( Number.isFinite(123) ); // true
alert( Number.isFinite(Infinity) ); // false
alert( Number.isFinite(2 / 0) ); // false

// Note the difference:
alert( Number.isFinite("123") ); // false
alert( isFinite("123") ); // true
```

# 📑 → Further reading
[Number.isNaN() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/isNaN)
[Number.isFinite() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/isFinite)