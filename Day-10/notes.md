# Day 10 – Control Statements (Logic Building)

---

## What are Control Statements?

Control statements change the normal flow of execution in a program.

By default:
Program executes line by line (top to bottom).

Control statements allow:

- Decision making
- Repetition
- Skipping statements
- Terminating loops

They are the foundation of logic building.

---

# 1️⃣ Decision-Making Statements

Used when program must choose between options.

---

## if Statement

Syntax:

if (condition) {
// code
}

If condition is true → block executes  
If false → skipped

---

## if-else Statement

if (condition) {
// true block
} else {
// false block
}

Used when exactly two outcomes exist.

---

## else-if Ladder

if (condition1) {
}
else if (condition2) {
}
else {
}

Used when multiple conditions exist.

Important:
Only the first true condition executes.

---

## Nested if

if (condition1) {
if (condition2) {
}
}

Used for multi-level decision making.

---

## switch Statement

Used when comparing a variable against multiple constant values.

Syntax:

switch(expression) {
case value1:
break;
case value2:
break;
default:
}

Works with:

- byte
- short
- int
- char
- String (Java 7+)
- enum

Important:
Without break → fall-through occurs.

---

# 2️⃣ Looping Statements

Loops are used to execute a block multiple times.

---

## for Loop

Used when number of iterations is known.

Syntax:

for(initialization; condition; update) {
// code
}

Example:

for(int i = 1; i <= 5; i++) {
System.out.println(i);
}

---

## while Loop

Used when number of iterations is not fixed.

Syntax:

while(condition) {
// code
}

Condition checked first (entry-controlled loop).

---

## do-while Loop

Syntax:

do {
// code
} while(condition);

Executes at least once (exit-controlled loop).

---

# 3️⃣ break and continue

---

## break

- Terminates loop immediately
- Used in loops and switch

---

## continue

- Skips current iteration
- Moves control to next iteration

---

# 4️⃣ Infinite Loops

Examples:

while(true) {
}

for(;;) {
}

Infinite loops are intentional in:

- Servers
- Game loops
- Event listeners

---

# 5️⃣ Entry-Controlled vs Exit-Controlled

Entry-Controlled:

- for
- while
  Condition checked before execution

Exit-Controlled:

- do-while
  Executes at least once

---

# 6️⃣ Common Interview Differences

### if vs switch

if:

- Works with ranges
- Complex conditions allowed

switch:

- Faster for fixed constant comparisons
- Cleaner for menu-driven programs

---

### for vs while

for:

- When iteration count known

while:

- When condition-based repetition needed

---

# 7️⃣ Output-Based Questions

Example 1:

int x = 5;

if (x > 2)
if (x < 10)
System.out.println("A");
else
System.out.println("B");

Output:
A

Reason:
else attaches to nearest if.

---

Example 2:

for(int i = 1; i <= 3; i++);
{
System.out.println("Hello");
}

Output:
Hello (only once)

Reason:
Semicolon ends loop.

---

Example 3:

int i = 1;
while(i <= 3) {
System.out.println(i);
i++;
}

Output:
1 2 3

---

# 8️⃣ Nested Loops (Logic Building Core)

Used for:

- Pattern printing
- Matrix problems
- Combinations

Structure:

for(...) {
for(...) {
}
}

Time Complexity:
Outer × Inner

---

# 9️⃣ Common Logical Mistakes

- Missing break in switch
- Infinite loop due to wrong condition
- Using = instead of ==
- Wrong loop boundaries
- Off-by-one errors

---

# 🔟 Best Practices

- Keep conditions simple
- Avoid deep nesting (reduce complexity)
- Use meaningful variable names
- Always dry-run your loop
- Check loop boundary carefully

---

# 1️⃣1️⃣ Dry Run Method (Very Important)

To solve logic problems:

Step 1: Write initial values  
Step 2: Check condition  
Step 3: Execute body  
Step 4: Update variable  
Step 5: Repeat

Dry running improves logic clarity.

---

# 1️⃣2️⃣ Quick Revision

- if → decision making
- switch → multiple fixed values
- for → fixed iterations
- while → condition-based loop
- do-while → executes at least once
- break → exit loop
- continue → skip iteration
- Nested loops → pattern & matrix logic

---

# Interview Readiness Checklist

You should confidently explain:

- Difference between if and switch
- Entry vs exit controlled loops
- How break works
- What causes infinite loop
- How nested loops increase time complexity
- Why semicolon after for loop is dangerous

---

# Day 10 Summary

Control statements build logic.

Without control flow:
Programs cannot make decisions.

Strong logic skills come from:

- Writing loops
- Solving pattern problems
- Dry-running code
- Practicing edge cases

Control statements are the base of:

- DSA
- Competitive coding
- Backend logic
- Real-world applications

---
