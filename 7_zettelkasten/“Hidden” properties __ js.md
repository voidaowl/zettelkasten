# Meta
2025-02-04 12:37
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# “Hidden” properties

Symbols allow us to create “hidden” properties of an object, that no other part of the code can accidentally access or overwrite.

For instance, if we’re working with `user` object that belong to 3rd-party code, we’d like to add IDs to them:
```JavaScript title:example.js
let user = {
	name: "John",
};

let id = Symbol("id");

user[id] = 1;

alert( user[id] ); // we can access the data using the symbol as key
```

What’s the benefit using `Symbol("id")` over a string `"id"`?

As `user` objects can belong to another codebase, it’s unsafe to add fields to them, since we might affect pre-defined behavior in that other codebase. However, symbols cannot be accessed accidentally. The 3rd-party code won’t be aware of newly defined symbols, so it’s safe to add symbols to the `user` objects.

Also, imagine another script wanting to have its own identifier inside `user`, for its own purposes.

Then that script can create its own `Symbol("id")`:
```JavaScript title:example.js
// ...
let id = Symbol("id");

user[id] = "Their id value";
```

There will be no conflict between our and their identifiers, because symbols are always different, even if they have the same name.

If we used string `"id"` instead of a symbol for the same purpose, then there would be conflict:
```JavaScript title:example.js
let user = { name: 'Jon' };

user.id = "Our id value";

user.id = "Their id value"; // Overwrites our id
```