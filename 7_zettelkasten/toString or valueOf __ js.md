# Meta
2025-02-04 18:46
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# toString or valueOf

If there’s no `Symbol.toPrimitive` then JavaScript tries to find methods `toString` and `valueOf`:
- For the `"string"` hint: call `toString`. If it doesn’t exist or if it returns an object instead of a primitive value, then call `valueOf`.
- For other hints: call `valueOf`. If it doesn’t exist or if it returns an object instead of a primitive, call `toString`.

These two methods are not symbols, but “regular” string-named methods. They provide an alternative “old-style” way to implement the conversion.

These methods must return a primitive value. If they return objects, they are ignored.

By default, a plain object has the following:
1. The `toString` method returns a string `"[object Object]"`.
2. The `valueOf` method returns the object itself.

```JavaScript title:example.js
let user = {name: "John"};

alert(user); // [object Object]
alert(user.valueOf() === user); // true
```

Let’s implement these methods to customize the conversion:
```JavaScript title:example.js
let user = {
	name: "John",
	money: 1000,

	// for hint="string"
	toString() {
		return `{name: "${this.name}"}`;
	},

	// for hint="number" or "default"
	valueOf() {
		return this.money;
	}
}

alert(user); // toString -> {name "John"}
alert(+user); // valueOf -> 1000
alert(user + 500); // valueOf -> 1500
```

Often we want a single “catch-all” place to handle all primitive conversions. In this case we can implement `toString` only:
```JavaScript title:example.js
let user = {
	name: "John",

	toString() {
		return this.name;
	}
};

alert(user); // toString -> John
alert(user + 500); // toString -> John500
```

In the absence of `Symbol.toPrimitive` and `valueOf`, `toString` will handle all primitive conversions.

## A conversion can return any primitive type
All primitive-conversion methods do not necessarily return the “hinted” primitive.

There’s no control whether `toString` returns exactly a string, or whether `Symbol.toPrimtive` returns a number if the hint is `"number"`.

The only mandatory thing is these methods must return a primitive, not an object.

# 📑→ Further reading
[String coercion - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/toPrimitive)
[Number coercion - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#numeric_coercion)
