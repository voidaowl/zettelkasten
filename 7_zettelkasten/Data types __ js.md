# Meta
2025-01-29 22:28
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Number
```JavaScript title:example.js
let n = 123;
n = 12.345;
```

The *number* type represents both integers and floating point numbers. Besides regular numbers, there are also “special numeric values”: `Infinity`, `-Infinity`, and `NaN`.

`Infinity` is the mathematical infinity. It’s a special value, greater than any number. We can obtain it by dividing by `0` or we can reference it directly.

`NaN` represents a computational error. Any mathematical operation involving `NaN` will result in `NaN` (we call it “sticky”).

# BigInt
```JavaScript title:example.js
const bigInt = 1234567890123456789012345678901234567890n;
```

In JavaScript, the “number” type can’t safely represent integer values larger than `2^53-1` (or `9007199254740991`), or less than `-2^53-1` for negatives.

For that reason, `BigInt` was recently added to the language to represent integers of arbitrary length. A `BigInt` value is create by appending `n` to the end of an integer.

# String
```JavaScript title:example.js
let str = "Hello";
let str2 = 'Single quotes are fine too';
let phrase = `can embed another ${str}`;
```

Double and single quotes are “simple” quotes. Backticks have extended functionality – they allow us to embed variables and expressions into a string by wrapping them inside `${...}`.


# Boolean
```JavaScript title:example.js
let nameFieldChecked = true;
let ageFieldChecked = false;
```

The Boolean type has only two values: `true` (equivalent to `1`) and `false` (equivalent to `0`).

# The “null” value
```JavaScript title:example.js
let age = null;
```

The special `null` value contains only the `null` value.

In JavaScript, `null` isn’t a reference to a non-existing object, or a null pointer like in some other languages. It’s just a special value which represents “nothing”, “empty”, or “value unknown”.

# The “undefined” value
The meaning of `undefined` is “value not assigned”.
```JavaScript title:example.js
let age;

console.log(age); // "undefined"
```

It’s possible to explicitly assign `undefined` to a variable, but it’s a **bad practice**. Normally, we use `null` to assign an “empty” or “unknown” value to a variable, while `undefined` is reserved as a default initial value for unassigned things.

# Objects and Symbols
The `object` type is special.

All other types are called “primitive” because values can contain a single thing. In contrast, objects are used to store collections of data and more complex entities, thus being called a **reference type**.

The `symbol` type is used to create unique identifiers for objects.

# The typeof operator
```JavaScript title:example.js
typeof undefined; // "undefined"

typeof 0; // "number"

typeof 10n; // "bigint"

typeof true; // "boolean"

typeof "foo"; // "string"

typeof Symbol("id"); // "symbol"

typeof Math; // "object"

typeof null; // "object"

typeof alert; // "function"
```

The `typeof` operator returns the type of the operand. It’s useful when we want to process values of different types differently or just want to do a quick check.

The last three lines needs further explanation:
1. `Math` is a built-in object that provides mathematical operation.
2. The result of `typeof null` is `"object"`. That’s an officially recognized error in `typeof`. `null` is **not** an object.
3. The result of `typeof alert` is `"function"`, because `alert` is a function.