# Meta
2025-02-06 13:12
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# A word about “length”
The `length` property automatically updates when we modify the array. To be precise, it’s not actually the count of values in the array, but the greatest numeric index plus one.

```JavaScript title:example.js
let fruits = [];
fruits[123] = 'Apple';

alert( fruits.length ); // 124
```

Another interesting thing is that `length` is writable. If we increase it manually, nothing interesting happens. If we decrease it, the array is truncated. The process is irreversible.

```JavaScript title:example.js
let arr = [1, 2, 3, 4, 5];

arr.length = 2;
alert( arr ) = [1, 2]

arr.length = 5;
alert( arr[3] ); // undefined
```

The simplest way to clear an array is: `arr.length = 0`.