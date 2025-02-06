# Meta
2025-02-05 21:22
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# parseInt and parseFloat
Numeric conversion using a `+` or `Number()` is strict. If a value is not exactly a number, it fails:
```JavaScript title:example.js
alert(+"100px"); // NaN
```

The sole **exception** is spaces at the beginning or at the end of the string, as they are ignored.

If we want to extract numbers from values that have units, e.g. `100px`, `12pt` or `19$`, we can use `parseInt` or `parseFloat`.

They “read” a number from a string until they can’t. In case of an error, the gathered number is returned. `paseInt` returns an integer. `parseFloat` returns a floating-point number:
```JavaScript title:example.js
alert( parseInt('100px') ); // 100
alert( parseFloat('12.5em') ); // 12.5
```

`parseInt/parseFloat` will return `NaN` when no digits can be read:
```JavaScript title:example.js
alert( parseInt('a123') ); // NaN, first symbol stops the process
```

The `parseInt(str, radix)`  function has an optional second parameter. It specifies the base of the numeral system, so `parseInt` can also parse strings or hex numbers, binary numbers, etc.:
```JavaScript title:example.js
alert( parseInt('0xff', 16)); // 255
alert( parseInt('ff', 16) ); // 255

alert( parseInt('2n9c', 36) ); // 123456
```

# 📑 → Further reading
[parseInt() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseInt)
[parseFloat() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseFloat)
