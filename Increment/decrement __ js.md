# Meta
2025-01-30 18:37
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #pending 

# Increment
Increases a variable’s value by 1:
```JavaScript title:example.js
let counter = 2;
counter++;
alert( counter ); // 3
```

# Decrement
Decreases a variable’s value by 1:
```JavaScript title:example.js
let counter = 2;
counter--;
alert( counter ); // 1
```

# Observations
> [!warning] Important:
> Increment/decrement can only be applied to variables. Trying to use it on a value like `5++` will give an error.

The operators `++` and `--` can be placed either before or after a variable:
	1. When an operator goes **after** a variable, it’s in “postfix” form: `counter++`.
	2. The “prefix” form is when the operator goes **before** the variable: `++counter`.

The difference between the two lies in the returned value of `++`/`--`:
	1. **prefix** form returns the **new value**, while
	2. **postfix** form returns the **old value** (prior to increment/decrement).

An example for **prefix** form:
```JavaScript title:example.js
let counter = 1;
let a = ++counter;

alert(a); // 2
```

An example for **postfix** form:
```JavaScript title:example.js
let counter = 1;
let a = counter++;

alert(a); //1
```