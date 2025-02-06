# Meta
2025-02-06 22:29
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Array.isArray
`typeof`  doesn’t distinguish a plain object from an array:
```JavaScript title:example.js
alert(typeof {}); // object
alert(typeof []); // object
```

`Array.isArray(value)` returns `true` if `value` is an array. Otherwise, returns `false`.
```JavaScript title:example.js
alert(Array.isArray({})); // false
alert(Array.isArray([])); // true
```

# 📑Further reader
[Array.isArray() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray)
