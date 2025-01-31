# Meta
2025-01-30 23:31
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# Multiple ‘?’
A sequence of ternary operators can return a value that depends on more than one condition. For example:
```JavaScript title:example.js
let age = prompt('age?', 18);

let message = (age < 3) ? 'Hi, baby!' :
	(age < 18) ? 'Hello!' :
	(age < 100) ? 'Greetings!' :
	'What an unusual age!';

alert(message);
```

Breakdown:
1. The first question mark checks whether `age < 3`.
2. If true – it returns `'Hi, baby!'` Otherwise, it continues to the expression after the colon `:`, checking `age < 18`.
3. If that’s true, it returns `'Hello!'`. Otherwise, it continues to the next colon `:`, checking `age < 100`.
4. If that’s true, it returns `'Greetings!'`. Otherwise, it continues to the expression after the last colon, returning `'What an unusual age!`
