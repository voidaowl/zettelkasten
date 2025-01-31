# Meta
2025-01-31 15:09
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# 📷 → What does it look like?
```JavaScript title:example.js
let sayHi = function() {
	lert( 'Hello!' );
}
```

# 🔍 → What does it do?
Allows us to create a new function in the middle of any expression.

# ❓ → How it does it.
As the function creation happens in the context of the assignment expression, this is a *function expression*.

Note that there’s no name after the `function` keyword. Omitting a name is allowed in function expressions.

In more advanced situations, a function may be created and immediately called or scheduled for later execution, not stored anywhere, thus remaining anonymous.

# 📑 → Further reading / Sources
[function expression - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function)
[Function expressions - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions#function_expressions)
