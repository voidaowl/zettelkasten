# Meta
2025-01-31 11:48
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# break
Normally, a loop exits when its condition becomes falsy.

But we can force the exit with the special `break` directive.
```JavaScript title:example.js
let sum = 0;

while (true) {
	let value = +prompt("Enter a number", '');

	if (!value) break;

	sum += value;

}

alert( 'Sum: ' + sum);
```

# ✅ → Best practice
The combination “infinite loop + `break` as needed” is great for situations when a loop’s condition must be checked not in the beginning or end of the loop, but in the middle or several places of its body.

# 📑 → Further reading
[break - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/break)
