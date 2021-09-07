# JVM Architecture

In JVM specification, VM instance behavior is described in terms of:
- subsystems;
- memory areas;
- data types;
- instructions.

These components describe an abstract inner architecture for the JVM. The main idea is not to dictate an inner architecture for implementations, but to provide a way to strictly define the external behavior of implementations.

JVM consists of:
- a **class loader subsystem**: a mechanism for loading types (classes and interfaces);
- an **execution engine**: a mechanism of executing the instructions contained in the methods of loaded classes;
- runtime data areas - the way of organizing memory in JVM:
    - method area (one per VM instance, shared by all threads) - stores type data of the class;
    - heap (one per VM instance, shared by all threads) - stores all objects onto the heap;
    - Java stacks (one per thread) - stores the state of non-native method invocations for the thread:
        - composed of stack frames (frames);
        - stack frame contains the state of one Java method invocation;
        - when a thread invokes a method, the JVM pushes a new frame on that thread's Java stack;
        - after completion, the VM pops and discards the frame for the method.
    - pc registers (one per thread) - indicates the next instruction to execute;
    - native method stacks - sotres the state of native method invocations.
- *native method interface*;
- *native method libraries*.