# Data Types

are defined by the JVM specification.
- Primitive types
  - float/double/byte/short/int/long/char/*returnValue*
- Reference types
  - class types
  - interface types
  - array types

`boolean` is a special type. During compilation it could be translated into **bytes** or **ints**.

e.g.:
- `false` is represented by `0` (`int`);
- `true` is represented by any non-zero int;
- operations involving `boolean` values use `int`s;
- array of `boolean` are accessed as arrays of `byte`.

`returnValue` type is used to implement `finally` clauses.

<hr>

[Return](../../../)