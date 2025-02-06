# Meta
2025-02-03 18:14
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Method examples

Let’s teach the user to say hello:
```JavaScript title:example.js
let user = {
	name: "John",
	age: 30,
};

user.sayHi = function() {
	alert("Hello!");
};

user.sayHi(); // Hello!
```

A *method* is a function that is a property of an object.

We can use pre-declared functions as methods:
```JavaScript title:example.js
let user = {
	// ...
};

// first, declare
function sayHi() {
	alert("Hello!");
}

// then add as a method
user.sayHi = sayHi;

user.sayHi(); // Hello!
```

There exists a shorthand for methods in object literals. These objects do the same.
```JavaScript title:example.js
user1 = {
	sayHi: function() {
		alert("Hello");
	}
};

user2 = {
	sayHi() {
		alert("Hello");
	}
}
```

# 📑 → Further reading
[Method - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Method)
[Defining methods - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_objects#defining_methods)
