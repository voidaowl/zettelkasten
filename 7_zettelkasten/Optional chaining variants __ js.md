# Meta
2025-02-04 12:16
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Other variants: ?.(), ?.[]

The optional chaining `?.` is not an operator, but a special syntax construct, that also works with functions and square brackets.

`?.()` is used to call a function that may not exist.
```JavaScript title:example.js
let userAdmin = {
	admin() {
		alert("I am admin");
	}
};

let userGuest = {};

userAdmin.admin?.(); // I am admin

userGuest.admin?.(); // nothing happens
```

`?.[]` also works, if we’d like to use square brackets to access properties instead of dot.
```JavaScript title:example.js
let key = "firstName";

let user1 = {
	firstName: "John",
};

let user2 = null;

alert( user1?.[key] ); // John
alert( user2?.[key] ); // undefined
```

We can use `?.` with `delete`:
```JavaScript title:example.js
delete user?.name;
```

> [!warning] **We can use optional chaining for safe reading and deleting, but not writing**
> The optional chaining `?.` has no use on the left sign of an assignment.

```JavaScript title:example.js
let user = null;

user?.name = "Jon"; // Error -> undefined = "Jon"
```