# Interface vs Abstract Class

- interfaces can have no state or implementation
- a class that implements an interface must provide an implementation of all the methods of that interface
- abstract classes may contain state (data members) and/or implementation (methods)
- abstract classes can be inherited without implementing the abstract methods (though such a derived class is abstract itself)
- interfaces may be multiple-inherited, abstract classes may not (this is probably the key concrete reason for interfaces to exist separately from abtract classes - they permit an implementation of multiple inheritance that removes many of the problems of general MI).

[Original answer by Michael Burr'09](https://stackoverflow.com/a/761342)

Java 8:
- default interface implementation
- interfaces with default implementation allows to add methods to an interface without having to change the existing classes which implement that interface. The new methods get default implementations (while the old methods likely remain without default implementations), and the existing classes which implement the interface don't have to implement new methods.
- Interfaces with default implementation could also be used like abstract classes for multiple [implementation] inheritance.

[Answer by Nick Alexeev'19](https://softwareengineering.stackexchange.com/a/391459)
