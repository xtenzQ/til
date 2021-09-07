# JVM
When we talk about JVM, it could be:
- an abstract specification;
- a concrete implemetation;
- a runtime instance;

JVM specification is flexible and defines certain features every JVM must have such as ability to execute Java bytecodes.

JVM can have different implementations:
  - completely in software;
  - to varying degrees in hardware. 

## Main job is

- to load `.class` files;
- to execute the bytecodes from `.class` files.

## Consists of
**a class loader**:
- loads `.class` files from the program and Java API (only those that are needed to run a program).

The bytecodes are executed in *execution engine*: 
- the simplest kind of execution engine of JVM implemented in software is an **interpreter that interprets the bytecodes one at a time**;
- another execution engine is **JIT** (*just-in-time compiler*) which is faster but requires more memory:
  - the bytecodes of a method are compiled to a native machine code the first time the method is invloked and the code is cached for re-use. 

<hr>

[Return](../../../)