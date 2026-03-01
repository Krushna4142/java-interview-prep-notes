<div align="center">

# 📅 Day 19 – Collections Framework Cheat Sheet

### Mastering Java Collections for Interviews & Real-World Projects

<img src="https://img.shields.io/badge/Day-19-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Topic-Collections%20Framework-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Level-Interview%20Focused-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />

</div>

---

## 🔗 Quick Navigation

- [🎯 Goal of the Day](#-goal-of-the-day)
- [🧠 What This Cheat Sheet Covers](#-what-this-cheat-sheet-covers)
- [📦 Core Interfaces Overview](#-core-interfaces-overview)
- [📚 List Implementations](#-list-implementations)
- [🔁 Set Implementations](#-set-implementations)
- [🗂️ Map Implementations](#️-map-implementations)
- [⚙️ Queue & Deque](#️-queue--deque)
- [🚀 When to Use What? (Decision Guide)](#-when-to-use-what-decision-guide)
- [🎯 Interview Rapid Fire](#-interview-rapid-fire)
- [⏭️ What’s Next?](#️-whats-next)

---

## 🎯 Goal of the Day

The goal of **Day 19** is to build a **quick-reference collections cheat sheet** that helps you:

- Revise faster before interviews
- Choose correct data structure in projects
- Understand internal behavior
- Avoid common mistakes

This is your **Collections revision blueprint**.

---

## 🧠 What This Cheat Sheet Covers

- List vs Set vs Map vs Queue
- Internal data structure
- Ordering behavior
- Duplicate rules
- Null handling
- Time complexity
- Best use case
- Interview traps

Everything summarized in one place.

---

## 📦 Core Interfaces Overview

Collection (root interface)
│
├── List
├── Set
└── Queue

Map (separate hierarchy)

---

## 📚 List Implementations

| Implementation | Ordering        | Duplicates | Null Allowed | Internal DS        | Best Use Case          |
| -------------- | --------------- | ---------- | ------------ | ------------------ | ---------------------- |
| ArrayList      | Maintains order | Yes        | Yes          | Dynamic Array      | Fast random access     |
| LinkedList     | Maintains order | Yes        | Yes          | Doubly Linked List | Frequent insert/delete |
| Vector         | Maintains order | Yes        | Yes          | Dynamic Array      | Legacy synchronized    |
| Stack          | LIFO            | Yes        | Yes          | Extends Vector     | Stack operations       |

### 🔥 Quick Rule:

- Need fast read → ArrayList
- Need frequent insert/delete → LinkedList

---

## 🔁 Set Implementations

| Implementation | Ordering        | Duplicates | Null     | Internal DS        | Best Use Case      |
| -------------- | --------------- | ---------- | -------- | ------------------ | ------------------ |
| HashSet        | No order        | No         | One null | HashTable          | Fast lookup        |
| LinkedHashSet  | Insertion order | No         | One null | Hash + Linked List | Maintain order     |
| TreeSet        | Sorted          | No         | No null  | Red-Black Tree     | Sorted unique data |

### 🔥 Quick Rule:

- Need uniqueness only → HashSet
- Need uniqueness + order → LinkedHashSet
- Need sorted unique → TreeSet

---

## 🗂️ Map Implementations

| Implementation | Ordering        | Null Key     | Internal DS        | Best Use Case          |
| -------------- | --------------- | ------------ | ------------------ | ---------------------- |
| HashMap        | No order        | One null key | HashTable          | Fast key-value storage |
| LinkedHashMap  | Insertion order | One null key | Hash + Linked List | Ordered map            |
| TreeMap        | Sorted by key   | No null key  | Red-Black Tree     | Sorted keys            |
| Hashtable      | No order        | No null      | HashTable          | Legacy synchronized    |

### 🔥 Quick Rule:

- Fast key-value → HashMap
- Maintain insertion order → LinkedHashMap
- Sorted keys → TreeMap

---

## ⚙️ Queue & Deque

| Implementation | Type        | Ordering       | Best Use Case     |
| -------------- | ----------- | -------------- | ----------------- |
| PriorityQueue  | Queue       | Priority-based | Task scheduling   |
| ArrayDeque     | Deque       | FIFO / LIFO    | Faster than Stack |
| LinkedList     | Queue/Deque | FIFO           | Simple queue      |

---

## 🚀 When to Use What? (Decision Guide)

If you need:

- Fast random access → ArrayList
- Fast insert/delete → LinkedList
- Unique elements → HashSet
- Sorted unique elements → TreeSet
- Fast key-value storage → HashMap
- Sorted key-value storage → TreeMap
- LIFO stack → ArrayDeque (preferred over Stack)
- Priority-based processing → PriorityQueue

---

## 🎯 Interview Rapid Fire

Be ready to answer:

- Difference between ArrayList & LinkedList?
- Why HashMap is not synchronized?
- How HashSet ensures uniqueness?
- How TreeMap sorts keys?
- Difference between fail-fast & fail-safe?
- Why is Stack considered legacy?
- What is load factor?
- What is internal structure of HashMap?

If you can answer these confidently →  
You are **Collections Interview Ready**.

---

## 🧠 Pro Tip (System Design Angle)

Collections are not just data structures.

They influence:

- Memory usage
- Performance
- Scalability
- Thread-safety decisions
- Backend architecture

Choosing wrong collection = performance issue.

---

## ⏭️ What’s Next?

<div align="center">

### 👉 **Day 20 – Generics & Type Safety**

Learn:

- Why generics were introduced
- Type safety at compile time
- Wildcards (? extends, ? super)
- Bounded types
- Interview traps

<br/>

[➡️ Continue to Day 20](../Day-20/README.md)

</div>

---
