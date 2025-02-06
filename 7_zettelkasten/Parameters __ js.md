# Meta
2025-01-31 14:13
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Function parameters
We can pass arbitrary data to functions using *parameters*.
```JavaScript title:example.js
function showMessage(from, text) {
	alert( from + ': ' + text );
}

showMessage('Ann', 'Hello!'); // Ann: Hello
```

A function aways gets a *copy* of the value:
```JavaScript title:example.js
function showMessage(from, text) {
	from = '*' + form + '*';

	alert( from + ': ' + text );
}

let from = 'Ann'

showMessage(from, 'Hello'); // *Ann*: Hello

// the value of 'from' is the same, the function modified a local copy
alert( from ); // Ann
```

When a value is passed as a function parameter, it’s called an *argument*.

A **parameter** is the variable listed inside the parentheses in the function declaration (it’s a *declaration time* term).

An **argument** is the value that is passed to the function when it is called (it’s a *call time* term).

# 📑 → Further reading
[Parameter - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Parameter)
