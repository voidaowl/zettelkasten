# Meta
2025-02-06 23:31
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Iterables and array-likes
Two official terms look similar, but are very different:
1. **Iterables** are objects that implement the `Symbol.iterato` method.
2. **Array-likes** are objects that have indexes and `length`, so they look like arrays.

Strings are both iterable and array-like.

Both iterables and array-likes are usually **not arrays**, as they don’t have `push`, `pop`, etc.