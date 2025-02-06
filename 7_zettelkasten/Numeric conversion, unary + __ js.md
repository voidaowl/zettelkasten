# Meta
2025-01-30 13:52
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #pending

# Unary +
If the operand isn’t a number, the unary plus converts it to a number (coercion).
```JavaScript title:example.js
// No effect on numbers
let x = 1;
alert( +x ); // 1

// Converts non-numbers
alert( +true ); // 1
alert( +"" ); // 0
```

It actually does the same thing as `Number(...)`, but is shorter.

# Binary +
The binary plus helps us sum values as strings:
```JavaScript title:example.js
let apples = "2";
let oranges = "3";

alert( apples + oranges ); // "23", still a string
```

If we want to treat them as numbers, we must convert (or coerce) them:
```JavaScript title:example.js
let apples = "2";
let oranges = "3";

alert( +apples + +oranges ); // 5, a number
// alert( Number(apples) + Number(oranges) ) // 5
```

Unary plusses are applied first, converting strings to numbers, and then the binary plus sums them up. Why? [[Operator precedence __ js|operator precedence]].