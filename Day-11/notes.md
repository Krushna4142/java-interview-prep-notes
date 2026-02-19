# Day 11 – OOP Concepts – Part 1 (Real-World Mapping)

---

## What is Object-Oriented Programming?

Object-Oriented Programming (OOP) is a programming paradigm based on:

- Objects
- Classes
- Real-world entity modelling

It allows us to structure programs in a modular and reusable way.

Instead of writing logic step-by-step, we design systems using objects.

---

## Why OOP?

OOP helps in:

- Code reusability
- Modularity
- Scalability
- Maintainability
- Real-world representation

It is the backbone of Java and modern backend development.

---

## Real-World Mapping Concept

Real-world entity → Class  
Real-world instance → Object

Example:

Blueprint → Class  
Actual house → Object

Car → Class  
BMW, Audi → Objects

---

## What is a Class?

A class is a blueprint or template used to create objects.

It contains:

- Variables → properties → state
- Methods → behaviour → actions

Example:

class Car {
String color;
int speed;

    void drive() {
    }

}

---

## What is an Object?

An object is an instance of a class.

It represents a real-world entity.

Example:

Car c = new Car();

Here:

- Car → class
- c → reference variable
- new Car() → object

---

## Memory Representation

Car c = new Car();

Stack Memory:

c → reference

Heap Memory:

Car object → actual data

---

## Class vs Object

| Class                  | Object                        |
| ---------------------- | ----------------------------- |
| Blueprint              | Real entity                   |
| Logical                | Physical                      |
| No memory when defined | Memory allocated when created |
| Used to create objects | Instance of class             |

---

## Object Creation – 3 Steps

1. Declaration

Car c;

2. Instantiation

new Car();

3. Initialization

Car c = new Car();

---

## Multiple Objects

Each object has:

- Separate memory
- Separate copy of instance variables

Example:

Car c1 = new Car();  
Car c2 = new Car();

Both stored in different heap locations.

---

## Reference Variable

A reference variable:

- Stores address of object
- Does not store actual data

Example:

Car c;

Only reference created, object not created.

---

## Object Without Reference

new Car();

Valid but cannot be accessed later.

Used for:

- Anonymous objects
- Method calling

---

## Fields (Instance Variables)

Variables defined inside class and outside methods.

Characteristics:

- Stored in heap
- Get default values
- Belong to object

---

## Methods

Methods define behaviour of an object.

Example:

void startEngine() {
}

They operate on instance variables.

---

## Real-World Example

class Student {

    String name;
    int rollNo;

    void study() {
    }

}

Student s1 = new Student();

Mapping:

Student → class  
s1 → object  
name, rollNo → state  
study() → behaviour

---

## Identity, State, Behaviour (Very Important)

Every object has:

### 1) Identity

Unique reference.

### 2) State

Values of variables.

### 3) Behaviour

Methods.

---

## Constructors (Interview Preview)

A constructor:

- Is used to initialize object
- Has same name as class
- Has no return type
- Automatically called when object is created

Example:

Car() {
}

---

## this Keyword (Preview)

this refers to:

Current object.

Used to:

- Access instance variables
- Resolve naming conflicts

---

## Method Calling Using Object

Car c = new Car();

c.drive();

Object is required to call non-static methods.

---

## Can a Class Exist Without Object?

Yes.

But instance members cannot be used without object.

---

## Can an Object Exist Without Class?

No.

Object is always created from a class.

---

## Common Interview Mistakes

- Thinking class occupies memory
- Confusing reference with object
- Forgetting new keyword
- Believing multiple objects share instance data
- Trying to access non-static members without object

---

## Output-Based Questions

### Example 1

Student s;

System.out.println(s);

Output:
Compile-time error (local variable not initialized)

---

### Example 2

Student s = new Student();
Student s2 = s;

Both point to same object.

---

### Example 3

new Student().study();

Valid anonymous object.

---

## Stack vs Heap in OOP

Stack:

- Reference variables
- Method calls

Heap:

- Object
- Instance variables

---

## Accessing Object Data

Using dot operator:

object.variable  
object.method()

Example:

s1.name  
s1.study()

---

## OOP Thinking Style (Most Important for Interviews)

Procedural thinking:

Write steps.

OOP thinking:

Identify:

- Object
- State
- Behaviour

Then design class.

---

## Interview One-Liners

Class is a blueprint for creating objects.

Object is an instance of a class.

Objects are stored in heap memory.

Reference variables store object address.

Every object has state and behaviour.

---

## Frequently Asked Interview Questions

### Basic Level

What is OOP?  
What is a class?  
What is an object?  
Difference between class and object?

---

### Medium Level

What happens when object is created?  
Where are objects stored?  
What is reference variable?  
Can we create multiple objects?

---

### Advanced Level

Explain memory for:

Student s = new Student();

What is anonymous object?  
Why objects are created using new?  
Can class exist without object?

---

## Quick Revision

- Class → blueprint
- Object → real entity
- new → allocates memory
- Reference → stored in stack
- Object → stored in heap
- Each object → separate state
- Identity + State + Behaviour

---

## Day 11 Summary

OOP allows real-world modelling in Java.

Class defines structure.  
Object represents real entity.

Understanding memory, reference, and object creation is critical for:

- Java interviews
- Spring Boot
- Low-level design
- Clean code architecture

This is the foundation for:

Encapsulation  
Inheritance  
Polymorphism  
Abstraction

---
