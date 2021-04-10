*cur. date: 04/11/2021*

# Why Spring

I've started Spring course by [Chad Darby](https://www.udemy.com/user/chaddarby2/) and since I'm not experienced there are tons of things I don't know. Let's go.

Why we should use Spring:
- simplier than J2EE;
- tons of helper classes.

Main goal of Spring - **simplify Java Enterprise Development**
Other goals include:
- Lightweight development with Java [POJOs](#POJO) (Plain-Old-Java-Objects);
- Dependency injection to promote [loose coupling](#Coupling);
- Declarative programming with Apsect-Oriented-Programming ([AOP](#AOP));
- Minimize boilerplate Java code.

So here comes two questions: wtf is loose coupling, POJO and AOP?
Okay, let's clarify it.

### Coupling

**Coupling in Java** is basically how much info one element has about the other or, in other words, *how often changes in one class force related changes in another one*. So **loose coupling** means that two objects are independent. Opposite to it is *tight coupling* when one object depends on the other.

Example of loose coupling (from [Edureka](https://www.edureka.co/blog/coupling-in-java/#loose)):
```Java
package lc;
 
class Volume {
      public static void main(String args[]) {
           Box b = new Box(25, 25, 25);
           System.out.println(b.getVolume());
      }
}
 
final class Box {
       private int volume;
       Box(int length, int width, int height) {
             this.volume = length * width * height;
       }
       public int getVolume() {
             return volume;
       }
}
```

### AOP

**AOP** or **Aspect-Oriented Programming** basically complements OOP by changing the way of thinking about the structure. In OOP the modularity unit is class and in AOP it's *aspect*. Aspect doesn't have a structure, it is scattered across methods, classes, etc. Let's take metrics in one common aspect. We have different logs which are scattered through different modules, it's irrelevant to the app, it's not a business rule. This feature is basically a crosscutting concern. And *the key idea of **AOP** is to abstract and encapsulate this concern*.

To read further check out [this](https://docs.jboss.org/aop/1.0/aspect-framework/userguide/en/html/what.html).

### POJO

Also let's talk about POJO. I dig deep (not really) into the Google and found the nice explanation to this:

> It is an ordinary Java object, not bound by any special restriction other than those forced by the Java Language Specification and not requiring any classpath. POJOs are used for increasing the readability and re-usability of a program. POJOs have gained the most acceptance because they are easy to write and understand.

**POJOs basically defines an entity!**

[Read here](https://www.geeksforgeeks.org/pojo-vs-java-beans/#:~:text=POJO%20stands%20for%20Plain%20Old,re%2Dusability%20of%20a%20program.)