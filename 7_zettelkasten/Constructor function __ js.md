# Meta
2025-02-03 23:00
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Constructor function

Constructor functions follow two conventions:
1. They are named with capital letter first.
2. They should be executed only with the `"new"` operator.

```JavaScript title:example.js
function User(name) {
	this.name = name;
	this.isAdmin = false;
}

let user = new User("Jack");

alert(user.name); // Jack
alert(user.isAdmin); // false
```

When a function is executed with `new`, it does the following:
1. A new empty object is created and assigned to `this`.
2. The function body executes. Usually, it modifies `this`, adds new properties to it.
3. The value of `this` is returned.

The main purpose of constructors is to implement reusable object creation code.

If we have many lines of code all about creation of a single complex object, we can wrap them in an immediately called constructor function:
```JavaScript title:example.js
let user = new function() {
	this.name = "John";
	this.isAdmin = false;
	// ...
}
```

The constructor can’t be called again, because it’s not saved anywhere, just created and called. This trick aims to **encapsulate** the code that constructs the single object, without future reuse.

# 📑 → Further reading
[new - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new)
