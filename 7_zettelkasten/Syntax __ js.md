# Meta
2025-02-01 11:31
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Syntax guidelines
> [!warning] **There are no “you must” rules**
> Nothing is set in stone. These are style preferences, not religious dogmas.

## Curly Braces
The “Egyptian” style is most common:
```JavaScript title:example.js
if (condition) { // <-- opening brace on same line as corresponding keyword
	// ...
}
```

### Variants
Beginners sometimes use braces for single-line constructs. Don’t.
```JavaScript title:example.js
if (n < 0) {alert(`Power: ${n} is not supported`);}
```

Split to a separate line without braces. Don’t. Will produce errors.
```JavaScript title:example.js
if (n < 0)
	alert(`Power ${n} is not supported`)
```

One line without braces – acceptable, if short.
```JavaScript title:example.js
if (n < 0) alert(`Power ${n} is not supproted.`)
```

The best variant:
```JavaScript title:example.js
if (n < 0) {
	alert(`Power ${n} is not supported`)
}
```

## Line Length
Split long lines of code.

Use backticks:
```JavaScript title:example.js
// backtick quotes ` allow to split the string into multiple lines
let str = `
  ECMA International's TC39 is a group of JavaScript developers,
  implementers, academics, and more, collaborating with the community
  to maintain and evolve the definition of JavaScript.
`;
```

…and, for `if` statements:
```JavaScript title:example.js
if (
	id === 123 &&
	moonPhase === 'Waning Gibbous' &&
	zodiacSign === 'Libra'
) {
	letTheSorceryBegin()
}
```

Max line length should be between `80` to `120` characters.

## Indents
**Horizontal indents:** use 2 or 4 spaces or the horizontal tab symbol.
```JavaScript title:example.js
show(parameters,
     aligned, // 5 spaces padding
     one,
     after,
     another
  ) {
  // ...
} 
```

**Vertical indents:** use empty lines to split code into logical blocks.
```JavaScript title:example.js
function pow(x, n) {
	let result = 1;
	//
	for (let i = 0; i < n; i++) {
		result *= x;
	}
	//
	return result;
}
```

Insert an extra newline where it helps to make code more readable. There should be **no more** than **9** lines of code without a vertical indentation.

## Semicolons
A semicolon should be present after each statement, even if it could be skipped.

## Nesting Levels
Try to avoid nesting code too many levels deep.

In a loop, you can use `continue` to avoid extra nesting.

For example, instead of adding a nested `if` conditional, like this:
```JavaScript title:example.js
for (let i = 0; i < 10; i++) {
	if (cond) {
		... // <- one more nesting level
	}
}
```

We can write:
```JavaScript title:example.js
for (let i = 0; i < 10; i++) {
	if (!cond) continue;
	... // <- no extra nesting level
}
```

A similar thing can be done with `if/else` and `return`.

Option 1:
```JavaScript title:example.js
function pow(x, n) {
	if (n < 0) {
		alert("Negative 'n' not supported");
	} else {
		let result = 1;

		for (let i = 0; i < n; i++) {
			result *= x;
		}

		return result;
	}
}
```

Option 2:
```JavaScript title:example.js
function pow(x, n) {
	if (n < 0) {
		alert("Negative 'n' not supported");
		return;
	}

	let result = 1;

	for (let i = 0; i < n; i++) {
		result *= x;
	}

	return result;
}
```

The second one is more readable because the “special case” of `n < 0` is handled early on. Once the check is done we can move on to the “main” code flow without the need for additional nesting.
