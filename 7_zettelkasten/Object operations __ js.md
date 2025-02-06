# Meta
2025-02-04 18:23
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Operations with objects

JavaScript doesn’t allow you to customize how operators work with objects. We can’t implement a special object method to handle addition (or other operators).

In case of such operations, objects are auto-converted to primitives, and then the operation is carried out over these primitives and results in a primitive value.

The result of `obj1 + obj2` can’t be another object!