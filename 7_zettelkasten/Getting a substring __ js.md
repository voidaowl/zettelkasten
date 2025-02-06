# Meta
2025-02-06 10:22
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# slice
Syntax: `str.slice(start [, end])` 
Returns the part of the string from `start` to (but not including) `end`.
```JavaScript title:example.js
let str = 'stringify';
alert( str.slice(0, 5) ); // 'strin'
alert( str.slice(0, 1) ); // 's'
```

If `end` is omitted, `slice` goes to the end:
```JavaScript title:example.js
let str = 'stringify';
alert( str.slice(2) ); // 'ringify'
```

Negative values for `start/end` are also possible:
```JavaScript title:example.js
let str = 'stringify';
alert( str.slice(-4, -1) ); // 'gif'
```

# substring
Syntax: `str.substring(start [, end])`
Returns the part of the string *between* `start` and `end` (not including `end`).

Compared to `slice`, it allows `start` to be greater than `end`.
```JavaScript title:example.js
let str = 'stringify';

// these are same for substring
alert( str.substring(2, 6) ); // 'ring'
alert( str.substring(6, 2) ); // 'ring'

// ...but not for slice:
alert( str.slice(2, 6) ); // "ring" (the same)
alert( str.slice(6, 2) ); // "" (an empty string)
```

Negative arguments are **not** supported. They are treated as `0`.

# 📑 → Further reading
[String.prototype.slice() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/slice)
[String.prototype.substring() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substring)
