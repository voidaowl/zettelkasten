# Meta
2025-01-31 12:08
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# 📷 → What does it look like?
```JavaScript title:example.js
switch (x) {
	case 'value1': // if (x === 'value1')
		...
		[break]

	case 'value2': // if (x === 'value2')
		...
		[break]

	default:
		...
		[break]
}
```

# 🔍 → What does it do?
Replaces multiple `if` checks, offering a more descriptive way to compare a value with multiple variants.

# ❓ → How it does it.
The `switch` has one or more `case` blocks and an optional `default`.

In the example above:
1. The value `x` is checked for a *strict* equality `===` to the value from the first `case` (i.e., `value1`), then to the second value (`value2`) and so on.
2. If the equality is found, `switch` starts to execute the code starting from the corresponding `case`, until the nearest `break` (or until the end of `switch`).
3. If no case is matched, then the `default` code is executed (if it exists).

# ⚒️ → A practical example
```JavaScript title:example.js
let a = 2 + 2;

switch (a) {
	case 3:
		alert( 'Too small' );
		break;
	case 4:
		alert( 'Exactly!' ); // (*)
		break;
	case 5:
		alert( 'Too big' );
		break;
	default:
		alert( "I don't know such values" );
}
```

**If there is no `break` then the execution continues with the next `case` without any checks!**

```JavaScript title:example.js
let a = 2 + 2;

switch (a) {
	case 3:
		alert( 'Too small' );
	case 4:
		alert( 'Exactly!' );
	case 5:
		alert( 'Too big' );
	default:
		alert( "I don't know such values" );
}

/* All of these will be executed:
alert( 'Exactly!' );
alert( 'Too big' );
alert( "I don't know such values" )
```

> [!info] **Any expression can be a `switch/case` argument**

Both `switch` and `case` allow arbitrary expressions:
```JavaScript title:example.js
let a = "1";
let b = 0;

switch (+a) {
	case b + 1:
		alert("this runs, because +a is 1, exactly equals b+1")
		break
	default:
		alert("this doesn't run");
}
```

# Grouping of “case”
Several variants of `case` which share the same code can be grouped.
```JavaScript title:example.js
let a = 3;

switch (a) {
	case 4:
		alert('Right!');
		break;

	case 3: // (*) grouped two cases
	case 5:
		alert('Wrong!')
		alert('Go take a math class!');
		break;

	default:
		alert('The result is strange.')
}
```

The ability to “group” cases is a side effect of how `switch/case` works without `break`. Here the execution of `case 3` starts from the line `(*)` and goes through `case 5`, because there’s no `break`.

# Type matters
```JavaScript title:example.js
let arg = prompt("Enter a value?");
switch (arg) {
	case '0':
	case '1':
		alert( 'One or zero' );
		break;

	case '2':
		alert( 'Two' );
		break;

	case 3: // (*) - this is type "Number"
		alert( 'Never executes!' );
		break;

	default:
		alert( 'An unknown value' );
}
```

# 📑 → Further reading / Sources
[switch - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch)
