# Meta
2025-02-06 19:18
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# concat
Syntax: `arr.concat(arg1, arg2, ..., argN)`

Creates a **new** array that includes values from other arrays and additional items. If an argument is an array, all its elements are copied. Otherwise, the argument itself is copied.

```JavaScript title:example.js
let arr = [1, 2];

alert( arr.concat([3, 4]) ); // 1,2,3,4

alert( arr.concat([3,4], [5,6], 7)); // 1,2,3,4,5,6,7
```

Other objects, even if they look like arrays, are added as a whole:
```JavaScript title:example.js
let arr = [1, 2];

let arrayLike = {
	0: "something",
	length: 1
};

alert( arr.concat(arrayLike) ); // 1,2,[object Object]
```

If an array-like object has a special `Symbol.isConcatSpreadable` property, it’s treated as an array:
```JavaScript title:example.js
let arr = [1, 2];

let arrayLike = {
	0: "something",
	1: "else",
	[Symbol.isConcatSpreadable]: true,
	length: 2,
};

alert( arr.concat(arrayLike) ); // 1,2,something,else
```

# 📑Further reading
[Array.prototype.concat() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)
[Symbol.isConcatSpreadable - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/isConcatSpreadable)
