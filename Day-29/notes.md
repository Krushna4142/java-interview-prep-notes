# Day 29 – Java Backend Interview Revision Notes

---

# Core Java Quick Revision

Java is a platform independent programming language.

Write Once Run Anywhere concept is achieved through JVM.

Compilation Flow:

Java Code
↓
Bytecode
↓
JVM
↓
Machine Code

---

# OOP Concepts

Encapsulation

Wrapping data and methods inside a class.

Example

class User
{
private String name;
}

---

Inheritance

One class acquires properties of another.

Example

class Animal
class Dog extends Animal

---

Polymorphism

Method behaves differently based on object.

Types

Method Overloading  
Method Overriding

---

Abstraction

Hiding implementation details.

Achieved using

Abstract classes  
Interfaces

---

# Collections Overview

Collection Framework provides data structures.

Important Interfaces

List  
Set  
Map

---

List

Allows duplicates  
Maintains order

Examples

ArrayList  
LinkedList

---

Set

No duplicates allowed.

Examples

HashSet  
TreeSet

---

Map

Stores key-value pairs.

Examples

HashMap  
TreeMap

---

# Exception Handling

Used to handle runtime errors.

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

---

# Multithreading Basics

Thread is a lightweight process.

Ways to create threads

Thread class  
Runnable interface

---

Synchronization

Used to avoid data inconsistency.

Example

synchronized method

---

# JVM Memory Model

JVM Memory Areas

Heap  
Stack  
Method Area

---

Heap

Stores objects.

---

Stack

Stores method calls and local variables.

---

Garbage Collection

Automatic memory management.

Removes unused objects.

---

# Spring Boot Overview

Spring Boot simplifies Java backend development.

Key Features

Auto configuration  
Embedded server  
Production ready features

---

Spring Boot Architecture

Controller

Handles HTTP requests.

Service

Contains business logic.

Repository

Handles database communication.

---

# API Flow

Client
↓
Controller
↓
Service
↓
Repository
↓
Database

---

# Backend Architecture Summary

Controller → API handling

Service → Business logic

Repository → Data layer

Database → Data storage

---

# Interview Preparation Tips

Understand concepts clearly.

Focus on real-world use cases.

Practice coding questions.

Revise architecture and backend flow.

---

End of Day 29 Notes
