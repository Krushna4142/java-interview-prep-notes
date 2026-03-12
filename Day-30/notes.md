# Day 30 – Final Revision Cheat Sheets

# Crack-Ready Backend Revision Notes

---

# 1. Java Compilation Flow

Java follows the **Write Once Run Anywhere** principle.

Flow:

Java Source Code (.java)
↓
Java Compiler (javac)
↓
Bytecode (.class)
↓
JVM
↓
Machine Code
↓
Program Execution

Important components:

JDK → Development tools  
JRE → Runtime environment  
JVM → Executes bytecode

---

# 2. Java Key Features

Platform Independent

Object Oriented

Secure

Robust

Portable

Multithreaded

High Performance

Distributed

---

# 3. OOP Concepts Quick Revision

Encapsulation

Wrapping data and methods into a single unit.

Example

class User
{
private String name;
}

---

Inheritance

Child class acquires properties of parent class.

Example

class Animal
{
}

class Dog extends Animal
{
}

---

Polymorphism

Same method behaves differently.

Types

Method Overloading  
Method Overriding

---

Abstraction

Hiding internal implementation details.

Achieved using:

Abstract classes  
Interfaces

---

# 4. Data Types Overview

Primitive Data Types

byte  
short  
int  
long  
float  
double  
char  
boolean

---

Non-Primitive Data Types

String

Arrays

Classes

Objects

---

# 5. Control Statements

Used to control program flow.

Conditional Statements

if  
if-else  
switch

---

Looping Statements

for  
while  
do-while

---

Jump Statements

break  
continue  
return

---

# 6. Collections Framework Overview

Java Collection Framework provides data structures.

Main Interfaces

Collection

List

Set

Map

---

# 7. List Interface

Allows duplicates

Maintains insertion order

Examples

ArrayList  
LinkedList  
Vector

---

# 8. Set Interface

Does not allow duplicates.

Examples

HashSet  
LinkedHashSet  
TreeSet

---

# 9. Map Interface

Stores key-value pairs.

Key must be unique.

Examples

HashMap  
LinkedHashMap  
TreeMap  
Hashtable

---

# 10. HashMap Internals

HashMap stores data using **hashing**.

Process

Key hashCode generated  
↓
Bucket index calculated  
↓
Data stored in bucket

If collision occurs → Linked List / Tree structure used.

---

# 11. Comparable vs Comparator

Comparable

Used for natural sorting.

Example

compareTo()

---

Comparator

Used for custom sorting.

Example

compare(Object o1, Object o2)

---

# 12. Exception Handling

Exception is an unwanted event that disrupts program flow.

Structure

try
{
}
catch(Exception e)
{
}
finally
{
}

---

# 13. Types of Exceptions

Checked Exceptions

Checked at compile time.

Examples

IOException  
SQLException

---

Unchecked Exceptions

Checked at runtime.

Examples

NullPointerException  
ArithmeticException  
ArrayIndexOutOfBoundsException

---

# 14. Multithreading Basics

Thread is the smallest unit of execution.

Ways to create thread

1. Extend Thread class

2. Implement Runnable interface

---

# 15. Thread Life Cycle

New

Runnable

Running

Waiting

Terminated

---

# 16. Synchronization

Used to control access to shared resources.

Example

synchronized method

Problem solved

Race condition

---

# 17. Concurrency Problems

Race Condition

Deadlock

Thread Starvation

Solution

Synchronization

Locks

Concurrent utilities

---

# 18. JVM Memory Model

Main memory areas

Heap Memory

Stack Memory

Method Area

---

Heap Memory

Stores objects.

Shared among threads.

---

Stack Memory

Stores method calls and local variables.

Each thread has its own stack.

---

Method Area

Stores class metadata and static variables.

---

# 19. Garbage Collection

Automatic memory management in Java.

Removes unused objects from heap memory.

Benefits

Prevents memory leaks

Improves application performance

---

# 20. Spring Boot Overview

Spring Boot is a framework used to build Java backend applications quickly.

Key features

Auto configuration

Embedded server

Production ready setup

Minimal configuration

---

# 21. Spring Boot Architecture

Typical layered architecture:

Controller  
Service  
Repository  
Database

---

Controller Layer

Handles HTTP requests.

Example

@GetMapping("/users")

---

Service Layer

Contains business logic.

Processes application rules.

---

Repository Layer

Handles database operations.

Uses JPA / Hibernate.

---

# 22. REST API Basics

REST stands for Representational State Transfer.

REST APIs use HTTP methods.

GET

POST

PUT

DELETE

Example

GET /users  
POST /users  
PUT /users/1  
DELETE /users/1

---

# 23. Spring Boot API Flow

Client
↓
DispatcherServlet
↓
Controller
↓
Service
↓
Repository
↓
Database
↑
Repository
↑
Service
↑
Controller
↑
Client

---

# 24. Backend Architecture Principles

Separation of concerns

Layered design

Loose coupling

High maintainability

Scalable systems

---

# 25. Backend Interview Quick Revision

Core Java fundamentals

OOP principles

Collections framework

Exception handling

Multithreading

JVM internals

Spring Boot architecture

REST API flow

---

# Final Learning Summary

You have revised:

Core Java

Object Oriented Programming

Collections Framework

Exception Handling

Multithreading

JVM Internals

Spring Boot Backend

REST API Architecture

Backend Interview Concepts

---

# Final Message

Consistent learning and clear understanding of fundamentals are the foundation of strong software engineering skills.

Keep building projects, explore system design, and continue improving your problem solving ability.

---

# End of Day 30 Notes
