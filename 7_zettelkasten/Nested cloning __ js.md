# Meta
2025-02-03 17:56
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Nested cloning

Properties can be references to other objects, like so:
```JavaScript title:example.js
let user = {
	name: "John",
	sizes: {
		height: 182,
		width: 50,
	}
};

alert( user.sizes.height ); // 182
```

Now it’s not enough to copy `clone.sizes = user.sizes`, because `user.sizes` is an object, and will be copied by reference, so `clone` and `user` will share the same sizes:
```JavaScript title:example.js
let user = {
	// --snip--
};

let clone = Object.assing({}, user);

alert( user.sizes === clone.sizes ); // true

user.sizes.width = 60; //  change a property from one
alert(clone.sizes.width); // 60, get result from other
```

To address that, we use `structuredClone(object)`, which clones the object with all its nested properties:
```JavaScript title:example.js
let user = {
	// --snip--
};

let clone = structuredClone(user);

alert( user.sizes === clone.sizes ); // false

user.sizes.width = 60;
alert(clone.sizes.width); // 50
```

`structuredClone` can clone most data types, and supports circular references, when an object property references the object itself (directly or via chain references).
```JavaScript title:example.js
let user = {};

user.me = user;

let clone = structuredClone(user);
alert(clone.me === clone); // true
```

`structuredClone` **fails** when an object has a function property:
```JavaScript title:example.js
// error
structuredClone({
	f: function() {}
})
```

To handle such complex cases, we may need to use a combination of cloning methods, write custom code or, to not reinvent the wheel, take an existing implementation such as `cloneDeep(obj)` from the JavaScript library `lodash`.

# 📑 → Further reading
[Window: structuredClone() method - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Window/structuredClone)
[The structured clone algorithm - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Structured_clone_algorithm)
[_.cloneDeep(value) | Lodash](https://lodash.com/docs/4.17.15#cloneDeep)
[Lodash](https://lodash.com/docs/)
