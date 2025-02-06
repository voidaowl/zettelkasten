# Meta
2025-02-06 21:22
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# filter
The `find` method looks for the first occurrence of an element that makes the function return `true`.

If there may be many, we can use `arr.filter(fn)`. Syntax is similar to find, but `filter` returns an array of all matching elements.

```JavaScript title:example.js
let results = arr.filter(function(item, index, arr) {...});
```

For example:
```JavaScript title:example.js
let user = [
	{id: 1, name: "John"},
	{id: 2, name: "Pete"},
	{id: 3, name: "Mary"},
];

let someUsers = users.filter(item => item.id < 3);

alert(someUsers.length); // 2
```

# 📑Further reading
[Array.prototype.filter() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
