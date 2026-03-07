# Day 23 – Synchronization & Concurrency (Interview Notes)

---

## What is Concurrency?

Concurrency means **multiple threads executing tasks in overlapping time periods**.

It does not always mean true parallel execution. Instead, the CPU **switches between threads quickly** so they appear to run simultaneously.

Example:

Thread 1 → Processing user request
Thread 2 → Writing log file
Thread 3 → Updating database

All tasks progress together.

---

## Why Concurrency is Needed

Modern applications must handle multiple tasks simultaneously.

Common examples:

- Web servers handling many users
- Backend APIs processing requests
- File downloading while user browsing
- Database queries running concurrently

Concurrency improves:

- CPU utilization
- Application responsiveness
- System scalability

---

## What is a Race Condition?

A **race condition** occurs when multiple threads access and modify the same shared data at the same time.

Example:

Initial Balance = 1000

Thread 1 withdraws 200  
Thread 2 withdraws 300

Execution order:

Thread1 reads balance → 1000
Thread2 reads balance → 1000
Thread1 updates → 800
Thread2 updates → 700

Correct result should be:

1000 - 200 - 300 = 500

But due to race condition the result becomes incorrect.

---

## What is a Critical Section?

A **critical section** is a part of code where **shared resources are accessed**.

Example:

balance = balance - amount

If multiple threads execute this simultaneously, data corruption may occur.

Therefore the critical section must be **protected**.

---

## What is Synchronization?

Synchronization is a mechanism that ensures **only one thread accesses a critical section at a time**.

It prevents:

- Race conditions
- Data inconsistency
- Thread interference

Basic idea:

Thread acquires lock
Execute critical section
Thread releases lock

Other threads must wait until the lock is released.

---

## Java Synchronization Mechanism

Java uses **monitor locks**.

Each object in Java has an **intrinsic lock (monitor)**.

When a thread enters a synchronized block:

- It acquires the object's lock
- Other threads must wait

---

## Synchronized Method

A method can be synchronized so that only one thread executes it at a time.

Example:

class Counter {

int count = 0;

synchronized void increment() {
count++;
}

}

Explanation:

- When a thread enters `increment()`
- It locks the object
- Other threads wait until the method finishes

---

## Synchronized Block

Instead of locking the entire method, we can lock **only the critical section**.

Example:

class Counter {

int count = 0;

void increment() {
synchronized(this) {
count++;
}
}

}

Advantages:

- Better performance
- Smaller locked region
- More control

---

## Object Level Lock

Synchronization works on **object-level locks**.

Example:

Counter c1 = new Counter();
Counter c2 = new Counter();

Two threads accessing:

c1.increment()
c2.increment()

Both can run simultaneously because they use **different locks**.

---

## Class Level Lock

Static synchronized methods lock the **class object**.

Example:

class Counter {

static int count = 0;

synchronized static void increment() {
count++;
}

}

Here lock belongs to the **class**, not object.

---

## Thread Safety

A class is **thread-safe** when multiple threads can use it **without causing incorrect results**.

Example:

Thread-safe operations:

- Atomic operations
- Synchronized methods
- Immutable objects

---

## Common Concurrency Problems

### Race Condition

Multiple threads modifying shared data.

### Deadlock

Two threads waiting for each other’s lock.

Example:

Thread A holds Lock1 and waits for Lock2
Thread B holds Lock2 and waits for Lock1

Both threads get stuck forever.

### Starvation

A thread never gets CPU time because other threads dominate resources.

### Thread Interference

Multiple threads interfere with shared variable updates.

---

## Performance Considerations

Synchronization provides safety but can reduce performance.

Reasons:

- Lock acquisition overhead
- Thread waiting time
- Context switching

Best practice:

- Synchronize only critical sections
- Avoid unnecessary locking

---

## Real World Example

Bank account system:

Deposit()
Withdraw()
CheckBalance()

Multiple users may access same account.

Without synchronization:

- Balance may become incorrect.

With synchronization:

- Operations execute safely.

---

## Interview Quick Questions

What is concurrency in Java?  
What is synchronization?  
What is race condition?  
What is critical section?  
Difference between synchronized method and block?  
What is object level locking?  
What is class level locking?  
What is thread safety?  
What is deadlock?

---

## Key Points to Remember

- Concurrency allows multiple tasks simultaneously
- Shared resources cause race conditions
- Synchronization prevents data corruption
- `synchronized` ensures mutual exclusion
- Locks control thread access
- Proper synchronization is essential for thread-safe applications

---

## Day 23 Summary

- Concurrency allows multiple threads to run
- Shared memory introduces risks
- Race conditions cause incorrect results
- Synchronization protects critical sections
- Java uses intrinsic locks for thread safety
