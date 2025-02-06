# Meta
2025-02-03 10:53
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Literals and properties

```JavaScript title:example.js
let user = { // an object
	name: "John", // by key "name" store value "John"
	age: 30, // by key "age" store value 30
}
```

A property has a *key* (aka identifier) before colon `":"` and a *value* to the right of it.

Property values are accessible using the dot notation:
```JavaScript title:example.js
// get property values of the object:
alert( user.name ); // John
alert( user.age ); // 30
```

Adding a value:
```JavaScript title:example.js
user.isAdmin = true;
```

Removing a property:
```JavaScript title:example.js
delete user.age;
```

Multiword property names can be used, but must be quoted:
```JavaScript title:example.js
let user = {
	name: "John",
	age: 30,
	"likes birds": true, // multiword property
}
```

The comma after the last property is called a *trailing* comma. Makes it easier to add/remove/move around properties.

# 📑 → Further reading
[Using object initializers - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_objects#using_object_initializers)
