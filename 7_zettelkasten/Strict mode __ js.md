# Meta
2025-01-29 21:34
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# 1️⃣ → What does it look like?
```JavaScript title:example.js
// At the top of the script
"use strict"
```

# 2️⃣ → What does it do?
Strict mode makes several changes to the normal JavaScript semantics.

# 3️⃣ → How it does it.
1. Eliminates some JavaScript silent errors by changing them to throw errors.
2. Fixes mistakes by making it difficult for JavaScript to perform optimizations: strict mode code can sometimes be made to run faster than identical “sloppy” code.
3. Prohibits some syntax likely to be defined in future versions of ECMAScript.

# 4️⃣ Variations
## Scripts
```JavaScript title:example.js
// Whole-script stirct mode syntax.
"use strict"
const v = "Hi! I'm strict mode script!";
```

## Functions
```JavaScript title:example.js
function myStrictFunction() {
	// Function-level strict mode syntax
	"use strict";
	function nested() {
		return "And so am I!";
	}
	return `Hi! I'm a strict mode function! ${nested()}`
}
```

> [!warning]
> Using `"use strict"` in functions with [[Rest parameters __ js|rest]], [[Default parameters __ js|default]], [[Destructuring assignment __ js|destructured]] parameters is a [[Syntax error __ js|syntax error]].

## Classes and Modules
The entire contents of [[Classes __ js|JavaScript classes]] and [[Modules __ js|modules]] are strict mode code, with no statement needed to initiate it.

# 📑 → Further reading / Sources
[Stirct mode - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)
