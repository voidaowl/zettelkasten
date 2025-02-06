# Meta
2025-02-06 10:00
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Strings are immutable

Strings can’t be changed in JavaScript. It’s impossible to change a character.
```JavaScript title:example.js
let str = 'Hi';

srt[0] = 'h'; // error
alert( str[0] ); // doesn't work
```

Workaround:
```JavaScript title:example.js
let str = 'Hi';

str = 'h' + str[1];

alert( str ); // hi
```