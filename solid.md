# What is SOLID?

> SOLID is a mnemonic acronym for five design principles intended to make software designs more understandable, flexible and maintainable

They were first introduced by Robert C. Martin in the early 2000s in his paper *Design Principles and Design Patterns*[^1] and they are the following:

- [Single-Responsibility Principle](https://github.com/mmelamud-godaddy/how-to-become-a-better-developer/blob/main/solid.md#single-responsibility-principle)
- [Open–Closed Principle](https://github.com/mmelamud-godaddy/how-to-become-a-better-developer/blob/main/solid.md#openclosed-principle)
- [Liskov Substitution Principle](https://github.com/mmelamud-godaddy/how-to-become-a-better-developer/blob/main/solid.md#liskov-substitution-principle)
- [Interface Segregation Principle](https://github.com/mmelamud-godaddy/how-to-become-a-better-developer/blob/main/solid.md#interface-segregation-principle)
- [Dependency Inversion Principle](https://github.com/mmelamud-godaddy/how-to-become-a-better-developer/blob/main/solid.md#dependency-inversion-principle)

## SOLID Principles in Functional Programming

<p align="center">
  <img width="440" height="262" src="https://user-images.githubusercontent.com/81258448/186962860-bbacd126-d577-4da4-bcdf-5d75f153f7a9.png">
</p>

## Single-Responsibility Principle

### *Every class or method in your program should have only a single reason to change.*

An object should only have a single responsibility, that is, only changes to one part of the software's specification should be able to affect the specification of the object.

Gather together the things that change for the same reasons. Separate things that change for different reasons.

## Open/Closed Principle

### *Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification*

This principle is usually instantly related to inheritance. A well-defined parent class that holds functionality and children of this class extend or reuse the mentioned functionality. In reality, it just means that we should be able to reuse and extend code without having to modify the original implementation.

Instead of using inheritance, Functional Programming achieves this by using two tools. Composition to create new behaviors from previously defined functions and higher-order functions to change functionality at runtime.

## Liskov Substitution Principle

### *Objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program.*

> *Let q(x) be a property provable about objects x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T.*
> 
> *Barbara Liskov*

In other words:
> Subtypes must not change any supertype’s significant behavior. Here, “significant behavior” means behavior upon which clients of those objects expressly depend

## Interface Segregation Principle

### *Many client-specific interfaces are better than one general-purpose interface.*

Keep interfaces small so that users don’t end up depending on things they don’t need. Creating any interfaces keeps them as small as possible. Divide big interfaces into smaller ones, to make sure every interface delivers exactly what it promises and nothing more.

In terms of FP, this principle is quite intuitive. Keep all the internal logic private and provide only the customer-facing functions outside the module. Show nothing more than what’s necessary to use your module correctly.

JavaScript doesn’t play well with interfaces, but here is a very rough example of applying Interface Segregation Principle in Javascript using composition.

The interface segregation principle states that an entity should never be forced to implement an interface that contains elements which it will never use. For example, a `Penguin` should never be forced to implement a `Bird` interface if that Bird interface includes functionality relating to flying, as penguins (spoiler alert) cannot fly.

```javascript
class Penguin {}

class Bird {}

const flyer = {
    fly() {
        console.log(`Flap flap, I'm flying!`);
    },
};

Object.assign(Bird.prototype, flyer);

const bird = new Bird();
bird.fly(); // Outputs 'Flap flap, I'm flying!'

const penguin = new Penguin();
penguin.fly(); // 'Error: penguin.fly is not a function'
```

## Dependency Inversion Principle

### *One should depend upon abstractions, not on concretions.*

In languages like C#, this is achieved by using two tools. One is to create interfaces to define contracts of a predefined functionality. The other is to use dependency injection so that users of that functionality don't manually instantiate the concrete class, instead, they receive an instance of the interface through their constructor and they just call the appropriate methods on the instance.

In functional programming, abstractions are the default way of handling code, functions are abstractions too, especially in functional programming where we care more about the "shape" of the data instead of to which specific type they are attached to. This creates the possibility to freely change the implementation at runtime by passing functions as parameters to other functions or even returning functions as results from the computation.

 [^1]: [Design Principles and Design Patterns](http://staff.cs.utu.fi/~jounsmed/doos_06/material/DesignPrinciplesAndPatterns.pdf) by Robert C. Martin
