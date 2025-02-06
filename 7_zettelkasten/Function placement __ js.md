# Meta
2025-02-01 11:53
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Function Placement
If you’re writing several “helper” functions and the code that uses theme, there are three ways to organize the functions.

1. Declare the functions *above* the code that uses them:
```JavaScript title:example.js
// function declarations
function createElement() {
	...
}

function setHandler(elem) {
	...
}

function walkAround() {
	...
}

// the code which uses them
let elem = createElement();
setHandler(elem);
walkAround();
```

2. Code first, then functions:
```JavaScript title:example.js
// the code which uses the functions
let elem = createElement();
setHandler(elem);
walkAround();

// --- helper functions ---
function createElement() {
	...
}

function setHandler(elem) {
	...
}

function walkAround() {
	...
}
```

3. Mixed: a function is declared where it’s first used.

Most of the time, the second variant is preferred. That’s because when reading code, we first want to know *what it does*. Then, maybe we don’t need to read the functions at all, especially if their names are descriptive of what they actually do.