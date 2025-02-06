# Meta
2025-02-04 12:29
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Symbol type

By specification, only two primitive types may serve as object property keys:
- string type, or
- symbol type.

If one uses another type, such as number, it’s auto-converted to string.

A “symbol” represents a unique identifier. Creation:
```JavaScript title:example.js
let id = Symbol();
```

Upon creation, we can give symbols a description (aka name), mostly useful for debugging:
```JavaScript title:example.js
let id = Symbol("id");
```

Symbols are guaranteed to be **unique**. Even if we create many symbols with the same description, they are different values. The description is merely a label.
```JavaScript title:example.js
let id1 = Symbol("id");
let id2 = Symbol("id");

alert( id1 === id2 ); // false
```

> [!warning] **Symbols don’t auto-convert to a string**

For instance, this `alert` will show an error:
```JavaScript title:example.js
let id = Symbol("id");
alert(id); // TypeError: Cannot convert a Symbol value to a string
```

If we really want to show a symbol, we must explicitly convert it:
```JavaScript title:example.js
let id = Symbol("id");
alert(id.toString()); // Symbol(id)
```

…or get `symbol.description` property to show the description only:
```JavaScript title:example.js
let id = Symbol("id");
alert(id.description); // id
```

# 📑 → Further reading
[Symbol - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol)
[Symbol.prototype.toString() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/toString)
[Symbol.prototype.description - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/description)
