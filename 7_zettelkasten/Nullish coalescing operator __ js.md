# Meta
2025-01-31 09:20
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Nullish coalescing operator ‘??’

`??` returns the first argument if it’s not `null/undefined`. Otherwise, the second one.

The common use case for `??` is to provide a default value.
```JavaScript title:example.js
let user;
alert(user ?? "Anonymous"); // Anonymous
```

Here’s the example with `user` assigned to a name:
```JavaScript title:example.js
let user = 'John';

alert(user ?? 'Anonymous'); // John
```

We can also use a sequence of `??` to select the first value from a list that isn’t `null/undefined`.
```JavaScript title:example.js
let firstName = null;
let lastName = null;
let nickName = "Supercoder";

// shows the first defined value:
alert(firstName ?? lastName ?? nickName ?? "Anonymous"); // Supercoder
```