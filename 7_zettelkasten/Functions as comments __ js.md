# Meta
2025-01-31 14:49
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Functions == Comments
Functions should be short and do exactly one thing. If that intended thing is big, maybe it’s worth it to split the function into a few smaller ones.

A separate function isn’t only easier to test and debug – its very existence is a great comment!

For instance, compare two functions `showPrimes(n)` below. Each outputs prime numbers up to `n`.

The first variant uses a label:
```JavaScript title:example.js
function showPrimes(n) {
	nextPrime: for let (i = 2; i < n; i++) {
		for (let j = 2; j < i; j++) {
			if(i % j == 0) continue nextPrime;
		}

		alert( i );
	}
}
```

The second variant uses an additional function `isPrime(n)` to test for primarily:
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
	return true;
}
```

The second variant is easier to understand. Sometimes people refer (and prefer) to such code as *self-describing*.