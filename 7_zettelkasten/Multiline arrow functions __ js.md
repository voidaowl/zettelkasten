# Meta
2025-01-31 20:11
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Multiline arrow functions
We can enclose multiple expressions and statements in curly braces. The major difference is that curly braces require a `return` within them to return a value (just like regular functions).
```JavaScript title:example.js
let sum  = (a, b) => {
	let result = a + b;
	return result;
}

alert( sum(1, 2) ); // 3
```