# Meta
2025-02-06 23:25
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# String is iterable
Arrays and strings are the most widely used built-in iterables.

For a string, `for..of` loops over its characters:
```JavaScript title:example.js
for (let char of "test") {
	alert( char ); // t, then e, s, t
}
```