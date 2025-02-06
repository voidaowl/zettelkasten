# Meta
2025-02-03 20:30
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# “this” is not bound
In JavaScript, `this` can be used in any function, even if it’s not a method of an object.

This produces no syntax error:
```JavaScript title:example.js
function sayHi() {
	alert( this.name );
}
```

The value of `this` is evaluated during the run-time, depending on the context.

For instance, here the same function is assigned to two different objects and has different “this” in the calls:
```JavaScript title:example.js
let user = { name: "Jon" };
let admin = { name: "Admin" };

function sayHi() {
	alert( this.name );
}

// use the same function in two objects
user.f = sayHi;
user.f = sayHi;

user.f(); // Jon
admin.f(); // Admin

admin['f'](); // Admin
```

The rule is simple: if `obj.f` is called, then `this` is `obj` during the call of `f`. So it’s either `user` or `admin` in the example above.

> [!info] **Calling without an object `this=undefined`**
> We can call the function without an object at all:

```JavaScript title:example.js
function sayHi() {
	alert(this);
}

sayHi(); // undefined
```

In this case, `this` is `undefined` in strict mode. If we try to access `this.name`, there will be an error.

In non-strict mode the value of `this` in such case will be the *global object*. This is a historical behavior that `"use strict"` fixes.

> [!info] **The consequences of unbound `this`**
> Unlike other programming languages, where `this` is “bound” to an object (e.g. `self` in Python), in JavaScript `this` is “free”, its value evaluated at call-time and independent of method declaration location, but rather dependent on what object is “before the dot”.
> 
> On one hand, a function can be reused by different objects. On the other, the greater flexibility creates more room for error.

