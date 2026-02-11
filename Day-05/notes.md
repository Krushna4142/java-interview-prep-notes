# Day 05 – Inheritance in Java (Quick Notes)

---

## What is Inheritance?

Inheritance is an OOP concept where one class (child class) acquires:

- Properties (variables)
- Behaviors (methods)

from another class (parent class).

It represents an **IS-A relationship**.

Example:
Dog IS-A Animal

---

## Why Inheritance is Important?

Inheritance provides:

- Code reusability
- Method overriding
- Runtime polymorphism
- Better hierarchical design
- Reduced code duplication

It is heavily used in:

- Frameworks (Spring, Hibernate)
- Real-world system modeling
- Enterprise applications

---

## Syntax of Inheritance

Inheritance is implemented using the `extends` keyword.

Example:

class Parent {
// properties and methods
}

class Child extends Parent {
// additional features
}

---

## Types of Inheritance in Java

Single Inheritance  
One child inherits from one parent.

Multilevel Inheritance  
A class inherits from a class which itself inherits from another class.

Hierarchical Inheritance  
Multiple classes inherit from one parent class.

Multiple Inheritance  
Not supported using classes.  
Supported using interfaces.

---

## Method Overriding

Method overriding occurs when:

- Child class provides its own implementation
- Same method signature as parent

Rules:

- Method name must be same
- Parameters must be same
- Return type must be same (or covariant)
- Access modifier cannot be more restrictive
- Cannot override final methods
- Static methods are hidden, not overridden

Overriding enables runtime polymorphism.

---

## super Keyword

The `super` keyword is used to:

1. Call parent class constructor
2. Call parent class method
3. Access parent class variables

Important:
Parent constructor is always called first when child object is created.

---

## Constructor and Inheritance

When child object is created:

1. Parent constructor executes first
2. Then child constructor executes

If parent constructor has parameters,
child must explicitly call it using:

super(arguments);

If not defined, default constructor is called automatically.

---

## final Keyword in Inheritance

final class

- Cannot be inherited

final method

- Cannot be overridden

Used to restrict inheritance.

Example:
String class is final.

---

## Access Modifiers and Inheritance

private members

- Not accessible in child class

protected members

- Accessible within package and child class

public members

- Accessible everywhere

default members

- Accessible within same package only

---

## Important Interview Differences

Inheritance vs Composition

Inheritance:

- IS-A relationship
- Tight coupling

Composition:

- HAS-A relationship
- More flexible design

Modern design prefers composition over inheritance in many cases.

---

## Common Interview Questions

- What is inheritance?
- What is IS-A relationship?
- Why Java does not support multiple inheritance?
- What happens if parent constructor is private?
- Can we override static methods?
- What is the use of super keyword?
- Difference between inheritance and composition?

---

## Common Beginner Mistakes

- Thinking constructors are inherited
- Trying to override private methods
- Forgetting super() in parameterized constructors
- Confusing overloading with overriding
- Misunderstanding multiple inheritance

---

## Real-World Example

Vehicle (Parent)

Car, Bike (Child)

Common properties:

- speed
- engine

Specific properties:

- Car → doors
- Bike → handle type

---

## Day 05 Summary

- Inheritance enables code reuse
- Represents IS-A relationship
- Implemented using extends
- Supports overriding and runtime polymorphism
- Java does not support multiple inheritance with classes
- super is used to access parent elements

Mastering inheritance is essential for advanced Java and backend development.

---
