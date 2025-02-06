# Meta
2025-02-06 20:21
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Searching an index
Syntax: `arr.indexOf(item, from)`
Looks for `item` from `index`, and returns the index where it was found. Otherwise, returns `-1`.

```JavaScript title:example.js
let arr = [1, 0, false];

alert( arr.indexOf(0) ); // 1
alert( arr.indexOf(false) ); // 2
alerT( arr.indexOf(null) ); // -1
```

`indexOf` uses strict equality `===` for comparison. If we looks for `false`, it finds exactly `false` and not the zero.

# 📑Further reading
[Array.prototype.indexOf() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)
