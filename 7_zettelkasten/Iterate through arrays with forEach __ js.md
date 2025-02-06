# Meta
2025-02-06 19:25
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Iterate: forEach
Syntax: `arr.forEach(function(item, index, array) { // do ... })`.
The method allows to run a function for each element of an array.

```JavaScript title:example.js
['Bilbo', 'Gandalf', 'Nazgul'].forEach(alert);
```

This code is more elaborate about their positions on the target array:
```JavaScript title:example.js
['Bilbo', 'Gandalf', 'Nazgul'].forEach((item, index, array) {
	alert(`${item} is at index ${index} in ${array}.`);
});
```

# 📑Further reading
[Array.prototype.forEach() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
