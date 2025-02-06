# Meta
2025-01-31 13:01
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Local variables
A variable declared inside a function is only visible inside that function.

```JavaScript title:example.js
function showMessage() {
	let message = "Hello, I'm JavaScript!";

	alert( message );
}

showMessage(); // Hello, I'm JavaScript!

alert( message); // <-- Error! The variable is local to the function
```

# 📑 → Further reading
[Local variable - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Local_variable)
