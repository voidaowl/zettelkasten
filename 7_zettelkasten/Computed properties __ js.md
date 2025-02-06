# Meta
2025-02-03 11:04
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Computed properties

We can use square brackets in an object literal, when creating an object. That’s called *computed properties*.
```JavaScript title:example.js
let fruit = prompt("What fruit to buy?", "apple");

let bag = {
	[fruit]: 5,
};

alert( bag.apple ); // 5 if fruit="apple"
```

The meaning of a computed property is simple: `[fruit]` means that the property name should be taken from `fruit`.

We can use more complex expressions inside square brackets:
```JavaScript title:example.js
let fruit = 'apple';
let bag = {
	[fruit + 'Computers']: 5 // bag.appleComputers = 5
};
```

# 📑 → Further reading
[Computed property names - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Object_basics#bracket_notation)
