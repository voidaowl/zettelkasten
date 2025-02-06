# Meta
2025-02-04 12:14
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed  

# Short-circuiting

`?.` immediately stops the evaluation if the left part doesn’t exist.

```JavaScript title:example.js
let user = null;
let x = 0;

user?.sayHi(x++); // no "user"

alert(x); // 0
```