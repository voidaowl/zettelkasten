# Meta
2025-02-03 11:21
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# The “for … in” loop

Walks over all keys of an object. Syntax:
```JavaScript title:example.js
for (key in object) {
	// ...
}
```

Example:
```JavaScript title:example.js
let user = {
	name: "John",
	age: 30,
	isAdmin: true,
};

for (let key in user) {
	// output keys
	alert( key );
	// output values
	alert( user[key] );
}
```

# 📑 → Further reading
[for…in - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)
