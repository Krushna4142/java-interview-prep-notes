<div align="center">

# 📅 Day 18 – Comparable vs Comparator

### Sorting Mechanisms & Custom Ordering in Java

<img src="https://img.shields.io/badge/Day-18-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Difficulty-Medium--High-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Focus-Comparable%20vs%20Comparator-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />

</div>

---

## 🔗 Quick Navigation

- [🎯 Goal of the Day](#-goal-of-the-day)
- [🧠 What You’ll Learn](#-what-youll-learn)
- [📌 Why This Topic Matters](#-why-this-topic-matters)
- [📁 Folder Structure](#-folder-structure)
- [⚙️ Comparable vs Comparator – Core Difference](#️-comparable-vs-comparator--core-difference)
- [🎯 Interview Preparation](#-interview-preparation-day-18)
- [⏭️ What’s Next?](#️-whats-next)

---

## 🎯 Goal of the Day

The goal of **Day 18** is to understand:

- How sorting works in Java
- Natural ordering vs Custom ordering
- Comparable interface
- Comparator interface
- Real-world sorting decisions
- Interview-level sorting clarity

This topic is frequently asked in **collections + OOP interviews**.

---

## 🧠 What You’ll Learn

By the end of this day, you will clearly understand:

- What is natural ordering
- What is custom ordering
- Comparable interface working
- Comparator interface working
- compareTo() vs compare()
- When to use which
- How TreeSet and TreeMap use comparison internally

📌 Deep explanations are available in **notes.md**.

---

## 📌 Why This Topic Matters

Comparable & Comparator are asked in:

- Java interviews
- Collection-based questions
- TreeSet / TreeMap questions
- Coding rounds (sorting custom objects)
- Backend project discussions

Interviewers test:

- Your OOP understanding
- Your sorting logic
- Your interface knowledge
- Your problem-solving clarity

This is a **decision-based topic**.

---

## 📁 Folder Structure

Day-18-Comparable-Comparator/  
│  
├── README.md → Overview & interview focus  
└── notes.md → Detailed sorting explanations

---

## ⚙️ Comparable vs Comparator – Core Difference

Comparable:

- Present inside java.lang package
- Used for natural ordering
- compareTo() method
- Class must implement it

Comparator:

- Present inside java.util package
- Used for custom ordering
- compare() method
- Separate class or lambda implementation

Key idea:

Comparable → Default sorting  
Comparator → Flexible sorting

---

## 🎯 Interview Preparation (Day 18)

You should be able to answer:

- Difference between Comparable and Comparator?
- What is natural ordering?
- How TreeSet sorts elements?
- Can we use multiple sorting logic?
- What happens if compareTo() returns 0?
- Why Comparator is preferred in modern Java?
- How to sort based on multiple fields?

All answers structured in **notes.md**.

---

## 🔗 Helpful References

- https://docs.oracle.com/javase/8/docs/api/java/lang/Comparable.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html
- https://www.baeldung.com/java-comparator-comparable

---

## ⏭️ What’s Next?

<div align="center">

### 👉 **Day 19 – Exception Handling & Custom Exceptions**

Learn about:

- try-catch-finally
- Checked vs Unchecked exceptions
- Custom exception creation
- Best practices
- Interview edge cases

<br/>

[➡️ Go to Day 19](../Day-19/README.md)

</div>

---
