# Meta
2025-01-31 14:42
**Tags:** [[JavaScript Learning]]
**Activity:** #learning 
**Status:** #completed 

# Naming conventions
Functions are actions. So their name is usually a *verb*. It should be brief, accurate, descriptive.

It’s a widespread practice to start a function with a verbal prefix which vaguely describes the action. For example:
- `'get...'` – return a value,
- `'calc...'` – calculate something,
- `'create...'` – create something,
- `'check...'` – check something.

Use camelCase.

# ✅ → Best practices
> [!info] **One function – one action**
> A function should do exactly what it suggests by its name, and no more.
> 
> Two independent actions usually deserve two functions, even if they are usually called together (in that case, make a 3rd function that calls the other two).

A few examples of breaking this rule:
- `getAge` – would be bad if it shows an `alert` with the age (should only get).
- `createForm` – would be bad if it modifies the document, adding a form to it (should only create and return).
- `checkPermissions` – would be bad if it displays the `access granted/denied` message (should only perform the check and return the result).

> [!info] **Ultrashort function names**
> Functions that are used *very often* usually have ultrashort names.
> These are exceptions. Generally, function names should be concise and descriptive.

# 📑 → Further reading
[Function: name - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/name)
