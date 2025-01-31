# Meta
2025-01-31 14:19
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# Default values
If a function is called, but an argument is not provided, the corresponding value becomes `undefined`.

We can specify the so-called “default” (to use if omitted) value for a parameter in the function declaration using `=`:
```JavaScript title:example.js
function showMessage(from, text='no text given') {
	alert( from + ': ' + text);
}

showMessage('Ann'); // Ann: no text given
```

The default value also jumps in if the parameter exists, but strictly equals `undefined`:
```JavaScript title:example.js
showMessage('Ann', undefined); // Ann: no text given
```

Functions can also serve as default parameters:
```JavaScript title:example.js
function showMessage(from, text = anotherFunction()) {
	// anotherFunction() only executed if no text given
	// its result becomes the value of text
}
```

> [!info] **Evaluation of default parameters**
> In JavaScript, a default parameter is evaluated every time the function is called without the respective parameter.

## Alternative default parameters
Sometimes it makes sense to assign default values for parameters at a later stage after the function declaration.

We can check if the parameter is passed during the function execution, by comparing it with `undefined`:
```JavaScript title:example.js
function showMessage(text) {
	// ..

	if (text === undefined) {
		text = 'empty message';
	}

	alert(text);
}

showMessage(); // emtpy message
```

…or we could use the `||` operator:
```JavaScript title:example.js
function showMessage(text) {
	// if text is undefined or otherwise falsy, set it to 'empty'
	text = text || 'empty';
	...
}
```

Modern JavaScript engines support the [[Nullish coalescing operator __ js|nullish coalescing operator]] `??`, it’s better when most falsy values, such as `0`, should be considered normal:
```JavaScript title:example.js
function showCount(count) {
	// if count is undefined or null, show 'unknown'
	alert(count ?? 'unknown')
}

showCount(0); // 0
showCount(null); // unknown
showCount(); // unknown
```

# 📑 → Further reading
[Default parameter - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters)
