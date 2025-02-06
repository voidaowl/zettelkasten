# Meta
2025-02-06 12:28
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Declaration
Syntax:
```JavaScript title:example.js
let arr = new Array();
let arr = []; // preferred
```

Array elements are numbered, ordered from `0`.

We can get an element by its number in square brackets.
```JavaScript title:example.js
let fruits = ['Apple', 'Orange', 'Plum'];

alert( fruits[0] ); // Apple
alert( fruits[2] ); // Plum
```

Replace:
```JavaScript title:example.js
fruits[2] = 'Pear'; // now ['Apple', 'Orange', 'Pear']
```

Add:
```JavaScript title:example.js
fruits[3] = 'Lemon'; // now ['Apple', 'Orange', 'Pear', 'Lemon']
```

Find length:
```JavaScript title:example.js
let fruits = ['Apple', 'Orange', 'Plum'];

alert( fruits.length ); // 3
```

Can store elements of any type:
```JavaScript title:example.js
let arr = [
	'Apple',
	{ name: 'John' },
	true,
	function() { alert('hello'); }, // trailing comma
];

alert( arr[1].name ); // John

arr[3](); // hello
```

Get last element with `"at"`:
```JavaScript title:example.js
let fruits = ['Apple', 'Orange', 'Plum'];

alert( fruits.at(-1) ); // Plum
```

So `arr.at(i)`:
- is exactly the same ass `arr[i]`, if `i >= 0`,
- for negative values of `i`, it steps back from the end of the array.

# 📑 → Further reading
[Array - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
[Array: length - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length)
[Array.prototype.at - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/at)
