<div align="center">

# 📅 Day 20 – Exception Handling

## 🎉 Welcome to Phase 4 – Writing Safer & Production-Ready Java

<img src="https://img.shields.io/badge/Day-30-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Topic-Exception%20Handling-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Phase-4-purple?style=for-the-badge" />
<img src="https://img.shields.io/badge/Level-Interview%20%2B%20Backend-orange?style=for-the-badge" />

</div>

---

## 🚀 Phase 4 Begins

If Phase 1 was **Java Basics**  
If Phase 2 was **OOP Mastery**  
If Phase 3 was **Collections & Core APIs**

👉 **Phase 4 is about writing safe, robust, and production-ready code.**

Welcome to the phase where your code:

- Doesn’t crash unexpectedly
- Handles real-world failures
- Becomes backend-ready
- Looks like professional Java

---

## 🎯 Goal of Day 30

- Understand what exceptions are
- Learn checked vs unchecked exceptions
- Master try-catch-finally
- Use throw and throws properly
- Create custom exceptions
- Understand interview edge cases
- Write defensive code

---

## 🧠 What is Exception Handling?

Exception Handling is a mechanism to:

Detect → Handle → Recover → Continue execution

Without it:

Program crashes

With it:

Program handles error gracefully

---

## 📦 Types of Exceptions

### 1️⃣ Checked Exceptions

- Checked at compile time
- Must be handled or declared

Examples:

- IOException
- SQLException
- FileNotFoundException

---

### 2️⃣ Unchecked Exceptions

- Occur at runtime
- Not mandatory to handle

Examples:

- NullPointerException
- ArithmeticException
- ArrayIndexOutOfBoundsException

---

### 3️⃣ Errors

- Serious system failures
- Should not be handled

Example:

- OutOfMemoryError
- StackOverflowError

---

## 🔧 Core Keywords

try → Block that may cause exception
catch → Handles the exception
finally → Always executes
throw → Manually throw exception
throws → Declare exception

---

## 🛠 Exception Handling Flow

try {
risky code
}
catch (Exception e) {
handle error
}
finally {
cleanup code
}

---

## 💡 Why Exception Handling Matters (Backend View)

In real-world backend systems:

- Database may fail
- File may not exist
- API may timeout
- User may enter invalid input

Without exception handling:
→ System crashes

With exception handling:
→ System responds gracefully

---

## 🧱 Custom Exceptions

You can create your own exception:

class InvalidAgeException extends Exception

Used when:

- Business rules are violated
- Domain-specific validation fails

Example:

- InvalidTransactionException
- InsufficientBalanceException

This is **interview gold**.

---

## ⚡ Interview Questions You Must Answer

- Difference between throw and throws?
- Difference between checked and unchecked?
- Can we have multiple catch blocks?
- What is multi-catch?
- Does finally always execute?
- What happens if exception is not handled?
- Can we override method and throw broader exception?
- What is try-with-resources?
- Why RuntimeException exists?

If you can answer these confidently →  
You are Phase 4 ready.

---

## 📁 Folder Structure

Day-20-Exception-Handling/  
│  
├── README.md  
├── notes.md  
├── BasicExceptionDemo.java  
├── CustomExceptionDemo.java  
└── TryWithResourcesDemo.java

---

## 🔥 Phase 4 Vision

Phase 4 will focus on:

- Exception Handling
- File Handling
- Multithreading Basics
- Java 8 Features
- Streams API
- Functional Interfaces
- Backend Thinking

This is where:

Student → Developer transition begins

---

## 🧠 System Design Angle

Exception handling helps in:

- Logging strategy
- Error codes
- API response design
- Service resilience
- Clean architecture

Real developers don’t just write code.

They handle failure properly.

---

## 🎉 Congratulations

You completed:

- 30 Days of Consistency
- 3 Strong Phases
- Core Java Foundation

Now entering:

# 🚀 Phase 4 – Advanced Java & Backend Thinking

---

<div align="center">

### 💬 “Strong developers are not those who avoid errors…

### but those who handle them intelligently.”

</div>

---
