<div align="center">

# 📅 Day 27 – Exception Handling in Spring Boot

## 🚀 Phase 5 – Spring Boot Backend Development

<img src="https://img.shields.io/badge/Day-27-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Topic-Exception%20Handling-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Phase-5-green?style=for-the-badge" />
<img src="https://img.shields.io/badge/Focus-Error%20Handling-orange?style=for-the-badge" />

</div>

---

# 📘 Day 27 – Exception Handling in Spring Boot

In real backend systems, things can go wrong:

Database errors
Invalid user input
Resource not found
Server failures

If we do not handle these errors properly, the application may crash or return poor responses.

Spring Boot provides powerful tools to **handle exceptions gracefully and return meaningful API responses**.

---

# 🎯 Goal of Today

Understand how **exception handling works in Spring Boot REST APIs**.

Topics covered:

✔ What is an Exception
✔ Why Exception Handling is Important
✔ Default Spring Boot Error Handling
✔ @ExceptionHandler
✔ @ControllerAdvice
✔ @RestControllerAdvice
✔ Custom Exception Classes
✔ Global Exception Handling

---

# ⚠️ What is an Exception?

An exception is an **unexpected event that occurs during program execution**.

Example problems:

User not found
Invalid input data
Database connection failure
Null pointer access

Example Java exception:

```java
int result = 10 / 0;

This causes:

java.lang.ArithmeticException
❗ Why Exception Handling is Important

Without proper handling:

Application crashes
Unclear error messages
Bad user experience
Security risks

Good exception handling provides:

Clear error responses
Consistent API behavior
Better debugging
Improved reliability
🔧 Default Error Handling in Spring Boot

Spring Boot automatically handles exceptions and returns a default error response.

Example response:

{
  "timestamp": "2024-01-01T12:00:00",
  "status": 500,
  "error": "Internal Server Error",
  "path": "/users"
}

But in real applications, we usually customize error responses.

🧩 @ExceptionHandler

@ExceptionHandler is used to handle specific exceptions inside a controller.

Example:

@RestController
public class UserController {

    @GetMapping("/users/{id}")
    public String getUser() {
        throw new RuntimeException("User not found");
    }

    @ExceptionHandler(RuntimeException.class)
    public String handleException(RuntimeException ex) {
        return ex.getMessage();
    }

}

This catches exceptions thrown in that controller.

🌍 Global Exception Handling

Instead of handling exceptions in each controller, we can create global exception handlers.

This keeps the code clean and reusable.

Spring provides:

@ControllerAdvice
🧠 @ControllerAdvice

@ControllerAdvice allows us to handle exceptions globally across all controllers.

Example:

@ControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(Exception.class)
    public String handleGlobalException(Exception ex) {
        return ex.getMessage();
    }

}

Now all controllers will use this handler.

🚀 @RestControllerAdvice

@RestControllerAdvice is a combination of:

@ControllerAdvice + @ResponseBody

Used for REST APIs.

Example:

@RestControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(RuntimeException.class)
    public String handleRuntimeException(RuntimeException ex) {
        return ex.getMessage();
    }

}

This automatically returns responses as JSON or text.

🧩 Custom Exception Classes

We can create custom exceptions for better error handling.

Example:

public class UserNotFoundException extends RuntimeException {

    public UserNotFoundException(String message) {
        super(message);
    }

}

Usage:

throw new UserNotFoundException("User not found");
🔄 Handling Custom Exceptions

Example global handler:

@RestControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(UserNotFoundException.class)
    public String handleUserNotFound(UserNotFoundException ex) {

        return ex.getMessage();

    }

}
🧠 Typical Exception Handling Flow
Client Request
      ↓
Controller
      ↓
Exception Occurs
      ↓
Global Exception Handler
      ↓
Custom Error Response
      ↓
Client
📦 Typical Project Structure
src
 └─ main
     └─ java
         └─ com.example.project
              ├─ controller
              ├─ service
              ├─ repository
              ├─ exception
              │     ├─ GlobalExceptionHandler.java
              │     └─ UserNotFoundException.java
              └─ model

Creating a separate exception package is recommended.

🧠 Interview Questions

You should now be able to answer:

What is an exception?
Why is exception handling important?
What is @ExceptionHandler?
What is @ControllerAdvice?
Difference between @ControllerAdvice and @RestControllerAdvice?
How do you create custom exceptions?
📁 Folder Structure (Day 27)
Day-27-SpringBoot-Exception-Handling
│
├── README.md
├── notes.md

🚀 What Comes Next
Day 28 – Validation in Spring Boot

You will learn:

✔ @Valid
✔ @NotNull
✔ @NotBlank
✔ @Size
✔ Input validation for REST APIs

This is critical for building secure and reliable backend APIs.

< align="center">
💬 “Good backend systems don’t just handle success — they handle failure gracefully.”



<br/>

[➡️ Go to Day 26](../Day-26/README.md)

</div>

```
