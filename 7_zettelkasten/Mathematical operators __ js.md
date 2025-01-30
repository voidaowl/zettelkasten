# Meta
2025-01-30 13:34
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Terms: “unary”, “binary”, “operand”
An **operand** is what operators are applied to. For example, in `5 * 2` there are two operands, `5` and `2`. Sometimes called *arguments*.

An operator is **unary** if it has a single operand. For example:
```JavaScript title:example.js
let x = 1;

x = -x;
alert( x ); // -1, unary negation
```

An operator is **binary** if it has two operands.

# Operations
The following math operations are supported:
- Addition `+`,
- Subtraction `-`,
- Multiplication `*`,
- Division `/`,
- Remainder `%`,
- Exponentiation `**`.

## Remainder %
The remainder operator `%` isn’t related to percentages. The result of `a % b` is the remainder of the integer division of `a` by `b`.
```JavaScript title:example.js
alert( 5 % 2 ); // 1
alert( 8 % 3 ); // 2
alert( 8 % 4 ); // 0
```

## Exponentiation
The exponentiation operator `a ** b` raises `a` to the power of `b`.
```JavaScript title:example.js
alert( 2 ** 4 ); // 16
alert( 8 ** (1/3) ); // 2
```