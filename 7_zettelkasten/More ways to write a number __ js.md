# Meta
2025-02-05 12:18
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# More ways to write a number

For long numbers, say 1 billion:
```JavaScript title:example.js
let billion = 1_000_000_000;
```

The JavaScript engine ignores the underscores.

We can shorten a number by appending the letter `"e"` to it and specifying the zeroes to count:
```JavaScript title:example.js
let billion = 1e9; // 1 billion (1 and 9 zeroes)

alert( 7.3e9 ); // 7.3 billion
```

`"e"` multiplies the number `1` with the given zeroes count.

Now what about very small numbers?
```JavaScript title:example.js
let mcs = 0.000001;
```

`"e"` can help here too:
```JavaScript title:example.js
let mcs = 1e-6; // five zeroes to the left from 1
```