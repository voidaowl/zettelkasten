# Meta
2025-02-01 11:54
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Bad comments
Novice mistake → explaining “what is going on in the code”:
```JavaScript title:example.js
// This code will do this thing (...) and that thing (...)
// ...and something else ...
very;
complex;
code;
```

In good code, the amount of “explanatory” comments should be minimal. The code should be easy to understand without them.

**Rule:** If the code is so unclear that it requires a comment, then maybe it should be rewritten instead.

## Recipe: factor our functions
Sometimes it’s beneficial to replace a code piece with a function, like here:
```JavaScript title:example.js
function showPrimes(n) {
	nextPrime:
	for (let i = 2; i < n; i++) {

		// check if i is a prime number
		for (let j = 2; j < i; j++) {
			if (i % j == 0) continue nestPrime;
		}

		alert(i);
	}
}
```

The better variant, with a factored-out function `isPrime`:
```JavaScript title:example.js
function showPrimes(n) {
	for (let i = 2; i < n; i++) {
		if (!isPrime(i)) continue;
		
		alert(i);
	}
}

function isPrime(n) {
	for (let i = 2; i < n; i++) {
		if (n % i == 0) return false;
	}
}
```

## Recipe: create functions
If we have a long “code sheet” like this:
```JavaScript title:example.js
// here we add whiskey
for (let i = 0; i < 10; i++) {
	let drop = getWhiskey();
	smell(drop);
	add(drop, glass);
}

// here we add juice
for (let t = 0; t < 3; t++) {
	let tomato = getTomato();
	examine(tomato);
	let juice = press(tomato);
	add(juice, glass);
}

// ...
```

…then it might be a better variant to refactor it into functions:
```JavaScript title:example.js
addWhiskey(glass);
addJuice(glass);

function addWhiskey(container) {
	for(let i = 0; i < 10; i++) {
		let drop = getWhiskey();
		// ...
	}
}

function addJuice(container) {
	for(let t = 0; t < 3; t++) {
		let tomato = getTomato();
		// ...
	}
}
```

Functions themselves tell what’s going on. There’s nothing to comment.

Code structure is better when split. It’s clear what every function does, what it takes and what it returns.

In reality, we can’t totally avoid “explanatory” comments. There are complex algorithms, and there are smart “tweaks” for purposes of optimization. But generally we should try to keep the code simple and self-descriptive.
