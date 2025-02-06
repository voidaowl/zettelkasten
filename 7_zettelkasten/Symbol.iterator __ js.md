# Meta
2025-02-06 23:09
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Symbol.iterator
Let’s make an iterable. We have an object that is not an array, but looks suitable for `for..of`, such as a `range` object representing an interval of numbers:
```JavaScript title:example.js
let range = {
	from: 1,
	to: 5,
};
```

To make `range` iterable we must add a method to the object named `Symbol.iterator`.
1. When `for..of` starts, it calls the method once (or errors if not found). The method must return an **iterator** – an object with the method `next`.
2. Onward, `for..of` works **only wit that returned object**.
3. When `for..of` wants the next value, it calls `next()` on that object.
4. The result of `next()` must have the form `{done: Boolean, value: any}`, where `done=true` means that the loop is finished. Otherwise, `value` is the next value.

```JavaScript title:example.js
let range = {
	from: 1,
	to: 5,
}

// 1. call to for..of initially calls this
range[Symbol.iterator] = function() {

	// ...it returns the iterator object:
	// 2. Onward, for..of works only with the iterato object below, asking it for next values
	return {
		current: this.from,
		last: this.to,

		// 3. next() is called on each iteration by the for..of loop
		next() {
			// 4. it should return the value as an object {done:.., value:..}
			if (this.current <= this.last) {
				return { done: false, value: this.current++ };
			} else {
				return { done: true };
			}
		}
	}
};

// now it works!
for (let num of range) {
	alert(num); // 1, then 2, 3, 4, 5
}
```

The core feature of iterables is **separation of concerns**.
- The `range` itself doesn’t have `next()` method.
- Instead, another object, a so-called “iterator” is created by the call to `range[Symbol.iterator]()`, and its `next()` generates values for the iteration.

So, the iterator object is separate from the object it iterates over.

We can simplify:
```JavaScript title:example.js
let range = {
	from: 1,
	to: 5,

	[Symbol.iterator]() {
		this.current = this.from;
		return this;
	},

	next() {
		if (this.current <= this.to) {
			return { done: false, value: this.current++ };
		} else {
			return { done: true };
		}
	}
};

for (let num of range) {
	alert(num); // 1, then 2, 3, 4, 5
}
```

Now `range[Symbol.iterator]()` returns the `range` object itself: it has the necessary `next()` method and remembers the current iteration progress in `this.current`.

The downside is that now it’s impossible to have two `for..of` loops running over the object simultaneously: they’ll share the iteration state, because there’s only one iterator – the object itself. Two parallel `for..of`s is a rare thing, even in async scenarios.

# 📑Further reading
[Symbol.iterator - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/iterator)
[Array.prototype[Symbol.iterator]() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Symbol.iterator)
