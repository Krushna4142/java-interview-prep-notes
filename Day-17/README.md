<div align="center">

# 📅 Day 17 – Map Interface & Hashing Internals

### Key-Value Architecture & Internal Working

<img src="https://img.shields.io/badge/Day-17-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Difficulty-High-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Focus-Map%20%26%20Hashing-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />

</div>

---

## 🔗 Quick Navigation

- [🎯 Goal of the Day](#-goal-of-the-day)
- [🧠 What You’ll Learn](#-what-youll-learn)
- [📌 Why This Topic Matters](#-why-this-topic-matters)
- [📁 Folder Structure](#-folder-structure)
- [⚙️ Map Hierarchy Overview](#️-map-hierarchy-overview)
- [🧠 HashMap Internal Working](#-hashmap-internal-working)
- [🎯 Interview Preparation](#-interview-preparation-day-17)
- [⏭️ What’s Next?](#️-whats-next)

---

## 🎯 Goal of the Day

The goal of **Day 17** is to deeply understand:

- Map interface
- Key-value storage mechanism
- Hashing concept
- HashMap internal working
- equals() and hashCode() importance

This topic is considered **core backend foundation knowledge**.

---

## 🧠 What You’ll Learn

By the end of this day, you will clearly understand:

- Difference between Map and Collection
- HashMap vs LinkedHashMap vs TreeMap vs Hashtable
- Hashing concept
- Collision handling
- Load factor
- Rehashing
- Java 8 improvements (treeification)

📌 Detailed internal explanations available in **notes.md**.

---

## 📌 Why This Topic Matters

Map & Hashing is asked in:

- Core Java interviews
- Spring Boot interviews
- Backend system design rounds
- Coding rounds
- Performance discussions

Interviewers test:

- Your understanding of hashing
- Memory behavior
- Performance awareness
- Internal data structure knowledge

This is a **must-master topic**.

---

## 📁 Folder Structure

Day-17-Map-Hashing-Internals/  
│  
├── README.md → Overview & interview focus  
└── notes.md → Deep internal explanations

---

## ⚙️ Map Hierarchy Overview

Map (Separate hierarchy from Collection)

Implementations:

- HashMap
- LinkedHashMap
- TreeMap
- Hashtable

Key characteristics:

- Stores key-value pairs
- Keys must be unique
- Values can be duplicate
- Not index-based

---

## 🧠 HashMap Internal Working

Basic Working Steps:

1. hashCode() generates hash
2. Hash converted to index
3. Bucket selection
4. If collision → equals() check
5. Store in linked list / tree (Java 8+)

Important Concepts:

- Load Factor (default 0.75)
- Initial Capacity (default 16)
- Rehashing
- Treeification after threshold

Java 8 Improvement:

If bucket size > 8 → converts to balanced tree (Red-Black Tree)

---

## 🎯 Interview Preparation (Day 17)

You should be able to answer:

- How HashMap works internally?
- What is hashing?
- What is load factor?
- What is collision?
- Difference between HashMap and Hashtable?
- Why equals() and hashCode() must be overridden together?
- Why TreeMap does not allow null key?
- How rehashing works?

All answers structured in **notes.md**.

---

## 🔗 Helpful References

- https://docs.oracle.com/javase/8/docs/api/java/util/Map.html
- https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html
- https://www.baeldung.com/java-hashmap

---

## ⏭️ What’s Next?

<div align="center">

### 👉 **Day 18 – Generics & Comparable/Comparator**

Learn about:

- Type safety
- Generics internals
- Comparable vs Comparator
- Custom sorting
- Interview-level sorting logic

<br/>

[➡️ Go to Day 18](../Day-18/README.md)

</div>

---
