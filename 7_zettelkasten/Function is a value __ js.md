# Meta
2025-01-31 15:12
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# A function is a value
No matter how the function is created, a function is a  value.

We can print the value using `alert()`:
```JavaScript title:example.js
function sayHi() {
	alert("Hello");
}

alert( sayHi ); // shows the function code
```

The last line **doesn’t run** the function, because there are no parentheses after `sayHi`.

We can copy a function to another variable:
```JavaScript title:example.js
function sayHi() { // (1)
	alert( 'Hello' );
}

let func = sayHi; // (2)

func(); // Hello // (3)
sayHi(); // Hello
```

What’s going on?
1. The function declaration `(1)` creates a function and puts it into the variable named `sayHi`.
2. `(2)` copies it into the variable `func`. Note that there are not parentheses after `sayHi`. If there were, `func = sayHi()` would write *the result of the call* `sayHi()` into `func`, not *the function* `sayHi` itself.
3. `(3)` – now the function can be called as both `sayHi()` and `func()`.

We could also have used a function expression to declare `sayHi` in the first line:
```JavaScript title:example.js
let sayHi = function() {
	alert( 'Hellow' );
};

let func = sayHi;
// ...
```

Everything would work the same.

> [!info] **Why is there a semicolon at the end?**
> The semicolon at the end of a function expression is recommended because a function expression is essentially a function assigned (with `=`) to a name.
