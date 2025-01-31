# Meta
2025-01-31 18:42
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# Function expression vs function declaration
How to differentiate between them in code.
1. *Function declaration:* a function, declared as a separate statement, in the main code flow:
2. *Function expression:* a function, created inside an expression or inside another syntax construct. Here, the function is created on the right side of the “assignment expression” `=`.
```JavaScript title:example.js
// Function declaration
function sum(a, b) {
	return a + b;
}

// Function expression
let sum = function(a, b) {
	return a + b;
}
```

The more subtle difference is *when* a function is created by the JavaScript engine.

**A function expression is created when the execution reaches it an is usable only from that moment.**

Once the execution flow passes to the right side of the assignment `let sum = function...` – here we go, the function is created and can be used (assigned, called, etc.) from now on.

**A function declaration can be called earlier than it is defined.**

For example, a global function declaration is visible in the whole script, no matter where it is.

That’s due to internal algorithms. When JavaScript prepares to run the script, it first looks for global function declarations in it and creates the functions. We can think of it as an “initialization stage”.

After all function declarations are processed, the code is executed. So it has access to the functions.

For example, this works:
```JavaScript title:example.js
sayHi('Jon'); // Hello, Jon

function sayHi(name) {
	alert( `Hello, ${name}` );
}
```

If it were a function expression, it wouldn’t work:
```JavaScript title:example.js
sayHi('Jon'); // error!

let sayHi = function(name) {
	alert( `Hello, ${name}` );
}
```

Function expressions are created when the execution reaches them.

Another special feature of function declarations is their **block scope**.

**In strict mode, when a Function Declaration is within a code block, it’s visible everywhere inside the block, but not outside of it.**

For instance, let’s imagine that we need to declare a function `welcome()` depending on the `age` variable that we get during runtime. And then we plan to use it some time later.

If we use function declaration, it won’t work as intended:
```JavaScript title:example.js
let age = prompt("What's your age?", 18)

// conditionally declare a function
if (age < 18) {
	function welcome() {
		alert('Hello!');
	}
} else {
	function welcome() {
		alert('Greetings!')
	}
}

// ... use it later
welcome() // Error: welcome is not defined
```

That’s because a function declaration is only visible inside the code block in which it resides.

Here’s another example:
```JavaScript title:example.js
let age = 16;

if (age < 18) {
	welcome(); // (runs)

	function welcome() {
		alert('Hello!');
	}

	welcome(); // (runs)
} else {

	function welcome() {
		alert('Greetings!')
	}
}

welcome(); // Error: welcome is not defined
```

What can we do to make `welcome` visible outside of `if`?

The correct approach would be to use a function expression and assign `welcome` to the variable that’s declared outside of `if` and has the proper visibility.

This code works as intended:
```JavaScript title:example.js
let age = prompt("What's your age?", 18);

let welcome;

if (age < 18) {
	welcome = function() {
		alert("Hello!");
	};
} else {
	welcome = function() {
		alert("Greetings!");
	};
}

welcome(); // ok know
```

We can simplify it even further using a ternary operator.
```JavaScript title:example.js
let age = prompt("What's your age?", 18);

let welcome = (age < 18) ?
	function() { alert("Hello!"); } :
	function() { alert("Greetings!"); };

welcome(); // ok now
```

> [!info] **When to choose Function Declaration versus Function Expression?**
> As a rule of thumb, when we need to declare a function, the first thing to consider is function declaration syntax. It gives more freedom in how to organize our code, because we can call such functions before they are declared.
> 
> That’s also better for readability, as it’s easier to look up `function f(...) {...}` in the code than `let f = function(...) {...}`. Function declarations are more “eye-catching”.
> 
> …but if a Function Declaration does not suit us for some reason, or we need a conditional declaration (we’ve just seen an example), then Function Expression should be used.