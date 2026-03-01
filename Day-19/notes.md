# 📚 Java Collections Framework – Complete Cheat Sheet (Interview Edition)

---

# 1️⃣ Collections Hierarchy

Iterable
│
Collection (root interface)
├── List
├── Set
└── Queue

Map (separate hierarchy – does NOT extend Collection)

---

# 2️⃣ Core Differences

List → Ordered, Allows duplicates
Set → Unordered (usually), No duplicates
Queue → FIFO / Priority-based
Map → Key-Value pair, Unique keys

---

# 3️⃣ LIST Cheat Sheet

## ArrayList

Internal Structure:
→ Dynamic Resizable Array

Default Capacity:
→ 10

Time Complexity:
get(index) → O(1)
add() → O(1) (amortized)
add(index) → O(n)
remove(index) → O(n)

Allows:
✔ Duplicates
✔ Multiple nulls
✔ Maintains insertion order

Best Use:
→ Frequent read operations

---

## LinkedList

Internal Structure:
→ Doubly Linked List

Time Complexity:
get(index) → O(n)
addFirst() → O(1)
addLast() → O(1)
remove() → O(1) (if reference known)

Allows:
✔ Duplicates
✔ Multiple nulls
✔ Maintains insertion order

Best Use:
→ Frequent insert/delete

---

## Vector (Legacy)

Internal:
→ Dynamic Array
→ Synchronized

Slower than ArrayList due to synchronization.

---

## Stack (Legacy)

Extends:
→ Vector

Better Alternative:
→ ArrayDeque

---

# 4️⃣ SET Cheat Sheet

## HashSet

Internal:
→ HashMap (uses keys only)

Time Complexity:
add() → O(1)
remove() → O(1)
contains()→ O(1)

Allows:
✔ One null
❌ No duplicates
❌ No ordering guarantee

Best Use:
→ Fast uniqueness checking

---

## LinkedHashSet

Internal:
→ HashMap + Linked List

Maintains:
✔ Insertion Order

Everything same as HashSet but ordered.

---

## TreeSet

Internal:
→ Red-Black Tree

Time Complexity:
add() → O(log n)
remove() → O(log n)
contains()→ O(log n)

Allows:
❌ No null
❌ No duplicates
✔ Sorted order

Sorting:
→ Natural ordering (Comparable)
→ Custom ordering (Comparator)

Best Use:
→ Sorted unique data

---

# 5️⃣ MAP Cheat Sheet

## HashMap

Internal (Java 8+):
→ Array of Node
→ LinkedList
→ Converts to Red-Black Tree if bucket > 8

Time Complexity:
put() → O(1)
get() → O(1)
remove() → O(1)

Allows:
✔ One null key
✔ Multiple null values
❌ No ordering

Default Load Factor:
→ 0.75

Default Capacity:
→ 16

---

## LinkedHashMap

Maintains:
✔ Insertion Order

Used for:
→ LRU Cache (access-order mode)

---

## TreeMap

Internal:
→ Red-Black Tree

Time Complexity:
put() → O(log n)
get() → O(log n)

Allows:
❌ No null key
✔ Sorted by keys

---

## Hashtable (Legacy)

✔ Synchronized
❌ No null key
❌ No null value

Replaced by:
→ ConcurrentHashMap (Modern)

---

# 6️⃣ QUEUE & DEQUE

## PriorityQueue

Internal:
→ Min Heap (by default)

Time Complexity:
add() → O(log n)
poll() → O(log n)

Ordering:
→ Natural or Comparator

---

## ArrayDeque

Internal:
→ Resizable Array

Faster than:
→ Stack
→ LinkedList (for queue operations)

Supports:
✔ FIFO
✔ LIFO

---

# 7️⃣ Comparable vs Comparator

Comparable:
→ Natural Ordering
→ compareTo()
→ Inside the class

Comparator:
→ Custom Ordering
→ compare()
→ Separate class / Lambda

---

# 8️⃣ Fail-Fast vs Fail-Safe

Fail-Fast:
→ Throws ConcurrentModificationException
Example:
→ ArrayList
→ HashMap

Fail-Safe:
→ Works on clone copy
Example:
→ ConcurrentHashMap
→ CopyOnWriteArrayList

---

# 9️⃣ Thread-Safety

Not Thread-Safe:
→ ArrayList
→ HashMap
→ HashSet

Thread-Safe:
→ Vector
→ Hashtable
→ ConcurrentHashMap

Better Approach:
→ Collections.synchronizedList()
→ Concurrent collections (java.util.concurrent)

---

# 🔟 Time Complexity Summary

ArrayList:
Access → O(1)
Insert → O(n)

LinkedList:
Access → O(n)
Insert → O(1)

HashSet:
Add → O(1)

TreeSet:
Add → O(log n)

HashMap:
Put/Get → O(1)

TreeMap:
Put/Get → O(log n)

PriorityQueue:
Add → O(log n)

---

# 1️⃣1️⃣ Interview Traps

Q: Why HashSet doesn’t allow duplicates?
A: Uses HashMap internally. Keys must be unique.

Q: Why TreeSet doesn’t allow null?
A: Uses comparison. null can’t be compared.

Q: Why HashMap allows one null key?
A: Special bucket for null key.

Q: What is load factor?
A: Resize trigger threshold (capacity × load factor).

Q: When does HashMap convert to Tree?
A: When bucket size > 8 (Java 8+).

---

# 1️⃣2️⃣ Decision Guide

Need Fast Read → ArrayList
Need Fast Insert/Delete → LinkedList
Need Unique → HashSet
Need Sorted Unique → TreeSet
Need Key-Value Fast → HashMap
Need Sorted Map → TreeMap
Need Thread Safe Map → ConcurrentHashMap
Need LIFO → ArrayDeque
Need Priority Processing → PriorityQueue

---

# 🚀 Final Advice

Collections choice affects:
→ Performance
→ Memory
→ Scalability
→ Thread safety
→ Backend system design

Wrong collection choice = Performance bottleneck.

Master this sheet → You are 80% ready for Java backend interviews.
