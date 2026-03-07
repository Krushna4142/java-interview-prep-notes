# 📘 Day 24 – JVM Memory & Garbage Collection (Complete Notes + Cheat Sheet)

---

# 🎯 Learning Goal

Understand how **Java manages memory internally** and how **Garbage Collection automatically removes unused objects**.

Topics covered:

```
✔ JVM Memory Architecture
✔ Heap vs Stack
✔ Method Area
✔ Program Counter
✔ Garbage Collection
✔ GC Algorithms
✔ Memory Errors
✔ Interview Questions
✔ Quick Cheat Sheet
```

---

# 🧠 JVM Memory Architecture

The **Java Virtual Machine (JVM)** divides memory into multiple regions.

```
JVM Memory
│
├── Heap Memory
│
├── Stack Memory
│
├── Method Area
│
├── Program Counter (PC Register)
│
└── Native Method Stack
```

Each region has a **specific purpose**.

---

# 🧩 1️⃣ Heap Memory

Heap memory stores **objects and instance variables**.

All objects created using `new` keyword are stored in **heap**.

Example:

```java
class Student {

    int id;
    String name;

    public static void main(String[] args) {

        Student s1 = new Student();

    }
}
```

Memory behavior:

```
Stack → Reference Variable (s1)
Heap → Actual Object
```

Visualization:

```
Stack Memory          Heap Memory
------------          -----------
s1  ------------>     Student Object
                      id
                      name
```

---

# 🧩 Heap Structure

Heap is divided into **Generations**.

```
Heap Memory
│
├── Young Generation
│   ├── Eden Space
│   ├── Survivor Space S0
│   └── Survivor Space S1
│
└── Old Generation
```

---

# 🌱 Young Generation

Where **new objects are created**.

Lifecycle:

```
New Object
   ↓
Eden Space
   ↓
Survivor Space
   ↓
Old Generation
```

---

# 🧓 Old Generation

Stores **long-living objects**.

Objects that survive multiple GC cycles are moved here.

---

# 🧩 2️⃣ Stack Memory

Stack stores:

```
✔ Method Calls
✔ Local Variables
✔ References
✔ Partial Results
```

Each **thread gets its own stack**.

Example:

```java
class StackExample {

    public static void main(String[] args) {

        int a = 10;
        int b = 20;

        int result = add(a, b);

        System.out.println(result);
    }

    static int add(int x, int y) {

        return x + y;

    }
}
```

Stack flow:

```
Stack Memory

main()
 ├─ a
 ├─ b
 └─ result

add()
 ├─ x
 └─ y
```

When method finishes → **stack frame removed**.

---

# 🧩 3️⃣ Method Area

Stores **class level information**.

```
Method Area Stores:

✔ Class Metadata
✔ Static Variables
✔ Method Bytecode
✔ Runtime Constant Pool
```

Example:

```java
class Test {

    static int count = 0;

}
```

`count` will be stored in **Method Area**.

---

# 🧩 4️⃣ Program Counter Register

PC Register stores:

```
Address of current executing instruction
```

Each thread has its **own PC register**.

---

# 🧩 5️⃣ Native Method Stack

Used for **native methods written in C/C++**.

Example:

```
Java → Native Library → OS
```

---

# ♻️ Garbage Collection (GC)

Garbage Collector automatically removes **unused objects**.

Goal:

```
✔ Free Heap Memory
✔ Prevent Memory Leak
✔ Improve Performance
```

Java developers **do not manually free memory**.

---

# 🧠 When Object Becomes Eligible for GC

An object becomes eligible for GC when:

```
No references point to that object
```

Example:

```java
class Demo {

    public static void main(String[] args) {

        Demo obj = new Demo();

        obj = null;

    }

}
```

Now object is **eligible for Garbage Collection**.

---

# 🧠 Types of Garbage Collection

### 1️⃣ Minor GC

Occurs in **Young Generation**.

```
Eden → Survivor
```

---

### 2️⃣ Major GC

Occurs in **Old Generation**.

---

### 3️⃣ Full GC

Cleans **entire heap memory**.

---

# ⚙️ Object Lifecycle

```
Object Created
      ↓
Eden Space
      ↓
Survivor Space
      ↓
Old Generation
      ↓
Garbage Collected
```

---

# 🧠 Garbage Collector Types

```
Serial GC
Parallel GC
CMS GC
G1 GC
ZGC
Shenandoah
```

---

### Serial GC

```
Single Thread
Used in small apps
```

---

### Parallel GC

```
Multiple Threads
Better throughput
```

---

### G1 GC (Garbage First)

```
Modern GC
Region-based memory
Used in large applications
```

---

# ⚠️ Common JVM Memory Errors

---

# 1️⃣ OutOfMemoryError

Occurs when **heap memory is full**.

Example:

```
java.lang.OutOfMemoryError: Java heap space
```

---

# 2️⃣ StackOverflowError

Occurs when **recursion becomes too deep**.

Example:

```java
class Test {

    static void recursive() {

        recursive();

    }

    public static void main(String[] args) {

        recursive();

    }

}
```

---

# 🧠 Stop-The-World Event

During GC:

```
All application threads pause temporarily
```

This is called:

```
Stop-The-World
```

---

# 🧠 Heap vs Stack (Interview)

```
Heap
-----
Stores Objects
Shared by Threads
Large Memory
Garbage Collected

Stack
-----
Stores Method Calls
Thread Specific
Small Memory
Automatically Cleared
```

---

# 🧠 Quick Interview Questions

### Q1. What is JVM?

```
Java Virtual Machine that runs Java bytecode.
```

---

### Q2. Where are objects stored?

```
Heap Memory
```

---

### Q3. What is stack used for?

```
Method calls and local variables.
```

---

### Q4. What triggers Garbage Collection?

```
Objects with no references.
```

---

# ⚡ JVM Memory Flow

```
Java Code
   ↓
Compiled to Bytecode
   ↓
Class Loader
   ↓
JVM Memory
   ↓
Execution Engine
   ↓
Garbage Collector
```

---

# 📌 JVM Memory Diagram

```
              JVM Memory
              ───────────

        +---------------------+
        |    Method Area      |
        +---------------------+

        +---------------------+
        |       Heap          |
        |  Young + Old Gen    |
        +---------------------+

        +---------------------+
        |       Stack         |
        |   Method Frames     |
        +---------------------+

        +---------------------+
        |    PC Register      |
        +---------------------+
```

---

# 🔖 SUPER QUICK CHEAT SHEET

```
JVM MEMORY

Heap
 → Objects
 → Instance variables
 → Garbage collected

Stack
 → Method calls
 → Local variables

Method Area
 → Class metadata
 → Static variables

PC Register
 → Current instruction pointer
```

---

```
HEAP STRUCTURE

Young Generation
   Eden
   Survivor S0
   Survivor S1

Old Generation
   Long living objects
```

---

```
GARBAGE COLLECTION

Minor GC → Young Gen

Major GC → Old Gen

Full GC → Entire Heap
```

---

```
COMMON ERRORS

OutOfMemoryError
StackOverflowError
```

---

# 🚀 Key Takeaways

```
✔ JVM manages memory automatically
✔ Heap stores objects
✔ Stack stores method calls
✔ Garbage Collector removes unused objects
✔ Young Generation stores new objects
✔ Old Generation stores long-living objects
```

---

# 📅 Progress

```
Day 24 Complete ✅
```

Next:

```
Day 25 – File Handling Basics
```

---
