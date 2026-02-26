# Day 16 – List & Set Interfaces (Use-Case Based Interview Notes)

---

## What is List?

List is an ordered collection that:

- Allows duplicates
- Maintains insertion order
- Supports index-based access
- Stores elements based on position

Available in:  
java.util.List

---

## List Implementations

### ArrayList

Data structure: Dynamic Array

Characteristics:

- Fast random access → O(1)
- Slow insertion/deletion in middle → O(n)
- Memory efficient
- Most commonly used

Best use-cases:

- Frequent read operations
- Storing API response data
- Iteration-heavy operations

---

### LinkedList

Data structure: Doubly Linked List

Characteristics:

- Fast insertion/deletion → O(1)
- Slow random access → O(n)
- More memory consumption
- Not cache friendly

Best use-cases:

- Frequent add/remove operations
- Queue & stack implementation
- Real-time data manipulation

---

## ArrayList vs LinkedList (Interview Decision Table)

Read-heavy application → ArrayList  
Write-heavy application → LinkedList

Frequent searching → ArrayList  
Frequent insertion/deletion → LinkedList

Memory-sensitive → ArrayList  
Data modification in middle → LinkedList

---

## What is Set?

Set is a collection that:

- Does not allow duplicates
- Is not index-based
- Stores unique elements
- Uses hashing or tree structure internally

Available in:  
java.util.Set

---

## Set Implementations

### HashSet

Data structure: Hash table

Characteristics:

- No order maintained
- One null allowed
- O(1) average time complexity
- Uses HashMap internally

Best use-cases:

- Removing duplicates
- Fast searching
- Unique elements storage

---

### LinkedHashSet

Data structure: Hash table + Linked list

Characteristics:

- Maintains insertion order
- Slightly slower than HashSet
- Unique elements

Best use-cases:

- Unique + ordered data

---

### TreeSet

Data structure: Red-Black Tree

Characteristics:

- Sorted data
- No null allowed
- O(log n)
- Natural ordering

Best use-cases:

- Sorted unique data
- Ranking systems
- Leaderboards

---

## List vs Set (Core Interview Difference)

List:

- Allows duplicates
- Maintains order
- Index-based
- get(index) possible

Set:

- No duplicates
- No index
- Faster search (HashSet)
- Used for uniqueness

---

## Performance Comparison

ArrayList:

- get() → O(1)
- add() → O(1) amortized
- remove() → O(n)

LinkedList:

- add/remove → O(1)
- get() → O(n)

HashSet:

- add/search/remove → O(1)

TreeSet:

- add/search/remove → O(log n)

---

## How to Remove Duplicates from List

Using Set:

List → HashSet → List

Reason:

Set stores only unique elements

---

## Real-World Backend Use-Cases

### Use ArrayList

- Fetching user list from database
- Storing product catalog
- Iterating response data

### Use LinkedList

- Implementing queue in messaging system
- Real-time insertion operations

### Use HashSet

- Storing unique user IDs
- Preventing duplicate entries
- Tag or keyword storage

### Use LinkedHashSet

- Maintaining unique search history

### Use TreeSet

- Sorted leaderboard
- Auto-sorted reports
- Range-based data

---

## Internal Working Insight (Interview Angle)

HashSet uses:

HashMap internally

Value stored as:

PRESENT (dummy object)

So:

HashSet = HashMap + uniqueness logic

---

## Sorting Behavior

List:

Collections.sort(list)

Set:

TreeSet → Auto sorted

---

## Null Handling

ArrayList → Allows multiple nulls  
LinkedList → Allows nulls

HashSet → One null  
LinkedHashSet → One null  
TreeSet → No null

---

## Thread Safety

None of these are synchronized by default.

To make synchronized:

Collections.synchronizedList()  
Collections.synchronizedSet()

---

## Common Interview Questions

### Easy

Difference between List and Set?  
Can List contain duplicates?  
Which Set maintains insertion order?

### Medium

ArrayList vs LinkedList?  
HashSet vs TreeSet?  
How to remove duplicates from List?

### Hard

How HashSet works internally?  
Why TreeSet does not allow null?  
Why Set is faster than List for searching?

---

## One-Line Decision Making (Interview Revision)

Need ordered data → List

Need unique data → Set

Need fast search → HashSet

Need sorted unique data → TreeSet

Need frequent read → ArrayList

Need frequent modification → LinkedList

---

## Common Mistakes

- Using ArrayList for frequent insertion
- Expecting order in HashSet
- Using TreeSet for null values
- Using List when uniqueness is required

---

## Coding Perspective (Selection Logic)

If duplicates allowed → List

If duplicates not allowed → Set

If sorting required → TreeSet

If fastest performance → HashSet

---

## Interview Summary

List → Ordered + Duplicates

Set → Unique + Fast search

ArrayList → Read heavy

LinkedList → Write heavy

HashSet → Fastest unique storage

TreeSet → Sorted unique storage

Choosing the correct collection based on use-case is a **top interview evaluation point**.

---
