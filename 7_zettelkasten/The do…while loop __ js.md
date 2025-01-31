# Meta
2025-01-31 09:47
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed

# 📷 → What does it look like?
```JavaScript title:example.js
do {
	// loop body
} while (condition);
```

# 🔍 → What does it do?
The loop first executes the body, then checks the condition and, while it’s truthy, executes it again and again.

# ❓ → How it does it.
```JavaScript title:example.js
let i = 0;
do {
	alert(i);
	i++;
} while (i < 3);
```

# ✅ → Best practice
This form of syntax should only be used when you want the body of the loop to execute **at least once** regardless of the condition being truthy. Usually, the `while(...) {...}` form is preferred.

# 📑 → Further reading / Sources
[do … while - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/do...while)