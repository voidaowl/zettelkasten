# Meta
2025-02-06 13:00
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Performance
Methods `push/pop` run fast, while `shift/unshift` are slow. Why?

The `shift` operation must do 3 things:
1. Remove the element with the index `0`,
2. Move all elements to the left, renumber them from the index `1` to `0`, from `2` to `1`, etc.,
3. Update the `length` property.

The more elements in the array, the more time to move them, more in-memory operations.

Similar things happen to `unshift`: to add an element to the beginning of the array, we must first move existing elements to the right, increasing their indexes.

Meanwhile, the `pop` operation removes one element from the end. It doesn’t need to move anything, because other elements keep their indexes.

`push` works similarly.