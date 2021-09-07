# JVM Sandbox

JVM Sandbox is a part of Java security model where Java programs run. Ths sandbox protects host system from:
- R/W to the disk;
- making a network connection with untrusted host;
- creating a new process;
- loading a new DLL and calling a native method.

The idea of a sandbox is to welcome code from any source but restricting actions from untrusted code which could possibly harm your system.

Sandbox components:
- class loader (customizable);
- class file verifier;
- safety features of the JVM;
- security manager (customizable);
- Java API.

Customization allows a user to create a sutomized security policy for a Java application.

<hr>

[Return](../../../)