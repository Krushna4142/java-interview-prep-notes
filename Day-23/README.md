<div align="center">

# 📅 Day 23 – Synchronization & Concurrency

### Managing Shared Resources in Multithreaded Java Applications

<img src="https://img.shields.io/badge/Day-23-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Topic-Concurrency-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Level-Multithreading-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Phase-4-purple?style=for-the-badge" />

</div>

---

## 🔗 Quick Navigation

- [🎯 Goal of the Day](#-goal-of-the-day)
- [🧠 What You’ll Learn](#-what-youll-learn)
- [📌 Why This Topic Matters](#-why-this-topic-matters)
- [📁 Folder Structure](#-folder-structure)
- [🔄 Concurrency Problem](#-concurrency-problem)
- [🔒 Synchronization Overview](#-synchronization-overview)
- [🎯 Interview Preparation](#-interview-preparation-day-23)
- [⏭️ What’s Next?](#️-whats-next)

---

## 🎯 Goal of the Day

The goal of **Day 23** is to understand how **multiple threads safely access shared resources** using **synchronization**.

This day focuses on:

- Understanding race conditions
- Learning synchronization in Java
- Preventing data inconsistency
- Managing concurrent access to shared resources
- Building thread-safe programs

---

## 🧠 What You’ll Learn

By the end of this day, you will clearly understand:

- What concurrency means
- What race condition is
- Why synchronization is needed
- How `synchronized` keyword works
- Difference between synchronized method and block
- Basic thread safety concepts

📌 Detailed explanations and interview preparation notes are available in **notes.md**.

---

## 📌 Why This Topic Matters

Synchronization and concurrency are asked in:

- Core Java interviews
- Backend engineering interviews
- Multithreading discussions
- System design basics

Interviewers use this topic to test:

- Understanding of shared memory problems
- Knowledge of thread safety
- Real-world backend system thinking

---

## 📁 Folder Structure

Day-23-Synchronization-Concurrency/
│
├── README.md # Overview, goals, interview focus
├── notes.md # Detailed interview preparation notes
├── RaceConditionDemo.java
├── SynchronizedMethodDemo.java
└── SynchronizedBlockDemo.java

---

## 🔄 Concurrency Problem

When multiple threads access the **same shared resource**, problems can occur.

Example:

Thread 1 → Reads value
Thread 2 → Reads same value
Thread 1 → Updates value
Thread 2 → Updates value

Result:

Incorrect final value
Data inconsistency

This situation is called a **Race Condition**.

---

## 🔒 Synchronization Overview

Synchronization ensures that:

- Only **one thread accesses a critical section at a time**
- Shared data remains **consistent**
- Concurrent threads do not corrupt data

Java provides:

- `synchronized` keyword
- Object-level locking
- Monitor-based thread control

Basic idea:

Lock → Execute critical section → Release lock

---

## 🎯 Interview Preparation (Day 23)

You should be able to answer:

- What is synchronization in Java?
- What is race condition?
- Why is synchronization required?
- What is the `synchronized` keyword?
- Difference between synchronized method and block?
- What is a critical section?
- What is thread safety?

📌 All answers are structured in **notes.md**.

---

## 🔗 Helpful References

- https://docs.oracle.com/javase/tutorial/essential/concurrency/
- https://www.geeksforgeeks.org/synchronization-in-java/
- https://www.baeldung.com/java-synchronized

---

## ⏭️ What’s Next?

<div align="center">

### 👉 **Day 24 – wait(), notify(), notifyAll()**

Learn about:

- Inter-thread communication
- Thread coordination
- Producer–Consumer problem
- Advanced thread communication mechanisms

<br/>

[➡️ Go to Day 24](../Day-24/README.md)

</div>

---
