# Day 15 – Java Collections Overview (Interview Notes)

---

## What is Java Collections Framework?

Java Collections Framework (JCF) is a unified architecture used to store, manipulate, and process groups of objects dynamically.

It provides:

- Ready-made data structures
- Algorithms for searching & sorting
- Performance optimization
- Type safety using generics

It is present in:  
java.util package

---

## Why Collections Are Needed?

Problems with Arrays:

- Fixed size
- No built-in methods
- Cannot store heterogeneous objects efficiently
- Memory wastage or overflow

Collections solve these by:

- Dynamic resizing
- Rich API support
- Better performance handling
- Standardized data structures

---

## Core Interfaces of Collection Framework

### 1. Iterable (Root Interface)

- Root of the collection hierarchy
- Provides iterator()

### 2. Collection

Parent interface of:

- List
- Set
- Queue

Common methods:

- add()
- remove()
- size()
- contains()
- isEmpty()
- clear()

---

## Important Note

Map is **NOT** part of Collection hierarchy.

Because:

- Collection stores individual elements
- Map stores key-value pairs

---

## Collection Hierarchy

Iterable  
 ↓  
Collection  
 ├── List  
 │ ├── ArrayList  
 │ ├── LinkedList  
 │ └── Vector  
 │  
 ├── Set  
 │ ├── HashSet  
 │ ├── LinkedHashSet  
 │ └── TreeSet  
 │  
 └── Queue  
 ├── PriorityQueue  
 └── ArrayDeque

Separate hierarchy:

Map  
 ├── HashMap  
 ├── LinkedHashMap  
 ├── TreeMap  
 └── Hashtable

---

## List Interface

Characteristics:

- Ordered collection
- Allows duplicates
- Index-based access
- Preserves insertion order

### ArrayList

- Dynamic array
- Fast random access
- Slow insertion/deletion in middle

### LinkedList

- Doubly linked list
- Fast insertion/deletion
- Slow random access

---

## ArrayList vs LinkedList (Interview Point)

ArrayList:

- Uses dynamic array
- Better for searching
- More cache friendly

LinkedList:

- Uses nodes
- Better for frequent insertion/deletion
- More memory consumption

---

## Set Interface

Characteristics:

- Does not allow duplicates
- Not index-based
- Used for unique elements

### HashSet

- Uses hashing
- No order
- Allows one null

### LinkedHashSet

- Maintains insertion order

### TreeSet

- Sorted data
- No null
- Uses Red-Black Tree
- O(log n)

---

## Queue Interface

Used for:

- Processing elements in order

Types:

### PriorityQueue

- Elements processed based on priority
- Natural sorting order

### ArrayDeque

- Faster than stack
- Used for queue + stack operations

---

## Map Interface

Stores:

Key → Value pairs

Key points:

- Key must be unique
- Value can be duplicate

---

### HashMap

- No order
- One null key allowed
- Multiple null values allowed
- O(1) average

### LinkedHashMap

- Maintains insertion order

### TreeMap

- Sorted by keys
- No null key
- O(log n)

### Hashtable

- Thread-safe
- No null key/value
- Legacy class

---

## HashMap Internal Working (Basic Interview Level)

Hashing process:

1. hashCode() → generates hash
2. Index calculation
3. Bucket storage
4. equals() for collision handling

Java 8:

- Converts bucket to balanced tree after threshold

---

## Performance Comparison

ArrayList:

- get() → O(1)
- add() → O(1) (amortized)

LinkedList:

- add/remove → O(1)
- get() → O(n)

HashSet:

- add/search → O(1)

TreeSet:

- add/search → O(log n)

HashMap:

- put/get → O(1) average

TreeMap:

- put/get → O(log n)

---

## When to Use What?

Use ArrayList:

- Frequent read operations

Use LinkedList:

- Frequent insert/delete

Use HashSet:

- Unique elements
- Fast performance

Use TreeSet:

- Sorted unique data

Use HashMap:

- Fast key-value storage

Use TreeMap:

- Sorted key-value storage

---

## Generics in Collections

Provides:

- Compile-time type safety
- No need for type casting

Example:

List<String> list = new ArrayList<>();

---

## Iteration Techniques

- for-each loop
- Iterator
- ListIterator
- forEach() method

---

## Common Interview Questions

### Easy

What is Collection framework?  
Difference between List and Set?  
Difference between ArrayList and LinkedList?

### Medium

Difference between HashMap and Hashtable?  
Difference between HashSet and TreeSet?  
Why Map is not part of Collection?

### Hard

How HashMap works internally?  
What is load factor?  
What is fail-fast iterator?  
How ConcurrentHashMap works? (conceptual)

---

## One-Line Interview Revision

ArrayList → Fast access  
LinkedList → Fast modification  
HashSet → Unique + Fast  
TreeSet → Sorted + Unique  
HashMap → Fast key-value  
TreeMap → Sorted key-value

---

## Common Mistakes

- Using ArrayList for frequent insertion
- Expecting order in HashSet
- Using HashMap in multi-threaded environment
- Forgetting equals() and hashCode()

---

## Real-World Use Cases

ArrayList:

- Storing API response list

HashSet:

- Removing duplicates

HashMap:

- Caching
- Database mapping
- Frequency counting

TreeMap:

- Leaderboards
- Sorted reports

---

## Interview Summary

- Collection stores objects dynamically
- List → ordered
- Set → unique
- Queue → processing order
- Map → key-value
- HashMap is most important for interviews

This topic is:

Core Java + Coding Round + System Design foundation.

---
