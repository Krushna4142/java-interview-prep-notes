# 📚 Day 22 – Multithreading Basics (Complete Notes)

---

# 1️⃣ What is Multithreading?

Multithreading means:

→ Executing multiple threads simultaneously  
→ Performing multiple tasks within a single process  
→ Better CPU utilization

Example:

Download file
Play music
Edit document

All running at the same time.

---

# 2️⃣ What is a Thread?

Thread is:

→ Smallest unit of execution  
→ Lightweight subprocess  
→ Part of a process

Every Java program has at least one thread:
→ main thread

---

# 3️⃣ Process vs Thread

Process:
→ Independent program
→ Separate memory
→ Heavyweight

Thread:
→ Part of process
→ Shared memory
→ Lightweight

Comparison:

Memory → Process (separate) / Thread (shared)  
Creation cost → Process (high) / Thread (low)  
Communication → Process (slow) / Thread (fast)

---

# 4️⃣ Ways to Create Thread

## ✅ Method 1: Extending Thread Class

class MyThread extends Thread {
public void run() {
System.out.println("Thread is running");
}
}

public class Demo {
public static void main(String[] args) {
MyThread t1 = new MyThread();
t1.start();
}
}

Limitation:
→ Cannot extend another class (Java does not support multiple inheritance)

---

## ✅ Method 2: Implementing Runnable (Recommended)

class MyRunnable implements Runnable {
public void run() {
System.out.println("Thread is running");
}
}

public class Demo {
public static void main(String[] args) {
Thread t1 = new Thread(new MyRunnable());
t1.start();
}
}

Advantages:
✔ Supports multiple inheritance  
✔ Cleaner design  
✔ Industry standard

---

# 5️⃣ start() vs run()

t1.start(); → Creates new thread and calls run()
t1.run(); → Normal method call (no new thread)

Important:
Always call start().

---

# 6️⃣ Thread Lifecycle

New

Runnable

Running

Blocked / Waiting

Terminated

Explanation:

New → Thread object created  
Runnable → Ready to run  
Running → CPU executing  
Blocked → Waiting for resource  
Terminated → Execution finished

---

# 7️⃣ Thread Methods

start()  
run()  
sleep(ms)  
join()  
setPriority(int)  
getPriority()  
currentThread()  
isAlive()

---

## sleep()

Pauses thread for given milliseconds.

Thread.sleep(1000);

Throws:
InterruptedException (checked)

---

## join()

Waits for another thread to finish.

t1.join();

Used when:
→ One thread depends on another

---

# 8️⃣ Thread Priority

Range:
1 (MIN_PRIORITY)  
5 (NORM_PRIORITY – default)  
10 (MAX_PRIORITY)

t1.setPriority(Thread.MAX_PRIORITY);

Note:
Priority does NOT guarantee execution order.

---

# 9️⃣ currentThread()

Returns reference of currently executing thread.

System.out.println(Thread.currentThread().getName());

---

# 🔟 isAlive()

Checks whether thread is still running.

t1.isAlive();

Returns:
true / false

---

# 1️⃣1️⃣ What is Context Switching?

When CPU switches between threads.

Managed by:
→ Thread Scheduler (JVM + OS)

Too many threads:
→ High overhead  
→ Performance drop

---

# 1️⃣2️⃣ Main Thread

Every Java application starts with:

public static void main(String[] args)

This is executed by:
→ Main Thread

You can verify:

System.out.println(Thread.currentThread().getName());

Output:
main

---

# 1️⃣3️⃣ Multitasking Types

1. Process-based multitasking
2. Thread-based multitasking (Java uses this)

---

# 1️⃣4️⃣ Common Multithreading Problems

Race Condition  
Deadlock  
Starvation  
Thread interference  
Data inconsistency

These occur due to:
→ Shared memory access

Will be solved using:
→ Synchronization  
→ Locks  
→ wait() / notify()

---

# 1️⃣5️⃣ Real-World Usage

Used in:

✔ Web servers  
✔ Backend APIs  
✔ Parallel processing  
✔ Gaming  
✔ Banking systems  
✔ Microservices

Example:
One server handling 1000 users → Uses threads internally.

---

# 1️⃣6️⃣ Important Interview Questions

Q: Difference between process and thread?  
Q: Difference between start() and run()?  
Q: Why Runnable is preferred?  
Q: What is thread lifecycle?  
Q: What is context switching?  
Q: Can we start thread twice?

Answer:
No. Starting thread twice throws IllegalThreadStateException.

---

# 1️⃣7️⃣ Key Rules to Remember

✔ Always call start()  
✔ Runnable preferred over Thread class  
✔ Threads share memory  
✔ Be careful with shared data  
✔ Too many threads reduce performance

---

# 🚀 Summary

Multithreading allows:

→ Parallel task execution  
→ Better CPU usage  
→ Faster backend systems  
→ Scalable applications

This is foundation for:

✔ Synchronization  
✔ Thread pools  
✔ Executor framework  
✔ High-performance backend systems

Master this → You are entering real backend engineering.
