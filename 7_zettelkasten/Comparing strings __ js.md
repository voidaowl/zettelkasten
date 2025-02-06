# Meta
2025-02-06 12:14
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Comparing strings
Strings are compared “lexicographically”, character by character.

A lowercase latter is always greater than the uppercase.

Letters with diacritical marks are “out of order”.
```JavaScript title:example.js
alert( 'Österreich' > 'Zealand' ); // true
```

Each character has a corresponding numeric code. There are two methods to find it.

`str.codePointAt(pos)`
Returns a decimal number representing the code for the character at position `pos`:
```JavaScript title:example.js
alert( 'Z'.codePointAt(0) ); // 90
alert( 'z'.codePointAt(0) ); // 122
alert( 'z'.codePointAt(0).toString(16) ); // 7a (hex)
```

`String.fromCodePoint(code)`
Creates a character by its numeric `code`:
```JavaScript title:example.js
alert( String.fromCodePoint(90) ); // Z
alert( String.fromCodePoint(0x5a) ); // Z (hex as arg)
```

A more complex example:
```JavaScript title:example.js
let str = '';

for (let i = 65; i <= 220; i++) {
	str += String.fromCodePoint(i);
}

alert( str );
/* 
 * OUTPUT:
 * ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~
 * ¡¢£¤¥¦§¨©ª«¬­®¯°±²³´µ¶·¸¹º»¼½¾¿ÀÁÂÃÄÅÆÇÈÉÊËÌÍÎÏÐÑÒÓÔÕÖ×ØÙÚÛÜ
 */
```

## Correct comparisons
Modern browsers support the internationalization standard [ECMA-402](https://ecma-international.org/publications-and-standards/standards/ecma-402/).

The call `str.localeCompare(str2)` returns an integer indicating whether `str` is less, equal or greater than `str2` according to the language rules:
- Returns a **negative** number if `str` is **less** than `str2`,
- Returns a **positive** number if `str` is **greater** than `str2`,
- Returns `0` if they are **equivalent**.

# 📑 → Further reading
[String.prototype.codePointAt() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/codePointAt)
[String.fromCodePoint() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCodePoint)
[String.prototype.localeCompare() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/localeCompare)
