<p align="center">
  <img src="https://raw.githubusercontent.com/your-username/java-system-design-for-beginners/main/assets/banner.png" width="100%">
</p>

<h1 align="center">Day 24 – JVM Memory & GC Cheat Sheet</h1>

<p align="center">
A quick revision guide for understanding <b>JVM Memory Structure</b> and <b>Garbage Collection</b>.
</p>

<p align="center">

![Java](https://img.shields.io/badge/Language-Java-orange)
![Level](https://img.shields.io/badge/Level-Intermediate-blue)
![Topic](https://img.shields.io/badge/Topic-JVM--Memory-green)
![Type](https://img.shields.io/badge/Type-CheatSheet-yellow)
![Progress](https://img.shields.io/badge/Day-24-red)

</p>

---

# 📘 Day 24 – JVM Memory & GC Cheat Sheet

## 🎯 Goal of Today

Understand how **Java manages memory internally** and how **Garbage Collection cleans unused objects automatically**.

This cheat sheet is designed for:

- ⚡ Quick Revision
- 💼 Interview Preparation
- 🧠 JVM Internal Understanding

---

# 🧠 JVM Memory Overview

The **Java Virtual Machine (JVM)** divides memory into multiple sections.

```
JVM Memory
│
├── Heap Memory
│   ├── Young Generation
│   │   ├── Eden
│   │   ├── Survivor 0
│   │   └── Survivor 1
│   │
│   └── Old Generation
│
├── Stack Memory
│
├── Method Area
│
└── Program Counter (PC Register)
```

---

# 🧩 1️⃣ Heap Memory

Heap stores **objects and instance variables**.

```
Heap Memory
│
├── Young Generation
│   ├── Eden
│   ├── Survivor Space 0
│   └── Survivor Space 1
│
└── Old Generation
```

### Young Generation

Where **new objects are created**.

Lifecycle:

```
New Object → Eden → Survivor → Old Generation
```

### Old Generation

Stores **long-lived objects**.

---

# 🧩 2️⃣ Stack Memory

Stack stores:

- Method calls
- Local variables
- References

Each **thread gets its own stack**.

Example:

```java
public class StackExample {

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

Stack Flow:

```
main()
 ├─ a
 ├─ b
 └─ result

add()
 ├─ x
 └─ y
```

---

# 🧩 3️⃣ Method Area

Stores:

- Class metadata
- Static variables
- Method bytecode
- Runtime constant pool

Example:

```
Class Info
Method Info
Static Variables
```

---

# 🧩 4️⃣ Program Counter Register

Stores **current instruction address**.

Each thread has its own **PC register**.

---

# ♻️ Garbage Collection (GC)

Garbage Collector automatically removes **unused objects** from memory.

Goal:

```
Free Heap Memory
Improve Performance
Avoid Memory Leaks
```

---

# 🔍 How Garbage Collection Works

Objects become eligible for GC when:

```
No references point to them
```

Example:

```java
class Demo {

    public static void main(String[] args) {

        Demo obj = new Demo();

        obj = null;   // eligible for garbage collection

    }
}
```

---

# 🧠 Types of Garbage Collectors

### Serial GC

Single-threaded collector.

```
Used in small applications
```

---

### Parallel GC

Uses multiple threads.

```
Improves throughput
```

---

### G1 Garbage Collector

Modern GC for **large applications**.

```
Region-based memory management
```

---

# ⚙️ JVM GC Process (Simplified)

```
1. Objects created in Eden
2. Survive → move to Survivor
3. Survive multiple cycles → Old Generation
4. Old objects cleaned by Full GC
```

---

# 📊 Heap Visualization

```
Heap Memory
│
├── Young Generation
│   ├── Eden (New Objects)
│   ├── S0
│   └── S1
│
└── Old Generation (Long-lived Objects)
```

---

# ⚠️ Common JVM Memory Errors

### 1️⃣ OutOfMemoryError

Occurs when heap is full.

Example:

```
java.lang.OutOfMemoryError: Java heap space
```

---

### 2️⃣ StackOverflowError

Occurs due to **deep recursion**.

Example:

```java
public class StackOverflowExample {

    static void recursiveCall() {
        recursiveCall();
    }

    public static void main(String[] args) {
        recursiveCall();
    }
}
```

---

# 🧠 Interview Questions

### Q1: Difference between Heap and Stack?

```
Heap → Objects
Stack → Method calls & local variables
```

---

### Q2: What triggers Garbage Collection?

```
When objects become unreachable
```

---

### Q3: What is Stop-the-World?

```
GC pauses application threads temporarily.
```

---

# 🚀 Key Takeaways

```
✔ Heap stores objects
✔ Stack stores method calls
✔ Method Area stores class metadata
✔ Garbage Collector frees unused memory
✔ JVM manages memory automatically
```

---

# 📅 Progress Tracker

```
Phase 1 – Backend Basics
Phase 2 – Core Java
Phase 3 – Collections
Phase 4 – Exception Handling & Concurrency
```

```
Day 24 Complete ✅
```

---

# 🔗 Next Day

```
Day 25 – File Handling Basics
```

---

<p align="center">
⭐ If this repository helps you learn Java & System Design, consider giving it a star.
</p>

<p align="center">
Built with consistency 🚀
</p>
