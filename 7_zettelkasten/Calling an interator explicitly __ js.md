# Meta
2025-02-06 23:27
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Calling an iterator explicitly
This code creates a string iterator and gets values from it “manually”:
```JavaScript title:example.js
let str = "Hello";

let iterator = str[Symbol.iterator]();

while (true) {
	let result = iterator.next();
	if (result.done) break;
	alert(result.value); // outpus chars one by one
}
```

Rarely needed, but gives more control over the process than `for..of`. For instance, we can split the iteration process: iterate a bit, stop, do something else, and resume.

# 📑Further reading
[String.prototype[Symbol.iterator]() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/iterator)
