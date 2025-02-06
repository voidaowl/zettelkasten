# Meta
2025-02-03 23:19
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Methods in constructor

We can add methods to `this`:
```JavaScript title:example.js
function User(name) {
	this.name = name;

	this.sayHi = function() {
		alert( "My name is: " + this.name );
	};
}

let jon = new User("Jon");

jon.sayHi(); // May name is: Jon
```