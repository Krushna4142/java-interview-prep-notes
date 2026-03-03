# 📚 Day 21 – Checked vs Unchecked Exceptions (Complete Notes)

---

# 1️⃣ Exception Hierarchy

Object
└── Throwable
├── Error
└── Exception
├── Checked Exceptions
└── RuntimeException (Unchecked Exceptions)

Key Point:
All unchecked exceptions extend RuntimeException.

---

# 2️⃣ Checked Exceptions

## Definition

→ Exceptions checked at compile time  
→ Must be handled OR declared using throws

If not handled:
→ Compilation error

---

## Examples

IOException  
SQLException  
FileNotFoundException  
ClassNotFoundException  
InterruptedException

---

## Example Code

import java.io.\*;

public class CheckedExample {

public static void main(String[] args) {
try {
FileReader fr = new FileReader("test.txt");
} catch (FileNotFoundException e) {
System.out.println("File not found");
}
}

}

If try-catch removed:
→ Compiler error

---

## Why Checked Exceptions Exist?

→ To handle external failures  
→ File handling  
→ Database operations  
→ Network calls

These are usually recoverable.

---

# 3️⃣ Unchecked Exceptions (Runtime Exceptions)

## Definition

→ Occur at runtime  
→ Not mandatory to handle  
→ Caused by programming mistakes

---

## Examples

NullPointerException  
ArithmeticException  
ArrayIndexOutOfBoundsException  
IllegalArgumentException  
NumberFormatException

---

## Example Code

public class UncheckedExample {

public static void main(String[] args) {
int a = 10 / 0; // ArithmeticException
}

}

Compiles successfully  
Fails at runtime

---

# 4️⃣ Checked vs Unchecked – Comparison Table

Feature Checked Unchecked

Checked at Compile time Runtime
Handling mandatory? Yes No
Parent Class Exception RuntimeException
Caused by External issues Programming errors
Compiler enforcement Yes No

---

# 5️⃣ throws Keyword

Used to declare checked exception in method signature.

import java.io.\*;

public class Example {

static void readFile() throws IOException {
FileReader fr = new FileReader("test.txt");
}

}

Meaning:
→ Caller must handle exception.

---

# 6️⃣ throw Keyword

Used to manually throw an exception.

public class Example {

static void checkAge(int age) {
if (age < 18) {
throw new IllegalArgumentException("Age must be 18+");
}
}

}

Used for:
→ Business validation  
→ Custom rule enforcement

---

# 7️⃣ Overriding Rules (Very Important)

If Parent method throws Checked Exception:

Child method:
✔ Can throw same exception  
✔ Can throw subclass (narrower exception)  
❌ Cannot throw broader exception

Example:

class Parent {
void method() throws IOException {}
}

class Child extends Parent {
void method() throws FileNotFoundException {} // Allowed
}

Not Allowed:

class Child extends Parent {
void method() throws Exception {} // Broader → Not allowed
}

Unchecked exceptions:
→ No restriction

---

# 8️⃣ Custom Checked Exception

class InvalidDataException extends Exception {
public InvalidDataException(String message) {
super(message);
}
}

Usage:

if (data == null) {
throw new InvalidDataException("Data cannot be null");
}

---

# 9️⃣ Custom Unchecked Exception

class InvalidDataException extends RuntimeException {
public InvalidDataException(String message) {
super(message);
}
}

Used when:
→ It is programming or validation mistake  
→ You don't want to force handling

---

# 🔟 Exception Propagation

If method does not handle checked exception:

→ It propagates to caller

Flow:

method1()
→ method2()
→ method3() throws exception

If not handled anywhere:
→ JVM handles → Program terminates

---

# 1️⃣1️⃣ When to Use Checked Exception?

✔ File handling  
✔ Database operations  
✔ API calls  
✔ Network failures  
✔ Recoverable situations

Rule:
If caller can recover → Use checked.

---

# 1️⃣2️⃣ When to Use Unchecked Exception?

✔ Invalid input  
✔ Null pointer mistakes  
✔ Logical errors  
✔ Programming bugs

Rule:
If it is developer mistake → Use unchecked.

---

# 1️⃣3️⃣ Why Modern Frameworks Prefer Unchecked?

Because:

→ Too many checked exceptions make code messy  
→ Leads to try-catch everywhere  
→ Cleaner APIs with unchecked exceptions

Spring Framework mostly uses RuntimeExceptions.

---

# 1️⃣4️⃣ Common Interview Questions

Q: Why does Java have checked exceptions?  
A: To force handling of recoverable external failures.

Q: Why RuntimeException is unchecked?  
A: Because they indicate programming mistakes.

Q: Can we catch unchecked exception?  
A: Yes, but not mandatory.

Q: Can we convert checked to unchecked?  
A: Yes, by wrapping inside RuntimeException.

Example:

try {
readFile();
} catch (IOException e) {
throw new RuntimeException(e);
}

---

# 1️⃣5️⃣ Real Backend Example

API Error Example:

{
"status": 400,
"message": "Invalid input",
"timestamp": "2026-03-03"
}

Checked Exception:
→ Database not reachable

Unchecked Exception:
→ Null value passed in service layer

---

# 1️⃣6️⃣ Summary

Checked Exceptions:
→ Compile-time safety  
→ Mandatory handling  
→ External failures

Unchecked Exceptions:
→ Runtime failures  
→ Programming mistakes  
→ Cleaner APIs

Understanding this difference is critical for:

✔ Interviews  
✔ Backend development  
✔ Clean architecture  
✔ Exception design

Master this → You understand Java error handling deeply.
