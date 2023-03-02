# Interface vs Abstract Class

Abstract classes and interfaces are both used to define abstract types in Java, but there are some differences between them.

- Implementation: Abstract classes can have both abstract and non-abstract methods, while interfaces can only have abstract methods. This means that abstract classes can provide some implementation details, while interfaces only define the method signatures.

- Inheritance: A class can extend only one abstract class, but it can implement multiple interfaces. This means that interfaces are more flexible in terms of inheritance.

- Access modifiers: Methods in an interface are implicitly public and abstract, while methods in an abstract class can have any access modifier (public, protected, or private) and can be either abstract or non-abstract.

- Constructors: Abstract classes can have constructors, while interfaces cannot.

- Variables: Abstract classes can have instance variables, while interfaces cannot. Interfaces can only have static final variables, which are effectively constants.

- Purpose: Abstract classes are generally used when you want to create a base class for a family of related classes, while interfaces are used when you want to define a set of behaviors that can be implemented by unrelated classes.

In summary, abstract classes and interfaces have different strengths and are used in different ways. Abstract classes provide more structure and can provide some implementation details, while interfaces provide more flexibility and are better suited for defining a set of behaviors.

<hr>

[Return](../../../)
