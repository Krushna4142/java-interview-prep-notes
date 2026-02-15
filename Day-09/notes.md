# Day 09 – Data Types & Variables (Java Memory Basics)

---

## What is a Data Type in Java?

A data type specifies:

- What type of value a variable can store
- How much memory is allocated
- What operations can be performed on that value

Java is a **strongly typed language**, so every variable must have a declared type.

---

## Java Data Types – Classification

### 1) Primitive Data Types

These store **actual values**.

| Type    | Size    | Default Value |
| ------- | ------- | ------------- |
| byte    | 1 byte  | 0             |
| short   | 2 bytes | 0             |
| int     | 4 bytes | 0             |
| long    | 8 bytes | 0L            |
| float   | 4 bytes | 0.0f          |
| double  | 8 bytes | 0.0d          |
| char    | 2 bytes | '\u0000'      |
| boolean | 1 bit\* | false         |

\* JVM implementation dependent.

---

### 2) Non-Primitive (Reference) Data Types

These store **reference (memory address)**, not the actual object.

Examples:

- String
- Arrays
- Classes
- Interfaces
- Objects

---

## Primitive vs Reference Data Types

| Feature       | Primitive    | Reference         |
| ------------- | ------------ | ----------------- |
| Storage       | Stack        | Stack + Heap      |
| Stores        | Actual value | Memory address    |
| Size          | Fixed        | Depends on object |
| Default value | Yes          | null              |

---

## Variable in Java

A variable is a named memory location used to store data.

### Syntax

type variableName = value;

Example:

int age = 21;

---

## Types of Variables in Java

### 1) Local Variables

Declared inside a method.

- Stored in stack
- No default value
- Must be initialized before use

---

### 2) Instance Variables

Declared inside a class but outside methods.

- Stored in heap (as part of object)
- Gets default values
- Each object has its own copy

---

### 3) Static Variables

Declared using static keyword.

- Stored in Method Area
- Shared among all objects
- Only one copy exists

---

## Memory Management – Stack vs Heap

### Stack Memory

Stores:

- Local variables
- Method calls
- Primitive values
- Object references

Characteristics:

- Fast access
- Thread-specific
- Automatically deallocated

---

### Heap Memory

Stores:

- Objects
- Instance variables
- Arrays

Characteristics:

- Shared across threads
- Managed by Garbage Collector
- Slower than stack

---

## Example – Memory Representation

int a = 10;

Stored directly inside **stack**.

---

Student s = new Student();

Stack:

s → reference

Heap:

Student object → actual data

---

## Default Values (Very Important for Interviews)

Default values are given only to:

- Instance variables
- Static variables

Local variables **do not get default values**.

---

## Important Interview Difference

### Why local variables do not get default values?

Because they are stored in stack and Java does not initialize stack memory automatically for performance reasons.

---

## Literal Types in Java

### Integer Literal

int a = 10;

### Floating Literal

double d = 10.5;

### Character Literal

char c = 'A';

### Boolean Literal

boolean flag = true;

### String Literal

Stored in **String Constant Pool**.

---

## var Keyword (Java 10+)

var x = 10;

- Type is inferred by compiler
- Cannot be used without initialization
- Only for local variables

---

## Type Promotion (Important for Output Questions)

In expressions:

byte → short → int → long → float → double

Example:

byte a = 10;
byte b = 20;
byte c = a + b; ❌ (because result becomes int)

---

## Common Interview Traps

### 1) Uninitialized Local Variable

int a;
System.out.println(a); ❌ Compile-time error

---

### 2) Default Value Confusion

Instance variable gets default value  
Local variable does not.

---

### 3) Reference vs Object

Student s;

Only reference created, object not created.

---

### 4) String Storage

String str = "Java";

Stored in **String Constant Pool**, not normal heap.

---

### 5) Multiple References to Same Object

Student s1 = new Student();
Student s2 = s1;

Both point to same heap object.

---

## Stack vs Heap – One-Line Interview Answer

Stack stores method-level data and references.  
Heap stores actual objects.

---

## Frequently Asked Interview Questions

### Basic Level

What are the 8 primitive data types in Java?  
Difference between primitive and non-primitive?  
What is a variable?  
Types of variables in Java?

---

### Medium Level

Where are local variables stored?  
Why do local variables not have default values?  
What is type promotion?  
Difference between instance and static variables?

---

### Advanced Level

Explain memory allocation for:

Student s = new Student();

How String is stored in memory?  
What happens when multiple references point to same object?

---

## Output-Based Question

int x = 10;
double y = x;

Result → Implicit widening (int → double)

---

byte a = 10;
byte b = 20;
byte c = a + b;

Compile-time error due to int promotion.

---

## Quick Revision

- Primitive → value in stack
- Reference → address in stack, object in heap
- Local → no default value
- Instance → default value
- Static → shared
- String → SCP
- Expression → type promotion to int or higher

---

## Day 09 Summary

Data types define memory usage and operations.  
Variables are memory containers.  
Primitive values are stored in stack.  
Objects are stored in heap.  
Understanding memory flow is critical for Java interviews.

---
