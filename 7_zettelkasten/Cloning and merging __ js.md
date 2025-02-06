# Meta
2025-02-03 11:45
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Object.assign

Copying all user properties from one object to another using `for...in`:
```JavaScript title:example.js
let user = {
	name: "John",
	age: 30,
};

let clone = {}; // the new empty object

for (let key in user) {
	clone[key] = user[key];
}

clone.name = "Pete";

alert( user.name ); // John
```

Using `Object.assing`, the syntax is:
```JavaScript title:example.js
Object.assign(dest, ...sources)
```

`dest` is a target object, while further arguments are a list of source objects.

```JavaScript title:example.js
let user = { name: "John" };

let permissions1 = { canView: true };
let permission2 = { canEdit: true };

Object.assign(user, permissions1, permissions2);

alert(user.name); // John
alert(user.canView); // true
alert(user.canEdit); // true
```

If the copied property name already exists, it gets overwritten:
```JavaScript title:example.js
let user = { name: "John" };

Object.assign(user, { name: "Pete" });

alert(user.name); // Pete
```

We can also use `Object.assign` to perform a simple object cloning:
```JavaScript title:example.js
let user = {
	name: "John",
	age: 30,
}

let clone = Object.assign({}, user);

alert(clone.name); // John
alert(clone.age); // 30
```

# 📑 → Further reading
[Object.assign - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/assign)
