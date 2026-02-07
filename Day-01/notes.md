# Day 01 – Java Introduction & JVM Internals (Quick Notes)

---

## 🔹 What is Java?

Java is a **high-level, object-oriented programming language** where:

- Code is written once
- Compiled into **bytecode**
- Executed using **JVM**

Java programs do **not run directly on the operating system**.  
They always run inside the **Java Virtual Machine (JVM)**.

📌 Java is mainly used for **enterprise, backend, and large-scale systems**.

---

## 👤 Why Java Was Introduced

Before Java:

- Programs were **platform-dependent**
- Same code could not run on different operating systems
- Manual memory management caused errors
- Security issues were common

Java solved these problems by:

- Introducing **bytecode**
- Using a **virtual machine (JVM)**
- Providing **automatic memory management**
- Improving **security and reliability**

---

## 🖥️ Platform Independence (Key Concept)

Java is platform-independent because:

- Java source code is compiled into **bytecode**
- Bytecode is **not OS-specific**
- JVM converts bytecode into machine code

📌 Same bytecode + different JVMs = same program behavior.

---

## 🔄 JVM – Java Virtual Machine

The **JVM** is responsible for:

- Loading Java bytecode
- Verifying bytecode for security
- Executing bytecode

Important points:

- JVM is **platform-dependent**
- JVM understands **only bytecode**
- JVM cannot execute `.java` files directly

---

## ☕ JRE – Java Runtime Environment

The **JRE** provides the environment required to **run Java programs**.

It contains:

- JVM
- Core Java libraries

📌 JRE is used only for **execution**, not development.

---

## 🧰 JDK – Java Development Kit

The **JDK** is used to **develop Java applications**.

It contains:

- JRE
- Java compiler (`javac`)
- Development and debugging tools

📌 Developers must install **JDK**.

---

## 🔗 Relationship Between JVM, JRE, and JDK

Hierarchy:

JDK  
→ JRE  
→ JVM

📌 JDK is for development  
📌 JRE is for execution  
📌 JVM runs the program

---

## 🔄 Java Program Execution Flow

Basic execution steps:

1. Write Java source file (`.java`)
2. Compile using `javac`
3. Bytecode file (`.class`) is generated
4. JVM loads the bytecode
5. JVM executes the program

📌 Platform independence is achieved at **bytecode level**.

---

## ☕ Java Perspective (Very Important)

In a Java application:

Source Code  
↓  
Bytecode  
↓  
JVM  
↓  
Operating System

- Java does not interact directly with OS
- JVM acts as an intermediate layer

---

## 🎤 Interview One-Liners

- Java runs on JVM, not directly on OS
- JVM executes bytecode
- JRE is required to run Java programs
- JDK is required to develop Java programs
- Bytecode enables platform independence

---

## ⚠️ Common Beginner Mistakes

- Saying Java runs directly on OS
- Confusing JVM with JDK
- Saying JVM is platform-independent
- Thinking JDK is required to run programs
- Ignoring bytecode concept

---

## ✅ Day 01 Summary

- Java is platform-independent
- JVM executes bytecode
- JRE provides runtime environment
- JDK is used for development
- This topic forms the **foundation of Java interviews**

---
