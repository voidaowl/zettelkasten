# Meta
2025-02-06 10:05
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Searching for a substring

There are multiple ways to look for a substring within a string.

## str.indexOf

Syntax: `str.indexOf(substr, pos)`.

It looks for the `substr` in `str` starting from given position `pos.`.

```JavaScript title:example.js
let str = 'Widget with id';

alert( str.indexOf('Widget') ); // 0
alert( str.indexOf('widget') ); // -1, not found

alert( str.indexOf('id') ); // 1
```

Let’s also use the positional parameter:
```JavaScript title:example.js
let str = 'Widget with id';

alert( str.indexOf('id', 2) ); // 12
```

For all occurrences, use a loop:
```JavaScript title:example.js
let str = 'As sly as a fox, as strong as an ox';

let target = 'as';

let pos = 0;
while(true) {
	let foundPos = str.indexOf(target, pos);
	if (foundPose == -1) break;

	alert( `Found at ${foundPos}` );
	pos = foundPos + 1;
}

/* OUTPUT:
* 7
* 17
* 27
 */
```

The same algorithm can be shortened:
```JavaScript title:example.js
let str = 'As sly as a fox, as strong as an ox';
let target = 'as';

let pos = -1;
while((pos = str.indexOf(target, pos + 1)) != -1) {
	alert( pos );
}
```

> [!info] **The reverse**
> There is a similar method `str.lastIndexOf(substr, position)` that searches from the end of a string to its beginnings. Lists the occurrences in the reverse order.

Conflict with `if`. This is not possible:
```JavaScript title:example.js
let str = 'Widget with id';

if (str.indexOf('Widget')) {
	alert('We found it'); // doesn't work!
}
```

The `alert` above doesn’t show because `str.IndexOf('Widget')` returns `0` (it did find the matching position), which `if` considers `false`.

We should check for `-1`:
```JavaScript title:example.js
let str = 'Widget with id';

if (str.indexOf('Widget') != -1) {
	alert('We found it'); // works
}
```

## includes, startsWith, endsWith

`str.includes(substr,pos)` returns `true/false` if `str` contains `substr`. Good when testing for the match, but don’t need the position.
```JavaScript title:example.js
alert( 'Widget with id'.includes('Widget') ); // true

alert( 'Hello'.includes('Bye') ); // false

alert( 'Widget'.includes('id') ); // true
alert( 'Widget'.includes('id', 3) ); // false
```

The methods `str.startsWith` and `str.endsWith` do exactly what they say:
```JavaScript title:example.js
alert( 'Widget'.startsWith('Wid') ); // true
alert( 'Widget'.endsWith('get') ); // true
```

# 📑 → Further reading
[String.prototype.indexOf() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf)
[String.prototype.lastIndexOf() - JavaScript | MND](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/lastIndexOf)
[String.prototype.includes() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes)
[String.prototype.startsSiwth() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/startsWith)
[String.prototype.endsWith() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/endsWith)
