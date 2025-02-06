# Meta
2025-02-04 11:13
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Optional chaining ‘?.’

The optional chaining operator `?.` is a safe way to access nested object properties, even if an intermediate property doesn’t exist.

## The “non-existent propery” problem

Let’s say we have several `user` objects. Most of then have addresses in `user.address`, with the street `user.address.street`, but some didn’t provide them.
```JavaScript title:example.js
let user = {}; // a user without "address" property

alert(user.address.street); // Error!
```

As `user.address` is `undefined`, an attempt to access its `street` fails with an error.

In many practical cases we’d prefer to get `undefined` instead of an error.

In Web development, we can get an object that corresponds to a web page element using a special method call, such as `document.querySelector('.elem')`, and it returns `null` when there’s no such element.
```JavaScript title:example.js
let html = document.querySelector('.elem').innerHTML; // error if '.elem' is 'null'
```

If the element doesn’t exist, we’ll get an error accessing `.innerHTML` property of `null`. In some cases, when the absence of the element is normal, we’d like to avoid the error and just accept `html = null` as the result. How?

The obvious answer would be to check the value with `if` or `?` before accessing the property:
```JavaScript title:example.js
let user = {};

alert(user.address ? user.address.street : undefined);
```

It works, there’s no error, but it’s rather inelegant. Here’s the same for `document.querySelector`:
```JavaScript title:example.js
let hmtl = document.querySelctor('.elem') ? ocument.querySelector('.elem').innerHTML : null;
```

For more deeply nested properties, it becomes even uglier, as more repetitions are required.
```JavaScript title:example.js
let user = {};

alert(user.address ? user.address.street ? user.address.street.name : null);
```

There’s a better way using `&&`:
```JavaScript title:example.js
let user = {};

alert( user.address && user.address.street && user.address.street.name ); // undefined
```

AND’ing the whole path ensures that all components exists (if not, evaluation stops), but also isn’t ideal. That’s why `?.` was added.