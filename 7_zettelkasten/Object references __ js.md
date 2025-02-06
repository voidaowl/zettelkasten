# Meta
2025-02-03 11:39
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Object references and copying

Objects are stored and copied “by reference”.

A variable assigned to an object stores not the object itself, but its “address in memory” – a “reference” to it.

When an object variable is copied, the reference is copied, but the object itself is not duplicated.

```JavaScript title:example.js
let user = { name: "John" };

let admin = user;

admin.name = 'Pete';

alert(user.name); // 'Pete'
```
