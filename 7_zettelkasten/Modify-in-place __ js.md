# Meta
2025-01-30 18:21
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Modify-in-place
We sometimes need to apply an operator to a variable and store the new result in the same variable. For example:
```JavaScript title:example.js
let n = 2;
n = n + 5;
n = n * 2;
```

This notation can be shortened by the operators `+=` and `-=`:
```JavaScript title:example.js
let n = 2;
n += 5; // now n = 7
n *= 2; // now n = 14
```

Short “modify-and-assign” operators exit for all arithmetic and bitwise operators: `/=`, `-=`, etc.

Such operators have the same precedence as a normal assignment, so they run after most other calculations.
```JavaScript title:example.js
let n = 2;

n *= 3 + 5;

alert( n ); // 16
```

# 📑 → Further reading
[Addition assignment (`+=`)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Addition_assignment)
[Bitwise AND assignment (`&=`)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_AND_assignment)
[Bitwise OR assignment (`|=`)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_OR_assignment)
[Bitwise XOR assignment (`^=`)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_XOR_assignment)
[Division assignment (`/=`)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Division_assignment)
[Exponentiation assignment (`**=`)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Division_assignment)
[Remainder assignment (`%=`)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Remainder_assignment)
[Subtraction assignment (`-=`)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Subtraction_assignment)
