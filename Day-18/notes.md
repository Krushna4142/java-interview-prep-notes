# Day 18 – Comparable vs Comparator (Interview Notes)

---

## Why Sorting is Important?

Sorting is required when:

- Displaying leaderboard
- Ranking students
- Sorting products by price
- Sorting employees by salary
- Maintaining sorted data in TreeSet / TreeMap

Java provides two ways to sort objects:

1. Comparable (Natural Ordering)
2. Comparator (Custom Ordering)

---

# Comparable Interface

Package:
java.lang

Method:
int compareTo(Object obj)

Purpose:
Defines natural/default sorting logic inside the class itself.

---

## How Comparable Works

Class implements Comparable interface.

Example logic:

class Student implements Comparable<Student> {

    int marks;

    public int compareTo(Student s) {
        return this.marks - s.marks;
    }

}

Sorting rule:

- Negative → current < other
- Zero → equal
- Positive → current > other

---

## Key Characteristics of Comparable

- Natural ordering
- Only one sorting logic possible
- Modifies original class
- Used by:
  - Collections.sort()
  - Arrays.sort()
  - TreeSet
  - TreeMap

---

## Comparator Interface

Package:
java.util

Method:
int compare(Object o1, Object o2)

Purpose:
Defines custom sorting logic outside the class.

---

## How Comparator Works

Separate class or lambda expression.

Example:

Comparator<Student> byMarks = (s1, s2) -> s1.marks - s2.marks;

Allows multiple sorting logics.

---

## Key Characteristics of Comparator

- Custom ordering
- Multiple sorting possible
- Does NOT modify original class
- Flexible
- Preferred in modern Java

---

# Comparable vs Comparator (Core Difference)

Comparable:

- Inside class
- Natural ordering
- compareTo()
- Single sorting logic

Comparator:

- Outside class
- Custom ordering
- compare()
- Multiple sorting logic

---

## Return Value Meaning

If:

compareTo() or compare() returns:

< 0 → first object smaller  
= 0 → equal

> 0 → first object greater

Important:

If returns 0 → TreeSet will NOT add duplicate element.

---

## TreeSet & TreeMap Internal Sorting

TreeSet and TreeMap:

- Use comparison internally
- Default → Comparable
- Custom → Comparator

If no Comparable & no Comparator → ClassCastException

---

## When to Use Comparable?

- When class has natural fixed order
- Example:
  - Integer
  - String
  - Date
  - Employee sorted by ID (default)

---

## When to Use Comparator?

- Multiple sorting required
- Sorting based on different fields
- Sorting without modifying original class
- Example:
  - Sort employee by salary
  - Sort employee by name
  - Sort employee by experience

---

## Multiple Field Sorting (Interview Level)

Primary sort by salary  
If equal → sort by name

Logic:

if (salary != other.salary)
return salary difference
else
return name comparison

---

## Modern Java (Java 8+)

Using Lambda:

Collections.sort(list, (a, b) -> a.age - b.age);

Using Comparator methods:

Comparator.comparing(Student::getMarks);

Comparator.comparing(Student::getMarks)
.thenComparing(Student::getName);

---

## Performance

Sorting complexity:

Collections.sort()

O(n log n)

Internally uses:

TimSort (Hybrid sorting algorithm)

---

## Common Interview Questions

Easy:

Difference between Comparable and Comparator?  
Which package contains Comparable?

Medium:

What happens if compareTo() returns 0?  
Can we use multiple Comparator?

Hard:

How TreeSet uses Comparable internally?  
Why Comparator is preferred in modern Java?  
What happens if compareTo() inconsistent with equals()?

---

## Important Interview Rule

compareTo() must be:

- Consistent with equals()
- Symmetric
- Transitive

Otherwise:

Unpredictable behavior in TreeSet / TreeMap.

---

## Real-World Use Cases

Comparable:

- Default ordering of entities

Comparator:

- Sorting API response
- Sorting dashboard data
- Sorting reports
- Multi-level sorting logic

---

## Common Mistakes

- Returning only 1 or -1 always
- Ignoring equals condition
- Not handling null values
- Modifying original class unnecessarily

---

## Quick Decision Guide

Need default sorting → Comparable

Need custom sorting → Comparator

Need multiple sorting → Comparator

Need sorting without modifying class → Comparator

---

## Interview Summary

Comparable → Natural order → compareTo() → Single logic

Comparator → Custom order → compare() → Multiple logic

TreeSet & TreeMap depend on comparison

Sorting complexity → O(n log n)

Comparator is more flexible and widely used in real-world projects.

---

## Final Takeaway

Understanding Comparable & Comparator means:

- Strong Collection knowledge
- Strong OOP knowledge
- Better coding round performance
- Better backend decision-making ability

Sorting is not just syntax —  
it reflects design thinking.

---
