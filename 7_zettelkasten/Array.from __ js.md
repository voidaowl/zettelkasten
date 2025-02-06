# Meta
2025-02-06 23:36
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Array.from
Takes an iterable or array-like value and makes a “real” `Array` from it.

```JavaScript title:example.js
let arrayLike = {
	0: "Hello",
	1: "World",
	length: 2
};

let arr = Array.from(arrayLike);
alert( arr.pop() ); // World
```

Syntax: `Array.from(obj[, mapFn, thisArg])`.

The optional second argument `mapFn` can be a function that will be applied to each element before adding it to the array, and `thisArg` allows us to set `this` to for it.

```JavaScript title:example.js
let str = '𝒳😂';

let chars = Array.from(str);

alert(chars[0]); // 𝒳
alert(chars[1]); // 😂
alert(chars.length); // 2
```

# 📑Further reading
[Array.from() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from)
