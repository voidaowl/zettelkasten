# Meta
2025-01-29 22:10
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# 📷 → What does it look like?
```JavaScript title:example.js
const myBirthday = "18.04.1982"
```

# 🔍 → What does it do?
Creates an immutable reference to a value. In other words, its value cannot be changed.

# ❓ → How it does it.
1. `const` declarations are scoped to blocks as well as functions.
2. `const` declarations can only be accessed after the place of declaration is reached, thus being regarded as [non-hoisted](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting).
3. `const` declarations do not create properties on [`globalThis`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/globalThis) when declared at the top level of a script.
4. `const` declarations cannot be redeclared by any other declaration in the same scope.
5. `const` begins declarations, **not** statements. You cannot use a lone `const` declaration as the body of a block.


# ✅ → Best practice

Use constants as aliases for difficult-to-remember values that are known before execution.

```JavaScript title:example.js
const COLOR_RED = "#f00";
const COLOR_ORANGE = "#ff7f00";
```

Benefits:
1. `COLOR_ORANGE` is much easier to remember than the hex value.
2. It’s much easier to mistype the hex code.
3. `COLOR_ORANGE` is a much more meaningful name for any potential reader.


# 📑 → Further reading / Sources
[const - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
