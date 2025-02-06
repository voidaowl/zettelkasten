# Meta
2025-02-06 13:23
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# toString
Arrays have their own implementation of `toString` method that returns a comma-separated list of elements.

For instance:
```JavaScript title:example.js
let arr = [1, 2, 3];

alert( arr ); // 1, 2, 3
alert( String(arr) === '1,2,3' ); // true
```

Also, let’s try this:
```JavaScript title:example.js
alert( [] + 1 ); // "1"
alert( [1] + 1 ); // "11"
alert( [1,2] + 1 ); // "1,21"
```

Arrays do not have `Symbol.toPrimitve`, neither a viable `valueOf`. They implement only to `toString` conversion, so here `[]` becomes an empty string string, `[1]` becomes `"1"`, and `[1,2]` becomes `"1,2"`.

When the binary plus `"+"` operator adds something to a string, it converts it to a string as well, so the next step looks like this:
```JavaScript title:example.js
alert( "" + 1 ); // "1"
alert( "1" + 1 ); // "11"
alert( "1,2" + 1 ); // "1,21"
```

# 📑 → Further reading
[Array.prototype.toString() - JavaScript - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/toString)
