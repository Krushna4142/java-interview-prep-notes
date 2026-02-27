# Day 17 – Map Interface & Hashing Internals (Interview Notes)

---

## What is Map?

Map is a data structure that stores:

Key → Value pairs

Key points:

- Keys must be unique
- Values can be duplicate
- Not part of Collection hierarchy
- Located in java.util package

---

## Why Map is Not Part of Collection?

Collection stores individual objects.

Map stores key-value pairs.

Hence, separate hierarchy.

---

## Map Hierarchy

Map
├── HashMap
├── LinkedHashMap
├── TreeMap
└── Hashtable

---

## Hashing Concept

Hashing converts an object into a numeric value using:

hashCode()

This number determines:

- Bucket index
- Storage location

Formula (simplified):

index = hash & (n - 1)

Where:
n = capacity

---

## HashMap Internal Working (Step-by-Step)

Default values:

Initial capacity = 16  
Load factor = 0.75

When put(key, value) is called:

1. hashCode() is generated
2. Hash is processed (improved hash)
3. Index calculated
4. Check bucket
   - If empty → store
   - If collision → equals() check
5. If equals true → replace value
6. If equals false → store in linked list
7. If bucket size > 8 → convert to tree (Java 8+)

---

## What is Collision?

When two different keys generate same bucket index.

Handled using:

- Linked List (before Java 8)
- Linked List → Red-Black Tree (Java 8+)

---

## Treeification (Java 8 Feature)

If:

Bucket size > 8  
AND capacity >= 64

Then:

Linked list converts into balanced tree.

Reason:

Improve worst-case complexity from O(n) to O(log n)

---

## Load Factor

Load Factor = capacity \* loadFactor

Default = 0.75

Meaning:

When 75% capacity is filled → rehashing occurs

---

## Rehashing

When size exceeds threshold:

1. Capacity doubles
2. All elements rehashed
3. Reinserted into new buckets

Costly operation.

---

## Time Complexity

Average case:

put() → O(1)  
get() → O(1)

Worst case (before Java 8):

O(n)

Worst case (after Java 8 treeification):

O(log n)

---

## equals() and hashCode() Rule (Most Important Interview Point)

If two objects are equal using equals():

Their hashCode must be equal.

If overridden equals()  
You MUST override hashCode()

Otherwise:

- Retrieval fails
- Unexpected behavior

---

## HashMap vs LinkedHashMap

HashMap:

- No order
- Faster
- One null key allowed

LinkedHashMap:

- Maintains insertion order
- Slightly slower
- One null key allowed

---

## HashMap vs TreeMap

HashMap:

- No order
- O(1)
- Allows one null key

TreeMap:

- Sorted keys
- O(log n)
- No null key
- Uses Red-Black Tree

---

## HashMap vs Hashtable

HashMap:

- Not synchronized
- Faster
- Allows one null key
- Allows multiple null values

Hashtable:

- Thread-safe
- Slower
- No null key
- No null value
- Legacy class

---

## TreeMap Internal Working

Data structure:

Red-Black Tree

Characteristics:

- Sorted by natural order
- Can use custom Comparator
- O(log n)

Used when:

- Sorted key-value required
- Range queries required

---

## Important Methods in Map

put(K, V)  
get(K)  
remove(K)  
containsKey(K)  
containsValue(V)  
keySet()  
values()  
entrySet()

---

## Iterating Map

Using entrySet():

for (Map.Entry<K, V> entry : map.entrySet())

Using keySet():

for (K key : map.keySet())

Best practice:

Use entrySet() (more efficient)

---

## Internal Storage Structure (Simplified)

HashMap internally uses:

Node<K, V>[] table

Each bucket contains:

- Node
- Linked list
- Or TreeNode (after threshold)

---

## Null Handling

HashMap:

1 null key allowed  
Multiple null values allowed

TreeMap:

No null key

Hashtable:

No null key  
No null value

---

## Real-World Use Cases

HashMap:

- Caching
- Frequency counter
- Database row mapping
- API response mapping

LinkedHashMap:

- Maintaining order of API response

TreeMap:

- Sorted leaderboard
- Ranking systems
- Range-based filtering

Hashtable:

- Legacy systems

---

## Common Interview Questions

Easy:

What is Map?  
Why Map not part of Collection?  
Difference between HashMap and TreeMap?

Medium:

How HashMap works internally?  
What is load factor?  
What is collision?

Hard:

Explain rehashing.  
Why equals and hashCode must be overridden together?  
Explain treeification in Java 8.

---

## Quick Revision Summary

Map → Key-Value structure

HashMap → Fastest

LinkedHashMap → Ordered

TreeMap → Sorted

Hashtable → Thread-safe (legacy)

Collision → Same bucket

Load Factor → Resize threshold

Rehashing → Capacity doubling

Treeification → LinkedList → Red-Black Tree

---

## Interview-Level Answer Structure

When asked:

“How HashMap works?”

Answer structure:

- Hashing concept
- hashCode()
- Index calculation
- Bucket
- Collision handling
- Load factor
- Rehashing
- Java 8 treeification

This structure gives senior-level clarity.

---

## Final Takeaway

HashMap is one of the most important classes in Java.

Understanding its internal working:

- Improves backend logic
- Improves coding performance
- Improves interview confidence

Mastering hashing = strong Java foundation.

---
