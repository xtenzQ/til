# Class Loader

**Main functions:**
- finds and loads types;
- verifies the correctness of imported classes;
- allocates and initialize memory for class variables;
- assists in the resolution of symbolic references.

The order of operations:
1. Finds and imports the binary data for a type;
2. Performs verification, preparation and resolution:
   1. Verification: ensures the correctness of the imported type;
   2. Preparation: allocates memory for class variables and initialize the memory to default values;
   3. Resoultion: transformes symbolic references from the type into direct references.
3. Initialization: invokes Java code that initializes class variables to their peroper starting values.

## Types of Class Loaders
- **primodal class loader** (also called **bootstrap**):
  - single;
  - is intrinsic;
  - is a part of JVM;
  - implemented in the same language as JVM (if JVM is C then primodal CL is also in C);
  - loads only trusted classes (of the Java API).
- **class loader objects**:
  - multiple; 
  - loads classes in custom ways (e.g. downloads class files via network);
  - is optional;
  - is a part of running Java app;
  - stored in the heap.

## Contribution to [JVM Sandbox](jvm-sandbox.md)
- guards the borders of the trusted class libs;
- prevents malicious code from interfering with trusted code by providing *protected namespaces* for classed loaded by different class loaders.

## Class Loader Objects

In `ClassLoader` class there are three gateaways into JVM: `defineClass()`, `findSystemClass()`, `resolveClass()`.

### `defineClass()`

```Java
protected final Class<?> defineClass(
  String name, byte[] b, int off, int len) throws ClassFormatError
```
This method is responsible for the conversion of an array of bytes into an instance of a class. And before we use the class, we need to resolve it.

In case data didn't contain a valid class, it throws a `ClassFormatError`.

### `findSystemClass()`

```Java
protected final Class<?> findSystemClass(String name) throws ClassNotFoundException
```
Finds a class with the specified binary name, loading it if necessary.
This method loads the class through the system class loader (see `getSystemClassLoader()`). The Class object returned might have more than one `ClassLoader` associated with it. Subclasses of `ClassLoader` need not usually invoke this method, because most class loaders need to override just `findClass(String)`.

### `resolveClass()`

```Java
protected final void resolveClass(Class<?> c)
```
Links the specified class. This (misleadingly named) method may be used by a class loader to link a class. If the class c has already been linked, then this method simply returns.

<hr>

[Return](../../../)