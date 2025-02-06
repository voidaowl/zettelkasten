# Meta
2025-02-06 12:36
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# pop/push, shift/unshift
A **queue** is one of the most common uses of an array. In computer science, it is an ordered collection of elements supporting two operations:
- `push` appends an element to the end, and
- `shift` removes the first element, advancing the queue, so that the 2nd element becomes the first.
- FIFO (First-In-First-Out)

A **stack** is another common data structure, which supports two operations:
- `push` adds an element to the end,
- `pop` takes an element from the end (‘top’).
- LIFO (Last-In-First-Out)

## Methods that work with the end of the array
`pop`
Extracts and returns last element:
```JavaScript title:example.js
let fruist = ['Apple', 'Orange', 'Pear'];

alert( fruits.pop() ); // Pear

alert( fruits ); // Apple, Orange
```

Both `pop` and `at(-1)` return the last element of the array, but `pop` modifies (mutates) the array by removing it.

`push`
Append the element to the end of the array:
```JavaScript title:example.js
let fruits = ['Apple', 'Orange'];

fruits.push('Pear');

alert( fruits ); // Apple, Orange, Pear
```

The call `fruits.push(...)` is equal to `fruits[fruits.length] = ...`.

## Methods that work with the beginning of the array
`shift`
Extracts and returns the first element:
```JavaScript title:example.js
let fruits = ['Apple', 'Orange', 'Pear'];

alert( fruits.shift() ); // Apple

alert( fruits ); // Orange, Pear
```

`unshift`
Add the element to the beginning of the array:
```JavaScript title:example.js
let fruits = ['Orange', 'Pear'];

fruits.unshift('Apple');

alert( fruits ); // Apple, Orange, Pear
```

`push` and `unshift` can add multiple elements at once.

# 📑 → Further reading
[Array.prototype.pop() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)
[Array.prototype.push() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)
[Array.prototype.shift() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift)
[Array.prototype.unshift() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift)