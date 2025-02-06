# Meta
2025-02-03 11:12
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Property name limitations

A variable cannot have be named using a reserved keyword.

For an object property, there’s no such restriction:
```JavaScript title:example.js
let obj = {
	for: 1,
	let: 2,
	return: 3,
};

alert( obj.for + obj.let + obj.return ); // 6
```

Other types are automatically converted to strings:
```JavaScript title:example.js
let obj = {
	0: "test",
};

alert( obj["0"] ); // test
alert( obj[0] ); // test
```

We can’t set it the special value `__proto__` to a non-object value:
```JavaScript title:example.js
let obj = {};
obj.__proto__ = 5;
alert(obj.__proto__); // [object Object]
```