# Meta
2025-02-04 18:05
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Symbol.keyFor


For global symbols, `Symbol.for(key)` returns a symbol by name.

To return a name by global symbol, we can use `Symbol.keyFor(sym)`.

```JavaScript title:example.js
// get symbol by name
let sym = Symbol.for("name");
let sym2 = Symbol.for("id");

// get name by symbol
alert( Symbol.keyFor(sym) ); // name
alert( Symbol.keyFor(sym2) ); // id
```

The `Symbol.keyFor` internally uses the global symbol registry to look up the key for the symbol. It **does not work** for non-global symbols (returns `undefined`).

All symbols have a `description` property.

```JavaScript title:example.js
let globalSymbol = Symbol.for("name");
let localSymbol = Symbol("name");

alert( Symbol.keyFor(globalSymbol) ); // name
alert( Symbol.keyFor(localSymbol) ); // undefined

alert( localSymbol.description ); // name
```

# 📑 → Further reading
[Symbol.keyFor() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/keyFor)
