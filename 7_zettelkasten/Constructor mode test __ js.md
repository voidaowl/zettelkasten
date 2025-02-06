# Meta
2025-02-03 23:08
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Constructor mode test: new.target

Inside a function, we can check whether it was called with `new` or without it, using a special `new.target` property.

It’s `undefined` for regular calls and equals the function if called with `new`:
```JavaScript title:example.js
function User() {
	alert(new.target);
}

// without "new":
User(); // undefined

// with "new":
new User(); // function
```

That can be used inside the function to know whether it was called with `new`, in “constructor mode”, or without it, in “regular” mode.

We can also make both `new` and regular calls to do the same, like so:
```JavaScript title:example.js
function User(name) {
	if (!new.target) {
		return new User(name);
	}

	this.name = name;
}

let john = User("John"); // redirects call to new User()
alert(john.name); // John
```

# 📑 → Further reading
[new.target - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new.target)
