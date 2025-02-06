# Meta
2025-02-03 10:59
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Square brackets notation

For multiword properties, dot access doesn’t work:
```JavaScript title:example.js
user.likes birds = true; // SyntaxError
```

Square bracket notation:
```JavaScript title:example.js
let user = {};

// set
user["likes birds"] = true;

// get
alert(user["likes birds"]); // true

// delete
delete user["likes birds"];
```

Square brackets provide a way to obtain the property name as the result of any expression:
```JavaScript title:example.js
let key = "likes birds";

// same as user["likes birds"] = true;
user[key] = true;
```

This provides a great deal of flexibilty:
```JavaScript title:example.js
let user = {
	name: "John",
	age: 30,
};

let key = prompt("What do you want to know about the user?", "name");

// access by variable
alert( user[key] ); // John (if enter "name")
```

The dot notation cannot be used in a similar way.

# 📑 → Further reading
[Bracket notation - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Object_basics#bracket_notation)
