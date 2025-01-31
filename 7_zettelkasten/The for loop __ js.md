# Meta
2025-01-31 09:50
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# 📷 → What does it look like?
```JavaScript title:example.js
for (begin; condition; step) {
	// ... loop body ...
}
```

# 🔍 → What does it do?
Loops over a set of values from `begin` until the `condition` is `true`, in intervals of `step`.

# ❓ → How it does it.
```JavaScript title:example.js
for (let i = 0; i < 3; i++) {
	alert(i);
}
```

Let’s examine it:

| **part**  |             |                                                                 |
| --------- | ----------- | --------------------------------------------------------------- |
| begin     | `let i = 0` | Executes once upon entering the loop                            |
| condition | `i < 3`     | Checked before every loop iteration. If `false`, the loop stops |
| body      | `alert(i)`  | Runs again and again while the condition is truthy.             |
| step      | `i++`       | Executes after the body on each iteration.                      |

The general loop algorithm works like this:
```Pseudocode title:example
Run begin
-> (if condition -> run body and run step)
-> (if condition -> run body and run step)
-> (if condition -> run body and run step)
...
```

## Inline variable declaration
Here, the “counter” variable `i` is declared right in the loop. This is called an “inline” variable declaration. Such variables are visible only inside the loop.
```JavaScript title:example.js
for (let i = 0; i < 3; i++) {
	alert(i); // 0, 1, 2
}
alert(i); // error, no such variable
```

Instead of defining a variable, we could use an existing one:
```JavaScript title:example.js
let i = 0;

for (i = 0; i < 3; i++) {
	alert(i); // 0, 1, 2
}

alert(i); // 3
```

## Skipping parts
Any part of `for` can be skipped.

We can omit `begin` if we don’t need to do anything at the loop start.
```JavaScript title:example.js
let i = 0;

for (; i < 3; i++) {
	alert(i); // 0, 1, 2
}
```

We can also remove `step`.
```JavaScript title:example.js
let i = 0;

for (; i < 3;) {
	alert( i++ );
}
```

This makes the loop identical to `while (i < 3)`.

We can remove everything, creating an infinite loop.
```JavaScript title:example.js
for (;;) {
	// repeats without limits
}
```

# 📑 → Further reading / Sources
[for - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)