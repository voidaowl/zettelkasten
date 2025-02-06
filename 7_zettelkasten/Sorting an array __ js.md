# Meta
2025-02-06 21:28
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# sort
Syntax: `arr.sort(compareFn)`.
Sorts the array **in place**, changing its element order. Returns the sorted array, but the return value is usually ignored, as `arr` itself is modified.

```JavaScript title:example.js
let arr = [1, 2, 15];

arr.sort();

alert( arr ); // 1, 15, 2
```

The items are **sorted as strings** by default.

All elements are converted to strings for comparisons, which means lexicographic ordering is applied.

To use our own sorting order, we must supply a function to compare two arbitrary values and return:
```JavaScript title:example.js
function compare(a, b) {
	if (a > b) return 1;
	if (a == b) return 0;
	if (a < b) return -1;
}
```

For instance, to sort as numbers:
```JavaScript title:example.js
function compareNumeric(a, b) {
	if (a > b) return 1;
	if (a == b) return 0;
	if (a < b) return -1;
}

let arr = [ 1, 2, 15 ];

arr.sort(compareNumeric);

alert( arr ); // 1, 2, 15
```

The `arr.sort(fn)` method implements a generic sorting algorithm (an optimize quicksort or Timsort most often). The algorithm may compare an element with multiple others in the process, but it tries to make as few comparisons as possible.

ℹ️ **A comparison function may return any number**
A comparison function is only required to return a positive number to say “greater” and a negative number to say “less”.
```JavaScript title:example.js
let arr = [ 1, 2, 15 ];

arr.sort(function(a, b) { return a - b; });

alert(arr); // 1, 2, 15
```

ℹ️ **Arrow functions for the best**
```JavaScript title:example.js
arr.sort( (a, b) => a - b );
```

ℹ️ **Use `localeCompare` for strings**
```JavaScript title:example.js
let countries = ['Österreich', 'Andorra', 'Vietnam'];

alert( countries.sort( (a, b) => a > b ? 1 : -1) ); // Andorra, Vietnam, Österreich (wrong)

alert( countries.sort( (a, b) => a.localeCompare(b) ) ); // Andorra,Österreich,Vietnam (correct!)
```

# 📑Further reading
[Array.prototype.sort() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
