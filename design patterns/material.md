The Dependency Inversion Principle (DIP) states that high level modules should not depend on low level modules; both should depend on abstractions. 

Abstractions should not depend on details.  Details should depend upon abstractions. 


![image](https://user-images.githubusercontent.com/32191603/132082064-d3c33b78-838f-4987-b958-0068b4db95e2.png)


**IOC**

in traditional programming, the custom code that expresses the purpose of the program calls the reusable libraries to take care of generic tasks, but with inversion of control, it is the framework that calls the custom, or task-specific, code."


So, what the heck does that mean? Basically it means that a framework, library or any external code is not called by you, rather than it calls your code from inside itself.


https://kentcdodds.com/blog/inversion-of-control



 ## Java Patterns :

**Inheritance versus composition: How to choose**


In object-oriented programming, we can use inheritance when we know there is an "is a" relationship between a child and its parent class. Some examples would be:

A person is a human.
A cat is an animal.
A car is a  vehicle.


In object-oriented programming, we can use composition in cases where one object "has" (or is part of) another object. Some examples would be:

A car has a battery (a battery is part of a car).
A person has a heart  (a heart is part of a person).
A house has a living room (a living room is part of a house).

**Diamond Problem in Java:**

![image](https://cdn.journaldev.com/wp-content/uploads/2013/07/diamond-problem-multiple-inheritance.png)


This leads to the ambiguity as the compiler doesn’t know which superclass method to execute. Because of the diamond-shaped class diagram, it’s referred to as Diamond Problem in java. The diamond problem in Java is the main reason java doesn’t support multiple inheritances in classes.

**From Java 8**

interfaces are enhanced to have a method with implementation. We can use default and static keyword to create interfaces with method implementation. forEach method implementation in Iterable interface is:
```
default void forEach(Consumer<? super T> action) {
    Objects.requireNonNull(action);
    for (T t : this) {
        action.accept(t);
    }
}
```

**Java 8 Functional Interface**

An interface with exactly one abstract method is called Functional Interface. @FunctionalInterface annotation is added so that we can mark an interface as functional interface.


The reason it's called a "functional interface" is because it effectively acts as a function. Since you can pass interfaces as parameters, it means that functions are now "first-class citizens" like in functional programming languages. This has many benefits, and you'll see them quite a lot when using the Stream API


While functional interfaces have a limit on abstract methods, there is no limit on default or static methods. Default or static methods can fine-tune our interfaces to share different behaviors with inheriting classes.

Before Java 8, if a new method was introduced in an interface, all the implementing classes would break. To fix it, we would need to individually provide the implementation of that method in all the implementing classes.


**Lambda Expression**

Reduced Lines of Code



