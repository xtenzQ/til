# Native Methods

When JVM is run on a host operating system, a Java program interacts with the host by invoking *native methods*.

## Native vs. Java method

||Java method|Native method|
|--|---------|-------------|
|Language|Java|Some other lang (C/C++, ASM, etc)|
|Compiled to|Bytecodes|Native machine code a particular processor|
|Stored in|`.class` files|`.dll` libraries|
|Platform|Independent|Specific|

## How it works
When a running program calls a native method, the JVM loads the `.dll` that contains the native method and invokes it.

## Why we use native methods
- to give direct access to the resources of the host;

## Native method interface
**JNI** or **Java Native Interface** enables native methods to work with any Java Platform implementation.
