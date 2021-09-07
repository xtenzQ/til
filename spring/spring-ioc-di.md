*cur.date: 04/11/2021*

# Spring IoC and DI

Let's start with core definitions.

Spring **Bean** is a Java object managed by a Spring IoC container. They are created from normal Java classes.

The idea of **Inversion of Control (IoC)** is about outsourcing creation and management of the objects to an object factory.

The *primary function* of Spring Container ("object factory") is to 1) create and manage objects and 2) to inject object's dependencies (Dependency Injection).

Spring Container can be configured with:
- XML (legacy);
- Java Annotations;
- Java Source Code.

Spring development process constsis of:
1. Configuring the Spring Beans;
2. Creating a Spring Container - known as *Application Context*;
3. Retrieving Beans from the container.

**Dependency injection (DI)** - we're basically outsourcing the construction and injection of your object to external entity (Object Factory).

Two most common injections are: constructor injection and setter injection.

<hr>

[Return](../../../)