# Meta
2025-02-03 22:55
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Arrow functions have no “this”

If we reference `this` from an arrow function, it’s take from the outer “normal” function.
```JavaScript title:example.js
let user = {
	firstName = "Ilyia",
	sayHi() {
		let arrow = () => alert(this.firstName);
		arrow();
	}
};

user.sayHi(); // Ilya
```

