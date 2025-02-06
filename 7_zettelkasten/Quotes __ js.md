# Meta
2025-02-06 08:55
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Quotes
```JavaScript title:example.js
let singe = 'single-quoted';
let double = "double-quoted";
let backticks = `backticks`;
```

Embed expressions with backticks:
```JavaScript title:example.js
function sum(a, b) {
	return a + b;
}

alert(`1 + 2 = ${sum(1, 2)}.`); // 1 + 2 = 3
```

Split strings on multiple lines with backticks:
```JavaScript title:example.js
let guestList = `Guests:
	* John
	* Pete
	* Mary
`;

alert(guestList);
/*
Guests:
* John
* Pete
* Mary
 */
```