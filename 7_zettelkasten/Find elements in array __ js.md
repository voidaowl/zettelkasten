# Meta
2025-02-06 21:09
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# find
Syntax: `arr.find(function(item, index, arr) { ... });`
Finds an item with a specific condition.
The function is called for elements of the array, one after another:
- `item` is the element.
- `index` is its index.
- `arr` is the array itself.

If it evaluates to `true`, stops the search and returns the `item`. Otherwise, returns `undefined`.
```JavaScript title:example.js
let users = [
	{id: 1, name: "John"},
	{id: 2, name: "Pete"},
	{id: 3, name: "Mary"},
];

let user = users.find(item => item.id === 1);

alert(user.name); // John
```

Note the function `item => item.id == 1` with one argument. That’s typical. Other arguments of this function are rarely used.

# findIndex
`arr.findIndex` has the same syntax but returns the index where the element was found instead of the element itself. Returns `-1` if nothing is found.

# findLastIndex
Same as `findIndex`, but searches from right to left.

```JavaScript title:example.js
let users = [
	{id: 1, name: "John"},
	{id: 2, name: "Pete"},
	{id: 3, name: "Mary"},
	{id: 4, name: "John"},
];

alert(users.findIndex(user => user.name == "John")); // 0
alert(users.findLastIndex(user => user.name == "John")); // 3
```

# 📑Further reading
[Array.prototype.find() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find)
[Array.prototype.findIndex() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex)
[Array.prototype.findLastIndex() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findLastIndex)