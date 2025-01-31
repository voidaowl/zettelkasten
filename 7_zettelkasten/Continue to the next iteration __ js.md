# Meta
2025-01-31 11:52
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# continue
The `continue` directive is a “lighter version” of `break`. It doesn’t stop the whole loop, but stops the current iteration and forces the loop to start a new one (if the condition allows).

We can use it if we’re done with the current iteration and would like to move on to the next one.

The loop below uses `continue` to output only odd values:
```JavaScript title:example.js
for (let i = 0; i < 10; i++) {
	if (i % 2 == 0) continue;
	alert(i); // 1, 3, 5, 7, 9
}
```

> [!info] **The `continue` directive helps decrease nesting**

A loop that shows odd values could look like this:
```JavaScript title:example.js
for (let i = 0; i < 10; i++) {
	if (i % 2) {
		alert( i );
	}
}
```

This is identical to the example above, but less readable.

> [!warning] **No `break/continue` to the right side of `?`**

Syntax constructs that are not expressions cannot be used with the ternary operator `?`. In particulars, directives such as `break` or `continue` are **not allowed**.

```JavaScript title:example.js
(i > 5) ? alert(i) : continue; // Error
```

# 📑 → Further reading
[continue - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/continue)
