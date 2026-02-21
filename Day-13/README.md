<div align="center">

# 🚀 Day 13 – Constructors & Keywords

<img src="https://img.shields.io/badge/Topic-Constructors%20%26%20Keywords-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Focus-Tricky%20Questions-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Language-Java-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />

---

### 🧠 Learning Objective

> Master constructor execution flow, keyword behavior, and interview-level edge cases.

</div>

---

## 📌 What I Learned Today

🔹 What is a constructor  
🔹 Default vs Parameterized constructor  
🔹 Constructor overloading  
🔹 Constructor chaining (`this()`)  
🔹 `this` keyword  
🔹 `static` keyword  
🔹 `final` keyword  
🔹 `super` keyword  
🔹 Object initialization flow

---

## 🏗️ Constructor Types

| Type                      | Purpose                            |
| ------------------------- | ---------------------------------- |
| Default Constructor       | Provided by JVM if none is written |
| Parameterized Constructor | Initialize object with values      |
| Copy Constructor (custom) | Copy data from another object      |

---

## 🔗 Constructor Chaining

````java
class Student {
    Student() {
        this(101);
        System.out.println("Default Constructor");
    }

    Student(int id) {
        System.out.println("Parameterized Constructor: " + id);
    }
}

---

## 🧠 Output:

Parameterized Constructor: 101
Default Constructor
🔑 Keywords Covered
1️⃣ this

✔ Refers to current object
✔ Calls another constructor
✔ Resolves variable shadowing

2️⃣ static

✔ Belongs to class
✔ Shared memory
✔ Static block executes first

3️⃣ final

✔ Variable → constant
✔ Method → cannot override
✔ Class → cannot inherit

4️⃣ super

✔ Calls parent constructor
✔ Access parent methods & variables

⚙️ Object Creation Flow

1️⃣ Static block
2️⃣ Instance block
3️⃣ Constructor

💻 Practice Implementations

✔ Constructor Overloading
✔ Constructor Chaining
✔ Static Variable Counter
✔ Final Keyword Example
✔ super Keyword Demo

🎯 Interview Tricky Points

❓ Can constructor be private? → ✅ Yes (Singleton)
❓ Can constructor be static? → ❌ No
❓ Can we inherit constructor? → ❌ No
❓ Can we call constructor manually? → ❌ No
❓ Is default constructor always created? → ❌ Only if none is written

🧩 Real-World Mapping
Concept	Real World Example
Constructor	Object initialization form
this	Current student identity
static	College name for all students
final	Aadhar number
super	Parent properties
📂 Folder Structure
Day-13-Constructors-Keywords/
 ┣ 📜 ConstructorDemo.java
 ┣ 📜 ConstructorChaining.java
 ┣ 📜 StaticExample.java
 ┣ 📜 FinalKeywordDemo.java
 ┣ 📜 SuperKeywordDemo.java
 ┗ 📜 README.md
🏆 Key Takeaway

Constructor controls object birth.
Keywords control object behavior.

<div align="center">
🔥 Progress Meter

██████████████░░░░░░░ 65%

🌟 Keep Going – Java Mastery in Progress
</div> ```
````
