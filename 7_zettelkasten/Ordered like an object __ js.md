# Meta
2025-02-03 11:32
**Tags:** [[JavaScript]]
**Activity:** #learning
**Status:** #completed 

# Ordered like an object

Objects key-property pairs are ordered in a special fashion:
- *integer* properties are sorted,
- others appear in creation order.

Example:
```JavaScript title:example.js
let codes = {
	"49": "Germany",
	"41": "Switzerland",
	"44": "Great Britain",
	// ...
	"1": "USA",
}

for (let code in codes) {
	alert(code); // 1, 41, 44, 49
}
```


> [!info] **Integer properties?**
> The *integer property* is a string that can be converted to-and-from an integer without change.

On the other hand, if the keys are non-integer, then they are listed in creation order:
```JavaScript title:example.js
let user = {
	name: "John",
	surname: "Smith",
};
user.age = 25;

for (let prop in user) {
	alert( prop ); // name, surname, age
}
```