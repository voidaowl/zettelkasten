# Meta
2025-02-01 12:04
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Good comments
So, if explanatory comments are usually bad, which comments are good?

## Describe the architecture
Provide a high-level overview of components, how they interact, what’s the control flow in various situations… In short – the bird’s eye view of the code.

## Document function parameters and usage

JDoc is useful:
```JavaScript title:example.js
/**
 * Returns x raised to the n-th power.
 * 
 * @param {number} x The number to raise.
 * @param {number} n The power, must be a natural number.
 * @param {number} x raised to the n-th power.
 */
function pow(x, n) {
	// ...
}
```

Such comments allow us to understand the purpose of the function and use it the right way without looking in its code.

## Why is the task solved this way?
What’s written is important, but what’s *not* written may be even more so. Why is the task solved this way? The code gives no answer.

If there are many ways to solve a task, why this one? Especially when it’s not the most obvious one.

Without such comments, the following situation is possible:
1. You (or your colleagues) open the code written some time ago, and see that it’s “suboptimal”.
2. You think: “I’m better now”, so you rewrite using the “more obvious and correct” variant.
3. … The urge to rewrite was good, but in the process you see that the “more obvious” solution is actually lacking. You even dimly remember why, because you already tried it long ago. You revert to the correct variant, but the time was wasted.

## Any subtle features of the code? Where are they used?
If the code has anything subtle and counter-intuitive, it’s definitely worth commenting.
