# Meta
2025-01-31 13:03
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# Outer variables
A function can access an outer variable as well, for example:
```JavaScript title:example.js
let userName = 'Jon';

function showMessage() {
	let message = 'Hello ' + userName;
	alert(message);
}

showMessage(); // Hello, Jon
```

The function has full access to the outer variable. It can modify it as well.
```JavaScript title:example.js
let userName = 'Jon';

function showMessage() {
	userName = 'Bob';
}

alert(userName); // Jon

showMessage();

alert(userName); // Bob
```

The outer variable is only used if there’s no local one.

If a same-named variable is declared inside a function the it *shadows* the outer one.
```JavaScript title:example.js
let userName = 'Jon';

function showMessage() {
	let userName = 'Bob';
}

showMessage();

alert( userName ); // Jon
```

>[!info] **Global variables**
> Variables declared outside of any function, such as the outer `userName` in the code above, are called *global*.
>
> Global variables are visible from any function (unless shadow by *local* functions).
>
> It’s a good practice to minimize the use of global variables. Modern code has few or no globals. Sometimes they can be useful to store project-level data.
>

# 📑 → Further reading
[Global variable - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Global_variable)
