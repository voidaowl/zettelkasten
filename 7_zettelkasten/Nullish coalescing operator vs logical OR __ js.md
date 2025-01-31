# Meta
2025-01-31 09:30
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# Comparison with OR ||
The important difference between `??` and `||` is that:
1. `||` returns the first *truthy* value, while
2. `??` returns the first *defined* value.

In other words, `||` doesn’t distinguish between `false`, `0`, `""`, and `null/undefined`.

```JavaScript title:example.js
let height = 0;

alert(height || 100); // 100
alert(heigh ?? 100); // 0
```