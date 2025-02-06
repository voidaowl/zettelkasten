# Meta
2025-02-03 11:16
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Property existence test, “in” operator

Reading a non-existent property returns undefined:
```JavaScript title:example.js
let user = {};

alert( user.noSuchProperty === undefined ); // true
```

There’s a special operator `"in"` to make this simpler. Syntax:
```JavaScript title:example.js
"key" in object
```

Example:
```JavaScript title:example.js
let user = { name: "John", age: 30 };

alert( "age" in user ); // true
alert( "ungabunga" in user ); // false 
```

On the left side of `in` there must be a *property name*, usually a quoted string.

If we omit quotes, that means a variable should contain the actual name to be tested:
```JavaScript title:example.js
let user = { age: 30, }

let key = "age";
alert( key in user ); // true
```

Why use `in`? There’s a special case where comparing to `undefined` fails.
```JavaScript title:example.js
let obj = {
	test: undefined,
}

alert( obj.test ); // undefined

alert( "test" in obj ); // true
```

The property `obj.test` technically exists, so the `in` operator works right.

# 📑 → Further reading
[in - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/in)
