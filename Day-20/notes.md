# 📚 Day 20 – Exception Handling (Complete Notes – Phase 4)

---

# 1️⃣ What is an Exception?

An Exception is:

→ An unwanted or unexpected event  
→ That occurs during program execution  
→ Disrupts normal program flow

Example:

int a = 10 / 0; // ArithmeticException

Without handling:
→ Program terminates abnormally

---

# 2️⃣ Exception Hierarchy

Object
└── Throwable
├── Error
└── Exception
├── Checked Exception
└── RuntimeException (Unchecked)

---

# 3️⃣ Types of Exceptions

## ✅ 1. Checked Exceptions

✔ Checked at compile time  
✔ Must handle using try-catch OR declare using throws

Examples:

- IOException
- SQLException
- FileNotFoundException
- ClassNotFoundException

Rule:
If method throws checked exception → must handle or declare.

---

## ✅ 2. Unchecked Exceptions (RuntimeException)

✔ Occur at runtime  
✔ Not mandatory to handle

Examples:

- ArithmeticException
- NullPointerException
- ArrayIndexOutOfBoundsException
- IllegalArgumentException

Usually caused by:
→ Programming mistakes

---

## ✅ 3. Errors

✔ Serious system-level problems  
✔ Should NOT be handled

Examples:

- OutOfMemoryError
- StackOverflowError

---

# 4️⃣ try-catch-finally

## Basic Syntax

try {
// risky code
} catch (ExceptionType e) {
// handling logic
} finally {
// cleanup code (always runs)
}

---

## Execution Flow

1. try block executes
2. If exception occurs → jumps to matching catch
3. finally always executes
4. If not handled → propagates to caller

---

# 5️⃣ Multiple Catch Blocks

try {
// risky code
} catch (ArithmeticException e) {
// handle arithmetic error
} catch (NullPointerException e) {
// handle null error
}

Rule:
Specific exception must come before generic.

Correct:

catch (ArithmeticException e)
catch (Exception e)

Wrong:

catch (Exception e)
catch (ArithmeticException e) // unreachable

---

# 6️⃣ throw Keyword

Used to manually throw an exception.

if (age < 18) {
throw new IllegalArgumentException("Invalid Age");
}

Purpose:
→ Business validation
→ Custom rule enforcement

---

# 7️⃣ throws Keyword

Used in method signature to declare exception.

public void readFile() throws IOException {
}

Meaning:
→ Caller must handle this exception.

---

# 8️⃣ throw vs throws

throw:
→ Used inside method
→ Actually throws exception
→ Followed by object

throws:
→ Used in method signature
→ Declares exception
→ Followed by class name

---

# 9️⃣ finally Block

✔ Always executes  
✔ Used for cleanup

Examples:
→ Closing file
→ Closing database connection
→ Releasing resources

Exception:
finally may not execute if:

- System.exit()
- JVM crash

---

# 🔟 try-with-resources (Java 7+)

Automatically closes resources.

try (BufferedReader br = new BufferedReader(new FileReader("file.txt"))) {
System.out.println(br.readLine());
}

Requirements:
→ Resource must implement AutoCloseable

Benefits:
✔ Cleaner code
✔ No need for finally block

---

# 1️⃣1️⃣ Custom Exception

## Creating Custom Checked Exception

class InvalidAgeException extends Exception {
public InvalidAgeException(String message) {
super(message);
}
}

## Creating Custom Unchecked Exception

class InvalidAgeException extends RuntimeException {
public InvalidAgeException(String message) {
super(message);
}
}

Use When:
→ Business logic validation
→ Domain-specific errors

---

# 1️⃣2️⃣ Exception Propagation

If method does not handle exception:

→ It propagates to caller

Example:

method1() → method2() → method3()

If method3 throws exception:
→ Goes to method2
→ If not handled → Goes to method1
→ If still not handled → JVM handles

---

# 1️⃣3️⃣ Important Interview Concepts

## ✔ Checked vs Unchecked

Checked:
→ Compile-time safety

Unchecked:
→ Programming error

---

## ✔ Can we override method and throw exception?

Rule:
Child method can:
✔ Throw same exception
✔ Throw narrower exception
❌ Cannot throw broader exception

---

## ✔ Can we have try without catch?

Yes, if finally is present.

try {
}
finally {
}

---

## ✔ Can finally run without catch?

Yes.

---

## ✔ Does finally always execute?

Almost always.

Exceptions:

- System.exit()
- Power failure
- JVM crash

---

# 1️⃣4️⃣ Best Practices

✔ Catch specific exceptions  
✔ Do not swallow exceptions  
✔ Log exceptions properly  
✔ Use custom exceptions for business logic  
✔ Clean resources properly  
✔ Avoid empty catch blocks  
✔ Never catch Throwable

---

# 1️⃣5️⃣ Real Backend Usage

Exception handling is used in:

→ API error responses  
→ Validation failures  
→ Database failures  
→ Logging strategy  
→ Microservices error handling

Example API response:

{
"status": 400,
"message": "Invalid input",
"timestamp": "2026-02-27"
}

---

# 1️⃣6️⃣ Common Exceptions You Must Know

ArithmeticException  
NullPointerException  
IllegalArgumentException  
IllegalStateException  
ArrayIndexOutOfBoundsException  
NumberFormatException  
IOException  
SQLException

---

# 1️⃣7️⃣ Summary

Exception Handling helps in:

✔ Preventing program crash  
✔ Maintaining flow  
✔ Writing robust applications  
✔ Handling real-world failures  
✔ Building production-ready systems

---

# 🚀 Phase 4 Mindset

Phase 4 focus:

→ Safe code  
→ Clean error handling  
→ Resource management  
→ Backend-level thinking

Strong developers are not those who avoid errors.

They are those who handle them intelligently.
