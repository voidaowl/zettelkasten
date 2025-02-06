# Meta
2025-02-03 11:09
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Property value shorthand

In real code, we often use existing variables as values for property names. For instance:
```JavaScript title:example.js
function makeUser(name, age) {
	return {
		name: name,
		age: age,
		// ...other properties
	};
}

let user = makeUser("John", 30);
alert(user.name); // John
```

Instead of `name: name`, we can just write `name`:
```JavaScript title:example.js
function makeUser(name, age) {
	return {
	name,
	age,
	// ...
	};
};
```

We can use both normal properties and shorthands in the same object:
```JavaScript title:example.js
let user = {
	name,
	age: 30,
}
```

# 📑 → Further reading
[Object initializer - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Object_basics#bracket_notation)
