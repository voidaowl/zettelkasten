# Meta
2025-02-04 18:39
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Symbol.toPrimitive

This method should be used name the conversion method:
```JavaScript title:example.js
obj[Symbol.toPrimitive] = function(hint) {
	// code to convert object to primitive
	// it must return a primitive value
	// hint = one of "string", "number", "default"
}
```

If the method `Symbol.toPrimitive` exists, its’ used for al hints, and no more methods are needed.

Here, `user` implements it:
```JavaScript title:example.js
let user = {
	name: "John",
	money: 1000,

	[Symbol.toPrimitive](hint) {
		alert(`hint: ${hint}`);
		return hint == "string" ? `{name: "${this.name}"}` : this.money;
	}
}

// conversion demo
alert(user); // hint: string -> {name: "John"}
alert(+user); // hint: number -> 1000
alert(user + 500); // hint: default -> 1500
```

# 📑 → Further reading
[Symbol.toPrimitive - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/toPrimitive)
[Primitive coercion - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#primitive_coercion)
