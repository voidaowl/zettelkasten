# Meta
2025-01-30 21:38
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed

# 📷 → What does it look like?
```JavaScript title:example.js
alert( 'Z' > 'A' ); // true
alert( 'Glow' > 'Glee' ); // true
alert( 'Bee' > 'Be' ); // true
```

# 🔍 → What does it do?
Compares two strings.

# ❓ → How it does it.
To see whether a string is greater than another, JavaScript uses **lexicographical** order.

The algorithm is simple:
1. Compare the first character of both strings.
2. If the first character from the first string is greater (or less) than the other string’s, then the first string is greater (or less) than the second. We’re done.
3. Otherwise, if both strings’ first characters are the same, compare the second characters the same way.
4. Repeat until the end of either string.
5. If both strings end and the same length, then they are equal. Otherwise, the longer string is greater.

> [!info] **Not a real dictionary, but Unicode order**
> Case matters. A capital `"A"` is not equal to a lowercase `"a"`, which is greater. Why? Because the lowercase character has a greater index in the internal encoding table JavaScript uses (Unicode).


# 📑 → Further reading / Sources
[Comparing strings - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#comparing_strings)