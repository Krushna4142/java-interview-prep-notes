# 📝 Day 13 – Constructors & Keywords Notes

---

## 🔹 Constructor

A constructor is a special method used to initialize objects.

### Characteristics

✔ Same name as class  
✔ No return type  
✔ Automatically called when object is created

---

## 🔹 Types of Constructors

### 1️⃣ Default Constructor

```java
class Test {
    Test() {
        System.out.println("Default Constructor");
    }
}
2️⃣ Parameterized Constructor
class Test {
    int id;

    Test(int id) {
        this.id = id;
    }
}
3️⃣ Constructor Overloading
class Test {
    Test() {}

    Test(int a) {}

    Test(int a, int b) {}
}
🔹 Constructor Chaining

Using this() to call another constructor.

class Demo {

    Demo() {
        this(10);
        System.out.println("Default");
    }

    Demo(int x) {
        System.out.println("Parameterized");
    }
}
🔹 this Keyword
Uses

✔ Refers current object
✔ Calls constructor
✔ Resolves variable conflict

this.id = id;
🔹 static Keyword
Static Variable

Single copy shared among all objects.

static int count;
Static Block

Executes once when class loads.

static {
    System.out.println("Static Block");
}
🔹 final Keyword
Final Variable
final int MAX = 100;
Final Method

Cannot be overridden.

Final Class

Cannot be inherited.

🔹 super Keyword
Call Parent Constructor
super();
Access Parent Method
super.display();
🔹 Object Initialization Flow
Static block
↓
Instance block
↓
Constructor
🔥 Tricky Interview Questions

✔ Constructor return type? → ❌ No
✔ Can we overload constructor? → ✅ Yes
✔ Can constructor be private? → ✅ Yes
✔ Can we use this() and super() together? → ❌ First statement rule

🧠 Memory Insight

Constructor initializes object in heap memory.

🎯 Quick Revision

✔ Constructor = object initialization
✔ this = current object
✔ static = class level
✔ final = constant / restriction
✔ super = parent reference
```
