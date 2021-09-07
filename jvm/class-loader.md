# Class Loader

## Types of Class Loaders
- primodal class loader:
  - can be only one;
  - is intrinsic;
  - is part of JVM;
  - implemented in the same language as JVM (if JVM is C then primodal CL is also in C);
  - loads only trusted classes (of the Java API).
- class loader objects:
  - can be many class loaders; 
  - loads classes in custom ways (e.g. downloads class files via network);
  - is optional;
  - isn't a part of JVM;
  - stored in the heap.