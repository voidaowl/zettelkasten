# Meta
2025-02-04 12:46
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Symbols are skipped by for…in

Symbolic properties do not participate in `for...in` loop.

```JavaScript title:example.js
let id = Symbol("id");
let user = {
	name: "John",
	age: 30,
	[id]: 123,
};

for (let key in user) alert(key); // name, age

// the direct access by the symbol works
alert( "Direct: " + user[id] ); // Direct: 123
```

`Object.keys(user)` also ignores them.

In contrast, `Object.assign` copies both string and symbol properties:
```JavaScript title:example.js
let id = Symbol("id");
let user = {
	[id]: 123
};

let clone = Object.assign({}, user);

alert( clone[id] ); // 123
```

Why? When we clone objects, we usually want *all* properties to be copied, including symbols.

# 📑 → Further reading
[Object.keys() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)
[Object.assign() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/assign)
