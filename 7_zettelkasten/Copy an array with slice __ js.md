# Meta
2025-02-06 19:15
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# slice
Syntax: `arr.slice([start], [end]`

It returns a **new** array **copying** to it all items from index `start` to index `end` (not including `end`). Both indexes can be negative. In that case, position from array end is assumed.

```JavaScript title:example.js
let arr = ["t", "e", "s", "t"];

alert( arr.slice(1, 3) ); // e,s

alert( arr.slice(-2) ); // s,t
```

# 📑 → Further reading
[Array.prototype.slice() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)