# Data Types

are defined by the JVM specification.
- Primitive types
  - `float`/`double`/`byte`/`short`/`int`/`long`/`char`/*returnValue*
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

The basic unit of size for data values is the `word` - a fiexd size chosen by the designer of each JVM implemetation:
- it should be large enough to hold a value of type `byte`, `short`, `int`, `char`, `float`, `returnValue`, or `reference`;
- two `word`s must be large enough to hold a value of type `long` or `double`;
- `word` should be at least 32 bits.

<hr>

[Return](../../../)