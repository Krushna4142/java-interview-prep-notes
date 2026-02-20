# Day 12 – OOP Concepts – Part 2 (Encapsulation & Abstraction)

---

## Encapsulation

Encapsulation is the process of:

- Binding variables and methods into a single unit
- Hiding internal data from outside world

It is achieved by:

- Declaring variables as private
- Providing public getters and setters

---

## Why Encapsulation?

- Data security
- Controlled access
- Flexibility to change implementation
- Improves maintainability

---

## Example

class Student {

    private int rollNo;

    public int getRollNo() {
        return rollNo;
    }

    public void setRollNo(int rollNo) {
        this.rollNo = rollNo;
    }

}

---

## Data Hiding

Data hiding means:

Direct access to variables is restricted.

Access is provided through methods.

---

## Advantages of Encapsulation

- Read-only class → only getter
- Write-only class → only setter
- Full control over data

---

## Abstraction

Abstraction means:

Showing only essential information and hiding implementation details.

Real-world example:

ATM → withdraw(), deposit()  
User does not know internal processing.

---

## Ways to Achieve Abstraction

1. Abstract class
2. Interface

---

## Abstract Class

A class declared using abstract keyword.

It can have:

- Abstract methods
- Concrete methods
- Constructors
- Variables

Cannot be instantiated.

---

### Abstract Method

A method without body.

abstract void display();

Must be implemented by child class.

---

## Example

abstract class Vehicle {

    abstract void start();

}

class Car extends Vehicle {

    void start() {
    }

}

---

## Interface (Introduction Level)

Interface is a blueprint of a class.

It contains:

- Abstract methods (default)
- public static final variables

Used to achieve 100% abstraction.

---

## Example

interface Animal {

    void sound();

}

class Dog implements Animal {

    public void sound() {
    }

}

---

## Abstract Class vs Interface

Abstract Class:

- Can have constructors
- Can have concrete methods
- Supports partial abstraction

Interface:

- No constructors
- Methods are abstract by default
- Supports multiple inheritance

---

## Encapsulation vs Abstraction

Encapsulation:

- Hides data
- Achieved using private variables

Abstraction:

- Hides implementation
- Achieved using abstract class & interface

---

## Real Interview Scenarios

### When to use Encapsulation?

When you want:

- Data security
- Validation before setting value

---

### When to use Abstraction?

When:

- Implementation changes but behaviour remains same
- You design common template for multiple classes

---

## Common Interview Questions

### Basic

What is encapsulation?  
What is abstraction?

---

### Medium

Why use getters and setters?  
Can abstract class have constructor?  
Can we create object of abstract class?

---

### Advanced

Difference between interface and abstract class?  
Why interface variables are public static final?  
Which is faster: abstract class or interface?

---

## Important Rules

- Private variables cannot be accessed outside class
- Abstract class cannot be instantiated
- Interface methods are public by default
- A class can implement multiple interfaces

---

## Memory Point

Encapsulation:

Data → hidden → accessed via methods

Abstraction:

Method declaration → child provides implementation

---

## Interview One-Liners

Encapsulation is data hiding.

Abstraction is implementation hiding.

Abstract class provides partial abstraction.

Interface provides full abstraction.

---

## Quick Revision

Encapsulation → private + getter/setter  
Abstraction → abstract class & interface  
Abstract class → IS-A relationship  
Interface → CAN-DO relationship

---

## Day 12 Summary

Encapsulation protects data.

Abstraction hides complexity.

Together they:

- Make code secure
- Make code scalable
- Help in real-world design
- Are heavily asked in interviews

These are core for:

Spring Boot  
System Design  
Low-Level Design

---
