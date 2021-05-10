### Python Internals :)

#### We're given the flag1 as a global variable as seen in the `exec()` call.

* To get the flag, we simply use the `getattr` function. However it prints `REDACTED`.
* Digging deeper, the type that holds the flag is a child class of builtin `str` class.
* This means we can simply get the copy of the flag using the slice implementation of `str`

Image goes here