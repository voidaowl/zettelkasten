# Meta
2025-01-31 18:25
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Callback functions
```JavaScript title:example.js
function ask(question, yes, no) {
	if (confirm(question)) yes();
	else no();
}

function showOk() {
	alert( "You agreed." );
}

function showCancel() {
	alert( "You canceled the execution." )
}

ask("Do you agree?", showOk, showCancel); 
```

**The arguments `showOk` and `showCancel` of `ask` are called *callback functions* or just *callbacks***.

The idea is that we pass a function and expect it to be “called back” later if necessary. In our case, `showOk` becomes callback for “yes” answer, and `showCancel` for “no” answer.

We can use Function Expressions to write an equivalent, shorter function:
```JavaScript title:example.js
function ask(question, yes, no) {
	if (confirm(question)) yes()
	else no();
}

ask {
	"Do you agree?",
	function() { alert('You agreed.'); },
	function() { alert('You canceled the execution.'); }
}
```

> [!info] **A function is a value representing an “action”**
> Regular values like strings or numbers represent the *data*.
> A function can be perceived as an *action*.
> We can pass it between variables and run when we want.

# 📑 → Further reading
[Callback function - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function)
