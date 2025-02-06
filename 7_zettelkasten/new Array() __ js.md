# Meta
2025-02-06 13:16
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# The Array constructor
```JavaScript title:example.js
let arr = new Array('Apple', 'Pear', 'etc');
```

It’s rarely used, because `[]` is shorter.

If `new Array` is called with a single argument, which is a number, it creates an array **without items, but with the given length**.

```JavaScript title:example.js
let arr = new Array(2);

alert( arr[0] ); // undefined

alert( arr.length ); // 2
```

# 📑 → Further reading
[Array() construct - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Array)
