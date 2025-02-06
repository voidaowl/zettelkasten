# Meta
2025-02-04 12:44
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Symbols in an object literal

If we want to use a symbol in an object literal, we must use square brackets around it.

```JavaScript title:example.js
let id = Symbol("id");

let user = {
	name: "John",
	[id]: 123 // not "id": 123
};
```

That’s because we need the value from the variable `id` as the key, not the string “id”.