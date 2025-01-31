# Meta
2025-01-30 13:52
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #pending 

# Unary +
The unary plus, or the plus operator `+` applied to a single value doesn’t do anything to numbers. If the operand isn’t a number, the unary plus converts it to a number (coercion).
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
The need to convert strings to numbers arises very often. For example, if we’re getting values from an HTML form field, they’re usually strings. The binary plus helps us sum them as strings:
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