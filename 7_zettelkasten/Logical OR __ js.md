# Meta
2025-01-30 23:39
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Logical OR
The “OR” operator is represented with two vertical line symbols:
```JavaScript title:example.js
result = a || b;
```

Logical combinations:
```JavaScript title:example.js
alert( true || true ); // true
alert( false || true ); // true
alert( true || false ); // true
alert( false || false ); // false
```

If an operand isn’t a boolean, it’s converted toa boolean for the evaluation.
```JavaScript title:example.js
if (1 || 0) {
	alert('truthy!');
}
```

Most of the time, OR `||` is used in an `if` statement to test if *any* of the given conditions is `true`.
```JavaScript title:example.js
let hour = 12;
let isWeekend = true;

if (hour < 10 || hour > 18 || isWeekend) {
	alert('The office is closed.');
}
```

# OR finds the first truthy value
Given multiple values:
```JavaScript title:example.js
result = value1 || value2 || value3
```

The OR `||` operator does the following:
1. Evaluates operands from left to right.
2. For each operand, converts it to a boolean. If the result is `true`, stops and returns the original value of that operand.
3. If all operands have been evaluated (i.e. all were `false`), returns the last operand.

A value is returned in its original form, without the conversion.

In other words, a chain of OR `||` returns the first truthy value or the last one if no truthy value is found.
```JavaScript title:example.js
alert(1 || 0); // 1

alert(null || 1); // 1
alert(null || 0 || 1); // 1

alert(undefined || null || 0); // 0
```

This leads to some interesting use compared to a “pure, classical, boolean-only OR”.

## Getting the first truthy value from a list
```JavaScript title:example.js
let firstName = "";
let lastName = "";
let nickName = "SuperCoder";

alert(firstName || lastName || nickName || "Anonymous"); // "SuperCoder"
```

## Short-circuit evaluation
The importance of this feature becomes obvious if an operand isn’t just a value, but an expression with a side effect, such as a variable assignment or a function call.
```JavaScript title:example.js
true || alert('not printed');
false || alert('printed');
```

# 📑 → Further reading
[Logical OR (`||`) - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_OR)