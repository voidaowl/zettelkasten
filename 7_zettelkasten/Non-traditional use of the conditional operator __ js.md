# Meta
2025-01-30 23:35
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Non-traditional use of ‘?’
Sometimes, the ternary operator is used as a replacement for `if`:
```JavaScript title:example.js
let company = prompt('Which company created JavaScript?', '');

(company == 'Netscape') ?
	alert('Right!') : alert('Wrong.');
```

This constitutes a **bad practice**, because it’s less readable than a traditional `if...else` block.