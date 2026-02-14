# 📘 Day 08 – Java Overview & JVM Architecture ☕⚙️

> Understanding How Java Actually Works Internally

<img src="https://img.shields.io/badge/Day-08-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Difficulty-Easy--Medium-success?style=for-the-badge" />
<img src="https://img.shields.io/badge/Focus-JVM%20Architecture-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />

</div>

---

## 🎯 Objective

Today’s goal is to deeply understand:

- What Java really is
- How Java achieves platform independence
- JVM architecture & internal components
- Memory areas inside JVM
- Class loading process
- Execution engine
- Why Java is powerful for scalable systems

This is not just syntax.
This is how Java works under the hood.

---

# 🧠 1️⃣ What is Java?

Java is:

- High-level programming language
- Object-Oriented
- Platform Independent
- Strongly typed
- Compiled + Interpreted

Java follows:

Write Once, Run Anywhere (WORA)

---

# 🔄 2️⃣ How Java Code Actually Runs

Step-by-step execution flow:

```
.java file
   ↓ (javac compiler)
.bytecode (.class file)
   ↓
JVM
   ↓
Machine Code
   ↓
Program Executes
```

Java is both:

- Compiled (source → bytecode)
- Interpreted / JIT compiled (bytecode → machine code)

---

# 🌍 3️⃣ Why Java is Platform Independent?

Because of **Bytecode + JVM**

- Java compiler generates bytecode
- Bytecode is platform neutral
- JVM converts bytecode into machine-specific instructions

Different OS → Different JVM  
Same bytecode → Works everywhere

---

# 🏗 4️⃣ JVM Architecture Overview

JVM (Java Virtual Machine) is responsible for:

- Loading classes
- Verifying bytecode
- Allocating memory
- Executing code
- Garbage collection

---

## 🔹 High-Level JVM Architecture

```
Class Loader Subsystem
        ↓
Runtime Data Areas (Memory)
        ↓
Execution Engine
        ↓
Native Interface
```

---

# 📦 5️⃣ Class Loader Subsystem

Responsible for loading `.class` files into memory.

### Types of Class Loaders:

1. Bootstrap ClassLoader
   - Loads core Java classes (java.lang, java.util)

2. Extension ClassLoader
   - Loads extension libraries

3. Application ClassLoader
   - Loads application classes

### Class Loading Process:

1. Loading
2. Linking
   - Verification
   - Preparation
   - Resolution
3. Initialization

---

# 🧠 6️⃣ JVM Memory Structure (Runtime Data Areas)

JVM memory is divided into:

---

## 🔹 Method Area

- Stores class metadata
- Static variables
- Method bytecode
- Shared among all threads

---

## 🔹 Heap Area

- Stores objects
- Shared among all threads
- Managed by Garbage Collector
- Largest memory area

Example:

```
User u = new User();
```

Object is stored in Heap.

---

## 🔹 Stack Area

- Each thread has its own stack
- Stores method calls
- Local variables
- Partial results

When method ends → Stack frame removed

---

## 🔹 PC Register

- Stores address of current instruction
- Each thread has its own PC register

---

## 🔹 Native Method Stack

- Used for native (C/C++) methods

---

# ⚙ 7️⃣ Execution Engine

Responsible for executing bytecode.

Components:

---

## 🔹 Interpreter

- Executes bytecode line by line
- Slower execution

---

## 🔹 JIT Compiler (Just-In-Time)

- Converts bytecode into native machine code
- Improves performance
- Frequently used methods get compiled

---

## 🔹 Garbage Collector (GC)

- Automatically removes unused objects
- Frees heap memory
- Prevents memory leaks

---

# 🛡 8️⃣ Bytecode Verifier

Ensures:

- No illegal memory access
- No stack overflow
- Code follows JVM rules
- Security & safety

---

# 🔌 9️⃣ JNI (Java Native Interface)

Allows Java to:

- Call native code (C/C++)
- Interact with OS-specific libraries

Used in:

- Performance-critical systems
- Hardware interaction

---

# 🚀 🔟 JVM vs JRE vs JDK

| Component | Purpose                 |
| --------- | ----------------------- |
| JVM       | Runs bytecode           |
| JRE       | JVM + Libraries         |
| JDK       | JRE + Development tools |

JDK contains:

- javac (compiler)
- javadoc
- debugger tools

---

# 📊 1️⃣1️⃣ Java Execution Summary

Java Code → Compiled → Bytecode → Loaded → Verified → Executed → Garbage Collected

This layered design makes Java:

- Secure
- Portable
- Scalable
- Enterprise-ready

---

# 🧠 30-Second Interview Revision

✔ Java is compiled + interpreted  
✔ Bytecode ensures platform independence  
✔ JVM has ClassLoader, Memory Areas, Execution Engine  
✔ Heap stores objects  
✔ Stack stores method calls  
✔ JIT improves performance  
✔ GC manages memory automatically  
✔ JDK > JRE > JVM

---

# 🏆 Why This Matters for You

As a Computer Engineering student:

Understanding JVM internals helps in:

- Writing memory-efficient code
- Avoiding stack overflow errors
- Debugging memory leaks
- Performing well in interviews
- Understanding system design deeply

Real engineers understand internals.

---

<br/>

## ⏭️ What’s Next?

<div align="center">

## 📌 Next Step

Tomorrow we move deeper into:

Memory management & Garbage Collection internals 🔥<br>

[➡️ Go to Day 09](../Day-09/README.md)

## </div>
