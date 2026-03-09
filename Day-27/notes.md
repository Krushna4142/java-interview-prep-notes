# Day 27 – Exception Handling in Spring Boot

# Phase 5 – Spring Boot Backend Development

---

# 1. What is an Exception?

An exception is an unexpected event that occurs during program execution.

It interrupts the normal flow of the application.

Examples of exceptions:

- Invalid input
- Database failure
- Resource not found
- Arithmetic errors
- Null pointer access

Example in Java:

int result = 10 / 0;

This throws:

java.lang.ArithmeticException

---

# 2. Why Exception Handling is Important

If exceptions are not handled properly, the application may crash.

Problems without exception handling:

- Application crashes
- Poor user experience
- Unclear error messages
- Difficult debugging
- Security risks

Good exception handling provides:

- Clear error responses
- Consistent API behavior
- Improved reliability
- Better debugging

---

# 3. Exception Handling in Spring Boot

Spring Boot provides built-in mechanisms for handling exceptions in REST APIs.

It allows developers to:

- Catch exceptions
- Customize error responses
- Handle errors globally

Spring Boot returns structured error responses.

Example default response:

{
"timestamp": "2024-01-01T12:00:00",
"status": 500,
"error": "Internal Server Error",
"path": "/users"
}

---

# 4. Types of Exceptions

In Java there are two main types.

Checked Exceptions

These must be handled at compile time.

Example:

IOException

SQLException

Unchecked Exceptions

These occur at runtime.

Example:

NullPointerException

ArithmeticException

IllegalArgumentException

---

# 5. Default Error Handling in Spring Boot

Spring Boot automatically handles exceptions.

If an error occurs, Spring Boot returns a default JSON response.

Example:

{
"timestamp": "2024-01-01T12:00:00",
"status": 404,
"error": "Not Found",
"path": "/users/10"
}

However, real applications require custom error messages.

---

# 6. @ExceptionHandler Annotation

@ExceptionHandler is used to handle specific exceptions in a controller.

It allows developers to define custom error responses.

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

This method handles RuntimeException thrown in the controller.

---

# 7. Limitation of @ExceptionHandler

The @ExceptionHandler defined inside a controller works only for that controller.

If multiple controllers exist, each controller would need its own exception handler.

This leads to code duplication.

To solve this problem we use global exception handling.

---

# 8. Global Exception Handling

Global exception handling allows exceptions to be handled across the entire application.

Spring Boot provides special annotations for this purpose.

@ControllerAdvice

@RestControllerAdvice

---

# 9. @ControllerAdvice

@ControllerAdvice is used to define global exception handlers.

It applies to all controllers in the application.

Example:

@ControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(Exception.class)
    public String handleGlobalException(Exception ex) {

        return ex.getMessage();

    }

}

This handler will catch exceptions from all controllers.

---

# 10. @RestControllerAdvice

@RestControllerAdvice is used in REST applications.

It combines:

@ControllerAdvice

@ResponseBody

This means responses are automatically returned as JSON.

Example:

@RestControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(RuntimeException.class)
    public String handleRuntimeException(RuntimeException ex) {

        return ex.getMessage();

    }

}

---

# 11. Custom Exception Classes

Developers can create custom exception classes.

This helps represent specific application errors.

Example:

UserNotFoundException

OrderNotFoundException

PaymentFailedException

Example custom exception:

public class UserNotFoundException extends RuntimeException {

    public UserNotFoundException(String message) {

        super(message);

    }

}

---

# 12. Throwing Custom Exceptions

Custom exceptions can be thrown in services or controllers.

Example:

throw new UserNotFoundException("User not found");

This helps create meaningful error messages.

---

# 13. Handling Custom Exceptions

Custom exceptions can be handled using global exception handlers.

Example:

@RestControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(UserNotFoundException.class)
    public String handleUserNotFound(UserNotFoundException ex) {

        return ex.getMessage();

    }

}

---

# 14. Exception Handling Flow

Typical flow when an exception occurs.

Client sends request

↓

Controller processes request

↓

Exception occurs

↓

Spring Boot finds matching exception handler

↓

Handler processes the error

↓

Response returned to client

---

# 15. Typical Exception Package

In Spring Boot projects, exceptions are organized in a separate package.

Example structure:

src
└─ main
└─ java
└─ com.example.project
├─ controller
├─ service
├─ repository
├─ model
└─ exception
├─ GlobalExceptionHandler.java
└─ UserNotFoundException.java

---

# 16. Best Practices for Exception Handling

Use custom exceptions for business errors.

Use global exception handlers instead of local ones.

Return meaningful error messages.

Avoid exposing internal system details.

Organize exceptions in a separate package.

---

# 17. Example Error Response Design

A good API error response may include:

timestamp

status

error

message

path

Example:

{
"timestamp": "2024-01-01T12:00:00",
"status": 404,
"error": "Not Found",
"message": "User not found",
"path": "/users/10"
}

---

# 18. Real World Use Cases

Exception handling is used for:

User not found

Invalid request input

Database failures

Authentication errors

Authorization errors

---

# 19. Advantages of Proper Exception Handling

Improves API reliability

Provides better user experience

Makes debugging easier

Maintains consistent error responses

Improves application stability

---

# 20. Exception Handling Cheat Sheet

Exception

Unexpected event that interrupts program flow.

@ExceptionHandler

Handles specific exceptions in controllers.

@ControllerAdvice

Global exception handling for all controllers.

@RestControllerAdvice

Global exception handling for REST APIs.

Custom Exception

User-defined exception class for specific errors.

Global Exception Handler

Centralized class for handling errors.

---

# End of Day 27 Notes
