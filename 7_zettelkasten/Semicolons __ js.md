# Meta
2025-01-29 21:26
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Semicolons
A semicolon may be omitted in most cases when a line breaks exists, but “in most cases” **does not** mean “always”.
```JavaScript title:example.js
console.log(3 +
1
+ 2);
```

The above outputs `6`. It is intuitively obvious that if the line ends with a `+`, then it is an incomplete expression. The expression works as intended, but it is a **bad practice**.

> [!info] An example of an error
> 
```JavaScript title:example.js
alert("Hello")

[1, 2].forEach(alert);
```

While the expression on line `1` executes correctly, the 2nd produces a `TypeError: alert(...) is undefined` error. JavaScript **does not** assume a semicolon before square brackets.