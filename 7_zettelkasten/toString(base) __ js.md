# Meta
2025-02-05 12:35
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# toString(base)

The method `num.toString(base)` returns a string representation of `num` in the numeral system with the given `base`.

```JavaScript title:example.js
let num = 255;

alert( num.toString(16) ); // ff
alert( num.toString(2) ); // 11111111
```

The `base` can vary:
- `16` is used for hex colors, character encodings, etc., digits can be `0...9` or `A...F`.
- `2` is for debugging bitwise operations, digits can be `0` or `1`.
- `36` is the maximum, digits can be `0...9` or `A...Z`.

A useful case for `36` is when we need to turn a long numeric identifier into something shorter, for example to make a short URL. We can simply represent it in the numeral system with base `36`:
```JavaScript title:example.js
alert( 123456..toString(36) ); // 2n9c
```

> [!warning] **Two dots to call a method**
> Please note that two dots in `123456..toString(36)` is not a typo. If we want to call a method directly or a number, like `toString` in the example above, then we need to place two dots after it.
> 
> If we placed a single dot, then there would be an error, because JavaScript syntax implies the decimal part after the first dot. And if we place one more dot, then JavaScript knows that the decimal part is empty and now goes the method.
> 
> Also could write `(123456).toString(36)`.

# 📑 → Further reading
[Number.prototype.toString() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toString)
