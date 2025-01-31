# Meta
2025-01-31 09:31
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# Precedence
The precedence of the `??` operator is the same as `||`, which is `3`.

That means that `??` is evaluated before `=` and `?`, but after most other operations such as `+`, `*`, etc.

```JavaScript title:example.js
let height = null;
let width = null;

// important: use parentheses
let area = (heigh ?? 100) * (width ?? 50);

alert(area); // 5000
```

If we mot parentheses:
```JavaScript title:example.js
// without parentheses
let area = height ?? 100 * width ?? 50;

// ...works this way (not what we want)
let area = height ?? (100 * width) ?? width;
```

## Using ?? with && or ||
Due to safety reasons, JavaScript forbids using `??` together with `&&` and `||` operators, unless the precedence is explicitly specified with parentheses.

This code triggers a `SyntaxError`:
```JavaScript title:example.js
let x = 1 && 2 ?? 3;

// Use parentheses to work around it
let x = (1 && 2) ?? 3; // 2
```

# 📑 → Further reading
[Nullish coalescing operator (??) - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)