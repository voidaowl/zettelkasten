# Meta
2025-02-06 22:08
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# reduce
Syntax:
```JavaScript title:example.js
let value = arr.reduce(function(accumulator, item, index, array) {
	// ...
});
```

The function is applied to all array elements one after another and “carries on” its result to the next call.

Arguments:
- `accumulator` – is the result of the previous function call, equals `initial` the first time (if `initial` is provided).
- `item` – is the current array item.
- `index` – is its position.
- `array` – is the array.

As the function is applied, the result of the previous function call is passed to the next one as the first argument.

```JavaScript title:example.js
let arr = [1, 2, 3, 4, 5];

let result = arr.reduce((sum, curret) => sum + current, 0);

alert(result); // 15
```

The function passed to `reduce` uses only 2 arguments. That’s usually enough. We can even omit the `initial` argument in the example above.

Such use requires extreme care. If the array is empty, then `reduce` call without initial value gives an error.

```JavaScript title:example.js
let arr = [];

arr.reduce((sum, curr) => sum + curr); // Error
```

> [!warning] **Always specify the initial value!**

The method `arr.reduceRight` does the same but goes from right to left.

# 📑Further reading
[Array.prototype.reduce() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)
[Array.prototype.reduceRight() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduceRight)
