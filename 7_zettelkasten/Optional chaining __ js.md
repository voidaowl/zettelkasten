# Meta
2025-02-04 12:04
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Optional chaining

The optional chaining operator `?.` stops the evaluation if the value before `?.` is `undefined` or `null`, and returns `undefined`.

In other words, `value?.prop`:
- works as `value.prop` if `value` exists,
- otherwise (while `value` is `undefined`/`null`) it returns `undefined`.

Here’s the safe way to access `user.address.street` with optional chaining:
```JavaScript title:example.js
let user = {};

alert( user?.address?.street ); // undefined (no error)
```

Here’s an example with `document.querySelector`:
```JavaScript title:example.js
let html = document.querySelctor('.elem')?.innerHTML; // will be undefined, if there's no '.elem'
```

Reading the address with `user?.address` works even if `user` doesn’t exist:
```JavaScript title:example.js
let user = null;

alert( user?.address ); // undefined
alert( user?.address.street ); // undefined
```

**Note:** the `?.` syntax makes optional the value **before** it, but not any further.

> [!warning] **Don’t overuse optional chaining**
> We should use `?.` only where it’s ok that something doesn’t exist.
> 
> For example, if according to our code logic `user` object must exist, but address is optional, then we should write `user.address?.street`, but not `user?.address?.street`.
> 
> Then, if `user` happens to be undefined, we’ll see an error and fix it.

> [!warning] **The variable before `?.` must be declared**
> If there’s no variable `user` at all, then `user?.anything` triggers an error. The variable must be declared with `let/const/var` or as a function parameter. Optional chaining works only on declared vriables.

# 📑 → Further reading
[Optional chaining - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining)
