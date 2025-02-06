# Meta
2025-02-06 22:32
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# The rare “thisArg” parameter
Almost all array methods that call functions, with a notable exception of `sort`, accept an optional parameter `thisArg`.

Here’s the full syntax of these methods:
```JavaScript title:example.js
arr.find(func, thisArg);
arr.filter(func, thisArg);
arr.map(func, thisArg);
```

The value of `thisArgue` parameter becomes `this` for `func`.

For example, here we use a method of `army` object as a filter, and `thisArg` passes the context:
```JavaScript title:example.js
let army = {
	minAge: 18,
	maxAge: 27,
	canJoin(user) {
		return user.age >= this.minAge && user.age < this.maxAge;
	}
};

let users = [
	{age: 16},
	{age: 20},
	{age: 23},
	{age: 30},
];

// find users, for whom army.canJoin returns true
let soldiers = users.filter(army.canJoin, army);

alert(soldiers.length); // 2
alert(soldiers[0].age); // 20
alert(soldiers[1].age); // 23
```