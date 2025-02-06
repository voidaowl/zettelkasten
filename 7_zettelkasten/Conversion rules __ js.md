# Meta
2025-02-04 18:25
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Conversion rules

1. There’s no conversion to boolean. All objects are `true` in a boolean context.
2. **Numeric conversion** happens when we subtract objects or apply mathematical functions. For instance, `Date` objects can be subtracted, and the result of `date1 - date2` is the time difference between two dates.
3. **String conversion** happens when we output an object with `alert(obj)` and similar contexts.

We can implement string and numeric conversion by ourselves, using special object methods.