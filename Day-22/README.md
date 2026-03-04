<div align="center">

# 📅 Day 22 – Multithreading Basics

### Introduction to Concurrency & Parallel Execution in Java

<img src="https://img.shields.io/badge/Day-22-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Topic-Multithreading-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Level-Backend%20Foundation-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Phase-4-purple?style=for-the-badge" />

</div>

---

## 🚀 Welcome to Concurrency

Till now your programs were:

Single-threaded
→ One task at a time
→ Sequential execution

From today:

Multi-threaded
→ Multiple tasks simultaneously
→ Better CPU utilization
→ Real-world backend behavior

Multithreading is a **core backend & system-level skill**.

---

## 🎯 Goal of the Day

- Understand what a thread is
- Learn process vs thread
- Create threads in Java
- Understand thread lifecycle
- Learn basic thread methods
- Understand context switching
- Build foundation for synchronization

---

## 🧠 What is a Thread?

A Thread is:

→ A lightweight unit of execution  
→ Smallest independent path of execution  
→ Part of a process

Example:

- Playing music
- Downloading file
- Typing message

All running simultaneously.

---

## 🆚 Process vs Thread

| Feature       | Process             | Thread              |
| ------------- | ------------------- | ------------------- |
| Definition    | Independent program | Sub-part of process |
| Memory        | Separate memory     | Shared memory       |
| Communication | Slow                | Fast                |
| Creation Cost | High                | Low                 |
| Example       | Chrome Browser      | Tabs inside Chrome  |

---

## 🛠 Ways to Create Thread in Java

### 1️⃣ Extending Thread Class

class MyThread extends Thread {
public void run() {
System.out.println("Thread running");
}
}

---

### 2️⃣ Implementing Runnable Interface (Recommended)

class MyRunnable implements Runnable {
public void run() {
System.out.println("Thread running");
}
}

Better because:
✔ Supports multiple inheritance  
✔ More flexible  
✔ Industry standard

---

## 🔄 Thread Lifecycle

New
↓
Runnable
↓
Running
↓
Blocked / Waiting
↓
Terminated

---

## 🔧 Important Thread Methods

start() → Starts thread  
run() → Contains thread logic  
sleep(ms) → Pause execution  
join() → Wait for thread to finish  
setPriority() → Set thread priority  
currentThread() → Get current thread

---

## ⚡ Example Flow

Thread t1 = new Thread(new MyRunnable());
t1.start();

Important:
Never call run() directly.
Always call start().

---

## 🧠 What is Context Switching?

When CPU switches from one thread to another.

Managed by:
→ Thread Scheduler  
→ JVM + OS

Too many threads:
→ Performance overhead

---

## 🧵 What is Multitasking?

1️⃣ Process-based multitasking  
2️⃣ Thread-based multitasking (Java uses this)

---

## ⚠️ Problems in Multithreading

- Race condition
- Data inconsistency
- Deadlock
- Starvation

These will be covered in upcoming days.

---

## 🏗 Why Multithreading Matters (Backend View)

Used in:

- Web servers
- Database operations
- API handling
- Microservices
- Background tasks
- Parallel processing

Example:
One server handling 1000 users → Uses threads.

---

## 📁 Folder Structure

Day-22-Multithreading-Basics/  
│  
├── README.md  
├── notes.md  
├── ThreadUsingClass.java  
├── ThreadUsingRunnable.java  
└── ThreadMethodsDemo.java

---

## 🎯 Interview Questions

Be ready to answer:

- Difference between process and thread?
- Difference between start() and run()?
- Why Runnable is preferred?
- What is thread lifecycle?
- What is context switching?
- What happens if we call run() directly?
- Can we start thread twice?
- What is daemon thread?

---

## 🚀 What’s Coming Next?

- Synchronization
- Race Conditions
- wait() / notify()
- Deadlocks
- Executor Framework
- Thread Pools

This is where:

Java Developer → Backend Engineer transition begins

---

<div align="center">

### 💬 “Concurrency is not about speed.

### It’s about structure, scalability, and smart resource usage.”

[➡️ Go to Day 23](../Day-23/README.md)

</div>

---
