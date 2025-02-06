# Meta
2025-02-03 11:41
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Comparison by reference

Two objects are equal only if they are the same object.

Here, `a` and `b` reference the same object, and thus are equal:
```JavaScript title:example.js
let a = {};
let b = a;

alert( a == b ); // true, both vars ref the same obj
alert( a === b ); // true
```

Here, two independent objects are not equal, even if they look alike:
```JavaScript title:example.js
let a = {};
let b = {};

alert( a == b ); // false
```

For comparisons like `obj1 > obj2` or for a comparison against a primitive `obj === 5`, objects are converted to primitives.

> [!info] **Const objects can be modified**
> An object declared as a `const` *can* be modified.

```JavaScript title:example.js
const user = {
	name: "John",
};

user.name = "Pete";

alert(user.name); // Pete
```