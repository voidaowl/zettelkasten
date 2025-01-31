# Meta
2025-01-31 08:59
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# && (AND)
The AND operator is represented with two ampersands `&&`:
```JavaScript title:example.js
result = a && b
```

In classical programming, AND returns `true` if both operands are truthy and `false` otherwise:
```JavaScript title:example.js
alert( true && true ); // true
alert( false && true ); // false
alert( true && false ); // false
alert( false && true ); // false
```

An example with `if`:
```JavaScript title:example.js
let hour = 12;
let minute = 30;

if (hour == 12 && minute == 30) {
	alert('The time is 12:30');
}
```

# AND “&&” finds the first falsy value
Given multiple AND’ed values:
```JavaScript title:example.js
result = value1 && value2 && value3;
```

The AND `&&` operator does the following:
1. Evaluates operands from left to right.
2. For each operand, converts it to a boolean. If the result is `false`, stops and returns the original value of that operand.
3. If all operands have been evaluated (i.e. all were truthy), returns the last operand.

In other words, AND returns the first falsy value or the last value if none were found.

The rules above are similar to OR. The difference is that AND returns the first *falsy* value, while OR returns the first *truthy* value.

```JavaScript title:example.js
alert( 1 && 0 ); // 0
alert( 1 && 5 ); // 5

alert( null && 5 ); // null
alert( 0 && "no matter what" ); // 0

alert( 1 && 2 && null && 3 ); // null

alert( 1 && 2 && 3 ); // 3
```

> [!info] **Precedence of AND `&&` is higher than OR `||`**
> `a && b || c && d` is essentially the same as if the `&&` expressions were in parentheses.

## ⚠️ → Don’t replace `if` with `||` or `&&`!
Sometimes, people use the AND `&&` operator as a “shorter way to write `if`”. For instance:
```JavaScript title:example.js
let x = 1;

(x > 0) && alert( 'Greater than zero!' );
```

The expression in the right part of `&&` would execute only if the evaluation reaches it. That is, only if `(x > 0)` is true, basically an analogue for:
```JavaScript title:example.js
let x = 1;
if (x > 0) alert( 'Greater than zero!' );
```

# 📑 → Further reading
[Logical AND (`&&`) - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND)
