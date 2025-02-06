# Meta
2025-02-05 12:04
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# A primitive as an object

The problem:
1. There are many things one would want to do with a primitive, like a string or a number. It would be great to access them using methods.
2. Primitives must be as fast and lightweight as possible.

The solution:
1. Primitives are still primitive. A single value, as desired.
2. The language allows access to methods and properties of strings, numbers, booleans and symbols.
3. For that to work, a special “object wrapper” that provides extra functionality is created, and then destroyed.

The “object wrappers” are different for each primitive type:
- `String`
- `Number`
- `Boolean`
- `Symbol`
- `BigInt`

> [!warning] **Constructors are for internal use only**
> Some languages like Java allow us to explicitly create “wrapper objects” for primitive using syntax like `new Number(1)` or `new Boolean(false)`.
> 
> In JavaScript, that’s also possible for historical reasons, but **highly unrecommended**.

```JavaScript title:example.js
alert( typeof 0 ); // "number"

alert( typeof new Number(0) ); // "object"
```

Objects are always truthy in `if`:
```JavaScript title:example.js
let zero = new Number(0);

if (zero) { // zero is true, because it's an object
	alert( "zero is truthy?!" );
}
```

Using the same functions `String/Number/Boolean` without `new` is fine. They convert a value to the corresponding type.

> [!warning] **null/undefined have no methods**
> The special primitives `null` and `undefined` are exceptions. They have no corresponding “wrapper objects” and provide no methods. An attempt to access a property of such value would give an error.
