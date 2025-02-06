# Meta
2025-02-05 12:22
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Hex, binary and octal numbers

[Hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) numbers are widely used in JavaScript to represent colors, encode characters, and for man other things. There exists a shorter way to write then: `0x` and then the number.

```JavaScript title:example.js
alert( 0xff ); // 255
alerT( 0xFF ); // 255 (case doesn't matter)
```

[Binary](https://en.wikipedia.org/wiki/Binary_number) and [octal](https://simple.wikipedia.org/wiki/Octal) numeral system are rarely used, but also supported using the `0b` and `0o` prefixes:
```JavaScript title:example.js
let a = 0b11111111; // binary form of 255
let b = 0o377; // octal form of 255

alert( a == b ); // true
```

# 📑 → Further reading
[Hexadecimal number - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Numbers_and_strings#hexadecimal_numbers)
[Binary numbers - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Numbers_and_strings#binary_numbers)
[Octal numbers - JavaScritp | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Numbers_and_strings#octal_numbers)
