# Meta
2025-02-03 23:14
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Return from constructors

Usually, constructors don’t have a `return` statement. If there is one, the rules are:
1. If `return` is called with an object, then the object is returned instead of `this`.
2. If `return` is called with a primitive, it’s ignored.

In other words, `return` with an object returns that object, in all other cases, `this` is returned.

Override:
```JavaScript title:example.js
function BigUser() {
	this.name = "John";
	return { name: "Godzilla" };
}

alert( new BigUser().name ); // Godzilla
```

Empty `return`:
```JavaScript title:example.js
function SmallUser() {
	this.name = "John";

	return; // <-- returns this
}

alert( new SmallUser().name ); // John
```

> [!info] We can omit parentheses after `new`. Bad style.
