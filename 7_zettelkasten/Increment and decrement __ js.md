# Meta
2025-01-30 18:37
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

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

To summarize:
1. If the result of increment/decrement is not used, there is no difference in which form to use.
2. If we’d like to increase a value *and* immediately use the result of the operator, we need the **prefix** form.
3. If we’d like to increment a value but use its previous value, we need the postfix form.

> [!info] **Increment/decrement among other operators**
> The operators `++/--` can be used inside expressions as well. Their precedence is higher than most other arithmetic operations.

For example:
```JavaScript title:example.js
let counter = 1;
alert( 2 * ++counter ); // 4
```

Compare with:
```JavaScript title:example.js
let counter = 1;
alert( 2 * counter++ ); // 2
```

# ✅ → Best practice
One line – one action, for predictable results and increased readability:
```JavaScript title:example.js
let counter = 1;
alert( 2 * counter ); // 2
counter++;
alert(counter); // 3
```

# 📑 → Further reading
[Increment (++)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Increment)
[Decrement (--)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Decrement)