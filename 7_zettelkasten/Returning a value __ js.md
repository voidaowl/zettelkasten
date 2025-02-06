# Meta
2025-01-31 14:32
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Returning a value
A function can return a value back into the calling code as the result.
```JavaScript title:example.js
function sum(a, b) {
	return a + b;
}

let result = sum(1, 2);
alert( result ); // 3
```

The directive `return` can be in any place of the function. When the execution reaches it, the function stops, and the value is returned to the calling code (assigned to `result` above).

There may be many occurrences of `return` in a single function.
```JavaScript title:example.js
function checkAge(age) {
	if (age >= 18) {
		return true;
	} else {
		return confirm('Do you have permission from your parents?');
	}
}

let age = promtp('How old are you?', 18);

if ( checkAge(age) ) {
	alert( 'Access granted' );
} else {
	alert( 'Access denied' );
}
```

It’s possible to use `return` without a value. That causes the function to exit immediately.
```JavaScript title:example.js
function showMovioe(age) {
	if ( !checkage(age) ) {
		return;
	}

	alert( 'Showing you the movie!' ); // (*)
	// ...
}
```

In the code above, if `checkAge(age)` returns `false`, then `showMovie` won’t proceed to the `alert`.

> [!info] **A function with an empty `return` or without it returns `undefined`**

If a function doesn’t return a value, it’s the same as if it returns `undefined`:
```JavaScript title:example.js
function doNothing() { /* empty */ }

alert( doNothing() === undefined ); // true
```

An empty `return` is also the same as `return undefined`:
```JavaScript title:example.js
function doNothing() {
	return;
}

alert( doNothing() === undefined ); // true
```

> [!warning] **Never add a newline between `return` and a value**

For a long expression in `return`, it might be tempting to put it on a separate line, like this:
```JavaScript title:example.js
return
	(some + long + expression * f(a) + f(b))
```

That doesn’t work, because JavaScript assumes a semicolon after `return`.

If we want the returned expression to wrap across multiple lines, we should start it at the same line as `return`, or at least put the opening parentheses there.

# 📑 → Further reading
[return - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/return)
[Function return values - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Return_values)
