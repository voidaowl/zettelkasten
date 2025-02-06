# Meta
2025-02-04 18:28
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Hints
There are three variants of type conversion that happen in various situations. They are called “hints” in the specification.

## “string”
For an object-to-string conversion, when we’re doing an operation on an object that expects a string, like `alert`:
```JavaScript title:example.js
// output
alert(obj);

// using object as a property key
anortherObj[obj] = 123;
```

## “number”
For an object-to-number conversion, like when we’re doing math:
```JavaScript title:example.js
// explicit conversion
let num = Number(obj);

// math (except binary plus)
let n = +obj;
let delta = date1 - date2;

// less/greater comparison
let greater = user1 > user2;
```

## “default”
Occurs in rare cases when the operator is “not sure” what type to expect.

For instance, binary plus `+` can work both with strings (concatenates them) and numbers (adds them). So if a binary plus gets an object as an argument, it uses the `"default"` hint to convert it.

If an object is compared using `==` with a string, number, or symbol, it’s also unclear which conversion should be done, so the `"default"` hint is used.
```JavaScript title:example.js
// binary plus
let total = obj1 + obj2;

// obj == number
if (user == 1) { ... };
```

The greater and less comparison operators, such as`<` and `>`, can work with both strings an numbers. Still, they use the `"number"` hint, **not** `"default"`.

In practice, things are a bit simpler.

All built-in objects except for `Date` implement `"default"` conversion the same way as `"number"`.

**To do the conversion, JavaScript tries to find and call three object methods:**
1. Call `obj[Symbol.toPrimitive](hint)` – the method with the symbolic key `Symbol.toPrimitive` (system symbol), if such a method exists,
2. Otherwise if hint is `"string"`:
	- try calling `obj.toString()` or `obj.valueOf()`, whatever exists,
3. Otherwise if hint is `"number"` or `"default"`:
	- try calling `obj.valueOf()` or `obj.toString()`, whatever exists.

# 📑 → Further reading
[toPrimitive - ECMAScript Specification](https://tc39.es/ecma262/#sec-toprimitive)
