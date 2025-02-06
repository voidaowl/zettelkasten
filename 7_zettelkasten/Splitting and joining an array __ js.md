# Meta
2025-02-06 21:42
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# split
A real life problem: we’re writing a chat app, and the user enters a comma-delimited list of recipients: `John, Pete, Mary`. An array of names would be much more comfortable to work with than a single string. How do we create it?

```JavaScript title:example.js
let names = "Bilbo, Gandalf, Nazgul";

let arr = names.split(', ');

for (let name of arr) {
	alert( `A message to ${name}.` ); // A message to Bilbo (and other names)
}
```

The `split` method has an optional second numeric argument – a limit on the array length. If provided, the extra elements are ignored. Rarely used in practice.
```JavaScript title:example.js
let arr = 'Bilbo, Gndalf, Nazgul'.split(',', 2);

alert( arr ); // Bilbo, Gandalf
```

The call to `split` with an empty `separator` would split the string into letters:
```JavaScript title:example.js
let str = "test";

alert( str.split('') ); // t,e,s,t
```

# join
The call `arr.join(glue)` does the reverse of `split`. It creates a string of `arr` items joined by `glue` between them.
```JavaScript title:example.js
let arr = ['Bilbo', 'Gandalf', 'Nazgul'];

let str = arr.join(';');

alert( str ); // Bilbo;Gandalf;Nazgul
```

# 📑Further reading
[String.prototype.split() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)
[Arr.prototype.join() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)