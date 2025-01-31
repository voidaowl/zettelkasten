# Meta
2025-01-30 00:00
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# alert
```JavaScript title:example.js
alert("Hello!")
```

# prompt
```JavaScript title:example.js
result = promtp(title, [default]);

// Example
let age = prompt("How old are you?", 100)

alert(`You are ${age} years old!`)
```

`title` is the text to show the user. `default` is an optional parameter, the initial value for the input field. The square brackets denote the parameter as optional.

# confirm
```JavaScript title:example.js
result = confirm(question)
```

The function `confirm` shows a modal windows with a question and two buttons: `OK` and `Cancel`. The result is `true` if OK is pressed. Otherwise, it is false.