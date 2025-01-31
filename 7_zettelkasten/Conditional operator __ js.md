# Meta
2025-01-30 23:26
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# Conditional operator ‘?’
Sometimes, we need to assign a variable depending on a condition.

For instance:
```JavaScript title:example.js
let accessAllowed;
let age = prompt('How old are you?', '');

if (age > 18) {
  accessAllowed = true;
} else {
  accessAllowed = false;
}

alert(accessAllowed);
```

The conditional or ‘ternary’ operator lets us do that in a shorter and simpler way. The syntax is:
```JavaScript title:example.js
let result = condition ? value1 : value2;
```

The `condition` is evaluated. If it’s truthy, then `value1` is returned. Otherwise – `value2`.
```JavaScript title:example.js
let accessAllowed = (age > 18) ? true : false;
```

Technically, we can omit the parentheses around `age > 18`. The ternary operator has a low precedence, so it executes after the comparison.

> [!info] **Note:** In the example above, you can avoid using the ternary operator altogether, because the comparison itself returns `true/false`.

# 📑 → Further reading
[Conditional (ternary) operator - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_operator)