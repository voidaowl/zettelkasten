# Meta
2025-01-31 11:59
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# label
Sometimes we need to break out from multiple nested loops at once.

For example, in the code below we loop over `i` and `j`, prompting for the coordinates `(i, j)` from `(0, 0)` to `(2, 2)`.

```JavaScript title:example.js
for (let i = 0; i < 3; i++) {
	for (let j = 0; j < 3; j++) {
		let input = prompt(`Value at coords (${i},${j})`, '')
		// What if we want to exit from here to "Done", bellow?
	}
}

alert('Done!')
```

We need a way to stop the process if the user cancels the input.

The ordinary `break` after `input` would only break the inner loop, so we use `label`.

A *label* is an identifier with a colon before the loop:
```JavaScript title:example.js
labelName: for (...) {
	...
}
```

So, let’s change the code above:
```JavaScript title:example.js
outer: for (let i = 0; i < 3; i++) {
	for (let j = 0; j < 3; j++) {
		let input = prompt(`Value at coords (${i},${j})`, '')
		if (!input) break outer;
		// do something with the value ...
	}
}

alert('Done!');
```

We can also move the label onto a separate line:
```JavaScript title:example.js
outer:
for (let i = 0; i < 3; i++) {
	...
}
```

> [!warning] **Labels do not allow to “jump” everywhere**

Labels don’t allow us to jump into an arbitrary place in the code.

For example, it’s impossible to do this:
```JavaScript title:example.js
break label; // jump to the label bellow, doens't work

label: for (...) { ... }
```

A `break` directive must be inside a code block. Technically, any labelled code block will do, e.g.:
```JavaScript title:example.js
label: {
	// ...
	break label; // works
	// ...
}
```

…although 99.9% of the time `break` is used inside loops, as we’ve seen in the examples above.

A `continue` is only possible from inside a loop.

# 📑 → Further reading
[Labeled statement - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/label)
