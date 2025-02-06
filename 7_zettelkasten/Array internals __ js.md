# Meta
2025-02-06 12:54
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Internals
Array is an object, and thus behaves like an object.

It is copied by reference:
```JavaScript title:example.js
let fruits = ['Banana'];

let arr = fruits;

alert( arr === fruits ); // true

arr.push('Pear');

alert( fruits ); // Banana, Pear
```

The engine tries to store an array’s elements in the contiguous memory area, one after another, and other optimizations that make arrays work fast.

If we quit working with arrays as with an “ordered collection”, these optimizations break.

Technically, we can do this:
```JavaScript title:example.js
let fruits = [];

fruits[99999] = 5;

fruits.age = 25;
```

Array-specific optimizations are not suited for such cases and will be turned off, their benefits disappear.

How to misuse an array?
1. Add a non-numeric property like `arr.test = 5`,
2. Make holes, like: add `arr[0]` and then `arr[1000]` (and nothing between),
3. Fill the array in reverse order, like `arr[1000]`, `arr[999]`, etc.
