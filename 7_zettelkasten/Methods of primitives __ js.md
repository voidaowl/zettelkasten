# Meta
2025-02-05 11:55
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Methods of primitive

A **primitive**:
- is a value of a primitive type,
- there are 7 primitive types:
	- `string`
	- `number`
	- `bigint`
	- `boolean`
	- `symbol`
	- `null`
	- `undefined`

An object:
- is capable of storing multiple values as properties,
- can be created with `{}`, declaring an *object literal*. There are other kinds of objects in JavaScript, such as *functions*.

We can store a function as an object property, a *method*:
```JavaScript title:example.js
let jon = {
	name: 'Jon',
	sayHi: function() {
		alert('Hi buddy!');
	}
};

jon.sayHi(); // Hi buddy!
```

Objects require additional resources to support the internal machinery.

# 📑 → Further reading
[Method - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Method)
[Method definitions - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Method_definitions)