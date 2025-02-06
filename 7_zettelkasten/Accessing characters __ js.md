# Meta
2025-02-06 09:06
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Accessing characters

To get a character at position `pos`, use square brackets `[]`, or call the method `String.prototype.at()`.

```JavaScript title:example.js
let str = `Hello`;

// first character
alert( str[0] ); // H
alert( str.at(0) ); // H

// last character
alert( str[str.length - 1] ); // o
alert( str.at(-1) ); // o
```

The `.at(pos)` method allows negative position.

We can iterate over characters using `for..of`:
```JavaScript title:example.js
for (let char of "Hello") {
	alert(char); // H,e,l,l,o
}
```

# 📑 → Further reading
[String.prototype.at() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/at)
