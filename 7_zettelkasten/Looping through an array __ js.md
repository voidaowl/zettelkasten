# Meta
2025-02-06 13:04
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Loops
We can cycle array items with a `for` loop over indexes:
```JavaScript title:example.js
let arr = ['Apple', 'Orange', 'Pear'];

for (let i = 0; i < arr.length; i++) {
	alert( arr[i] );
}
```

For arrays, there’s another loop, `for..of`:
```JavaScript title:example.js
let fruits = ['Apple', 'Orange', 'Pear'];

for (let fruit in fruits) {
	alert( fruit );
}
```

The `for..of` loop doesn’t give access to the index, merely the value at said index.

Because arrays are object, we can also use `for..in`:
```JavaScript title:example.js
let arr = ['Apple', 'Orange', 'Pear'];

for (let key in arr) {
	alert( arr[key] ); // Apple, Orange, Pear
}
```

Potential problems:
1. `for..in` iterates over *all properties*, not only the numeric ones.
2. `for..in` is optimized for generic objects, not arrays, and thus is 10-100 times slower.

**Don’t use `for..in` for arrays.**