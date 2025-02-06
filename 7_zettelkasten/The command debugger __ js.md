# Meta
2025-02-01 09:28
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# The command “debugger”
We can also pause the code by using the `debugger` command in it:
```JavaScript title:example.js
function hellow(name) {
	let phrase = `Hello, ${name}!`;

	debugger; // <-- the debugger stops here

	say(phrase);
}
```

Such commands work only when the developer tools are open, otherwise the browser ignores it.