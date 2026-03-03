<div align="center">

# 📅 Day 21 – Checked vs Unchecked Exceptions

### Understanding Compile-Time Safety vs Runtime Failures

<img src="https://img.shields.io/badge/Day-21-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Topic-Exceptions-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Focus-Interview%20Concepts-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />

</div>

---

## 🎯 Goal of the Day

Today’s objective is to clearly understand:

- What are Checked Exceptions?
- What are Unchecked Exceptions?
- Key differences between them
- When to use which
- Interview-level edge cases
- Backend real-world impact

This is one of the **most asked Java interview concepts**.

---

## 🧠 Exception Hierarchy Refresher

Object
└── Throwable
├── Error
└── Exception
├── Checked Exceptions
└── RuntimeException (Unchecked Exceptions)

---

## ✅ Checked Exceptions

### Definition

- Checked at compile time
- Must be handled using try-catch OR declared using throws

### Examples

- IOException
- SQLException
- FileNotFoundException
- ClassNotFoundException

### Rule

If a method throws a checked exception:

→ You MUST handle it  
OR  
→ You MUST declare it using `throws`

---

## 🔥 Why Checked Exceptions Exist?

To force developers to:

- Handle external failures
- Handle file/database/network operations
- Write safer code

These are usually **recoverable conditions**.

---

## ❌ Unchecked Exceptions (RuntimeException)

### Definition

- Occur at runtime
- Not mandatory to handle

### Examples

- NullPointerException
- ArithmeticException
- ArrayIndexOutOfBoundsException
- IllegalArgumentException

### Why Not Checked?

Because they usually occur due to:

→ Programming mistakes  
→ Bad logic  
→ Incorrect assumptions

---

## 🆚 Checked vs Unchecked – Direct Comparison

| Feature            | Checked           | Unchecked            |
| ------------------ | ----------------- | -------------------- |
| Checked at         | Compile time      | Runtime              |
| Must Handle?       | Yes               | No                   |
| Inherits From      | Exception         | RuntimeException     |
| Caused By          | External failures | Programming errors   |
| Compiler Enforces? | Yes               | No                   |
| Example            | IOException       | NullPointerException |

---

## 💡 Real-World Backend Perspective

Checked Exceptions:

- File reading failure
- Database connectivity issues
- API timeouts

Unchecked Exceptions:

- Null pointer due to bad coding
- Invalid argument passed
- Logic errors

---

## ⚠️ Interview Traps

Be ready to answer:

- Why Java introduced checked exceptions?
- Why RuntimeException is unchecked?
- Can we convert checked to unchecked?
- Should we make custom exceptions checked or unchecked?
- Why many modern frameworks prefer unchecked exceptions?
- Can child class throw broader exception while overriding?

---

## 🧱 Overriding Rules (Important)

If parent method throws checked exception:

Child method:
✔ Can throw same exception  
✔ Can throw narrower exception  
❌ Cannot throw broader exception

Unchecked exceptions:
✔ No restriction

---

## 🛠 When to Use What?

Use Checked Exception when:

- Error is recoverable
- Caller should handle it
- It is external system failure

Use Unchecked Exception when:

- It is programming mistake
- Invalid input
- Business validation failure

---

## 📁 Folder Structure

Day-21-Checked-vs-Unchecked/  
│  
├── README.md  
├── notes.md

---

## 🚀 Why This Concept Matters

Understanding this helps in:

- Writing production-ready backend code
- Designing APIs properly
- Avoiding poor exception design
- Clearing Java interviews confidently

---

<div align="center">

[➡️ Go to Day 22](../Day-22/README.md)

</div>

---
