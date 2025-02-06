# Meta
2025-02-04 19:05
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Further conversions

If we pass an object as an argument, then there are two stages of calculations:
1. The object is converted to a primitive (using the rules described above).
2. If necessary for further calculations, the resulting primitive is also converted.

```JavaScript title:example.js
let obj = {
	// toString handles all conversions in the absence of other methods
	toString() {
		return "2";
	}
};

alert(obj * 2); // 4, object converted to string "2", multiplication coerced it into a number
```

Binary plus will concatenate strings in the same situation, as it accepts a string:
```JavaScript title:example.js
let obj = {
	toString() {
		return "2";
	}
};

alert(obj + 2); // "22"
```