# S.O.L.I.D. Principles
---
- **Single-Responsibility Principle**

*Every class or method in your program should have only a single reason to change.*

An object should only have a single responsibility, that is, only changes to one part of the software's specification should be able to affect the specification of the object.

Gather together the things that change for the same reasons. Separate things that change for different reasons.

- **Open/Closed Principle**

*Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification*

- **Liskov Substitution Principle**

*Objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program.*

> *What is wanted here is something like the following substitution property: If for each object o1 of type S there is an object o2 of type T such that for all programs P defined in terms of T, the behavior of P is unchanged when o1 is substituted for o2 then S is a subtype of T*
> 
> *Barbara Liskov*

- **Interface Segregation Principle**

*Many client-specific interfaces are better than one general-purpose interface.*

- **Dependency Inversion Principle**

*One should depend upon abstractions, [not] concretions.*

## SOLID Principles in Functional Programming
![solid](https://user-images.githubusercontent.com/81258448/186962860-bbacd126-d577-4da4-bcdf-5d75f153f7a9.png)
