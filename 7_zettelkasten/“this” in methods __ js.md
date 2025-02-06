# Meta
2025-02-03 19:16
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# “this” in methods

To access the object it belongs to, a method can use the `this` keyword.

The value of `this` is the object “before dot”, the one used to call the method.

```JavaScript title:example.js
let user = {
	name: "John",
	age: 30,

	sayHi() {
		// "this" is the current object
		alert(this.name);
	}
};

user.sayHi(); // John
```

The value of `this` is `user`.

# 📑 → Further reading
[What is “this”? - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Object_basics#what_is_this)
[this - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
