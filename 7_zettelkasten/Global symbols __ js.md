# Meta
2025-02-04 12:51
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Global symbols

Sometimes we want same-named symbols to be same entities. For instance, different parts of our application want access symbol `"id"` meaning exactly the same property.

To achieve that, there exists a *global symbol registry*. We can create symbols in it and access them later, and it guarantees that repeated accesses by the same name return exactly the same symbol.

In order to read (create if absent) a symbol from the registry, use `Symbol.for(key)`.

The call checks the global registry, and if there’s a symbol described as `key`, then returns it, otherwise creates a new symbol `Symbol(key)` and stores it in the registry by the give `key`.
```JavaScript title:example.js
// read from the global registry
let id = Symbol.for("id"); // if symbols doesn't exist, create it

// red it again
let idAgain = Symbol.for("id");

// the same symbol
alert( id === idAgain ); // true
```

Symbols inside the registry are called *global symbols*, and can be used application-wide.

# 📑 → Further reading
[Symbold.for() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/for)
