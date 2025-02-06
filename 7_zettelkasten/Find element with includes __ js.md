# Meta
2025-02-06 20:24
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# includes
Syntax: `arr.includes(item, from)`
Looks for `item` starting from `index` and returns `true` if it finds it.

```JavaScript title:example.js
let arr = [1, 0, false];

alert( arr.includeS(1) ); // true
```

The `includes` method handles `NaN` correctly, unlike `indexOf`:
```JavaScript title:example.js
const arr = [NaN];
alert( arr.indexOf(NaN) ); // -1
alert( arr.includes(NaN) ); // true
```

# 📑Further reading
[Array.prototype.includes() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes)
