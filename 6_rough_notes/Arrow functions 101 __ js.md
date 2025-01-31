# Meta
2025-01-31 19:10
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# 📷 → What does it look like?
```JavaScript title:example.js
func = (arg1, arg2, ..., argN) => expression;
```

# 🔍 → What does it do?
This creates a function `func` that accepts arguments `arg1, ... argN`, then evaluates the `expression` on the right side with their use and returns its result.

# ❓ → How it does it.
Let’s see a concrete example.
```JavaScript title:example.js
let sum = (a, b) => a + b;

alert( sum(1, 2) ); // 3
```

If we have only one argument, the parentheses around parameters can be omitted, making that even shorter.
```JavaScript title:example.js
let double = n => n * 2;

alert( double(3) ); // 6
```

If there are no arguments, parentheses are empty, but they must be present:
```JavaScript title:example.js
let sayHi = () => alert('Hello!');

sayHi(); // Hello!
```

Arrow functions can be used in the same way as function expressions.

For instance, to dynamically create functions:
```JavaScript title:example.js
let age = prompt('What is your age?', 18);

let welcome = (age < 18) ?
	() => alert('Hello!') :
	() => alert('Greetings!');

welcome();
```

Arrow functions may appear unfamiliar and not very readable at first, but that quickly changes as the eyes get used to the structure.

They are very convenient for simple one-line actions.

# 📑 → Further reading / Sources
[Arrow function expressions - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
