# Meta
2025-02-05 21:30
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Other math functions

`Math.random()` returns a random number from 0 to 1, inclusive:
```JavaScript title:example.js
alert( Math.random() ); // 0.1234567894322
alert( Math.random() ); // 0.5435252343232
alert( Math.random() ); // ... (any random numbers)
```

`Math.max(a, b, c, ...)` and `Math.min(a, b, c, ...)` return the greatest and smallest number from the arbitrary number of arguments.
```JavaScript title:example.js
alert( Math.max(3, 5, -10, 0, 1) ); // 5
alert( Math.min(1, 2) ); // 1
```

`Math.pow(n, power)` returns `n` raised to the given power:
```JavaScript title:example.js
alert( Math.pow(2, 10) ); // 1024
```

# 📑 → Further reading
[Math - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)
