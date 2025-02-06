# Meta
2025-02-06 13:31
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Don’t compare arrays with ==
The loose equality operator `==` has no special treatment for arrays. It works the same as with objects.

The rules:
1. Two objects are equal `==` only if they’re references to the same object.
2. If one of the arguments of `==` is an object, and the other a primitive, the object is converted to primitive.
3. …with an exception of `null` and `undefined`, that equal `==` each other and nothing else.

The strict comparison `===` is even simpler, as it doesn’t convert types.

If we compare arrays with `==`, they are never the same, unless we compare two variables that reference exactly the same array.

```JavaScript title:example.js
alert( [] == [] ); // false
alert( [0] == [0] ); // false
```

Comparison with primitives give seemingly strange results as well:
```JavaScript title:example.js
alert( 0 == [] ); // true, 0 == ''
alert( '0' == [] ); // false, '0' != ''
```

How to compare arrays? Compare them item-by-item in a loop or using other iteration methods.