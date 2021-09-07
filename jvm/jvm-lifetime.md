# The Lifetime of a JVM

When a Java application starts, a runtime instance is created. Each Java app runs inside its own JVM.

There are two threads in JVM: 
- *daemon* - thread is used by JVM itself (such as garbage collector);
- *non-daemon* - the initial thread of an application (such as `main()`).

Java app continues to execute as long as any non-daemon threads are still running.

<hr>

[Return](../../../)