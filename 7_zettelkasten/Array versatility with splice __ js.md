# Meta
2025-02-06 19:07
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# splice
How to delete an element from an array?

We can use `delete`, since arrays are objects:
```JavaScript title:example.js
let arr = ['I', 'go', 'home'];

delete arr[1];

alert( arr[1] ); // undefined

alert( arr.length ); // 3
```

The `arr.splice` method can insert, remove and replace elements.
Syntax: `arr.splice(start[, deleteCount, elem1, ..., elemN])`

It modifies `arr` starting from index `start`: removes `deleteCount` elements and then inserts `elem1, ..., elemN` at their place. Returns the array of removed elements.

```JavaScript title:example.js
let arr = ["I", "study", "JavaScript"];

arr.splice(1, 1); // from index 1 remove 1 element

alert( arr ); // ["I", "JavaScript"];
```

Here we remove 3 elements and replace them with the other two:
```JavaScript title:example.js
let arr = ["I", "study", "JavaScript"];

arr.splice(0, 3, "Let's", "dance");

alert( arr ); // ["Let's", "dance"]
```

`splice` returns the array of removed elements:
```JavaScript title:example.js
let arr = ["I", "study", "JavaScript"];

// remove first 2 elements
let remove = arr.splice(0, 2);

alert( removed ); // "I", "study"
```

`splice` can also insert elements without any removals. For that, set `deleteCount` to `0`:
```JavaScript title:example.js
let arr = ["I", "study", "JavaScript"];

// from index 0, delete 0m then insert
arr.splice(2, 0, "complex", "lanugage");

alert( arr ); // ["I", "study", "complex", "language", "JavaScript"]
```

Negative indexes are allowed:
```JavaScript title:example.js
let arr = [1, 2, 5];

arr.splice(-1, 0, 3, 4);

alert( arr ); // 1,2,3,4,5
```

# 📑 → Further reading
[Array.prototype.splice() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)

