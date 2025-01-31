# Meta
2025-01-31 09:41
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# 📷 → What does it look like?
```JavaScript title:example.js
while (condition) {
	// code
	// so-called "loop body"
}
```

# 🔍 → What does it do?
While the `condition` is truthy, the `code` from the loop body is executed.

# ❓ → How it does it.
```JavaScript title:example.js
let i = 0;
while (i < 3) {
	alert( i );
	i++;
}
```

The code above outputs `i` while `i < 3`.

A single execution of the loop body is called an *iteration*. The loop in the example above performs 3 iterations.

If `i++` was missing, the loop would repeat (in theory) forever.

Any expression or variable can be a loop condition, not just comparisons: the condition is evaluated and converted to a boolean by `while`. For instance, a shorter way to write `while (i != 0)` is `while (i)`:
```JavaScript title:example.js
let i = 3;
while (i) {
	alert( i );
	i--;
}
```

> [!info] Curly braces are not required for a single-line body
```JavaScript title:example.js
let i = 3;
while (i) alert(i--);
```

# 📑 → Further reading / Sources
[while - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while)