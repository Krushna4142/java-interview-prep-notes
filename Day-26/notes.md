# Day 26 – REST Controllers & Annotations

# Phase 5 – Spring Boot Backend Development

---

# 1. What is REST?

REST stands for:

Representational State Transfer

REST is an architectural style used to build web services that allow communication between client and server using HTTP.

REST APIs usually return data in JSON format.

Example response:

{
"id": 1,
"name": "Alice"
}

REST APIs are stateless.

This means:

Every request contains all necessary information.

---

# 2. What is a REST API?

A REST API allows applications to communicate using HTTP requests.

Client examples:

- Web browser
- Mobile application
- Frontend application
- Postman

Server example:

- Spring Boot application

Example API request:

GET /users

Example API response:

[
{ "id": 1, "name": "Alice" },
{ "id": 2, "name": "Bob" }
]

---

# 3. HTTP Methods Used in REST

Common HTTP methods used in REST APIs:

GET

Used to retrieve data.

Example:

GET /users

POST

Used to create new data.

Example:

POST /users

PUT

Used to update existing data.

Example:

PUT /users/1

DELETE

Used to delete data.

Example:

DELETE /users/1

---

# 4. What is a Controller in Spring Boot?

A Controller is a Java class that handles HTTP requests.

Responsibilities:

Receive HTTP request

Process request

Return response

Controllers expose API endpoints.

Example endpoint:

GET /users

POST /users

---

# 5. @RestController Annotation

@RestController is used to create REST APIs.

It tells Spring Boot that this class will handle HTTP requests and return data directly.

@RestController automatically converts return values to JSON.

Example:

@RestController
public class HelloController {

    @GetMapping("/hello")
    public String sayHello() {

        return "Hello Spring Boot";

    }

}

API call:

http://localhost:8080/hello

Response:

Hello Spring Boot

---

# 6. @Controller vs @RestController

@Controller

Used for web applications that return HTML pages.

@RestController

Used for REST APIs that return JSON or text data.

@RestController internally includes:

@Controller + @ResponseBody

---

# 7. @RequestMapping Annotation

@RequestMapping maps HTTP requests to controller classes or methods.

Example:

@RestController
@RequestMapping("/users")
public class UserController {

}

Now all endpoints will start with:

/users

Example endpoints:

/users/all

/users/1

/users/create

---

# 8. @GetMapping Annotation

@GetMapping handles HTTP GET requests.

Used for retrieving data.

Example:

@GetMapping("/users")
public String getUsers() {

    return "All Users";

}

HTTP request:

GET /users

---

# 9. @PostMapping Annotation

@PostMapping handles HTTP POST requests.

Used for creating new resources.

Example:

@PostMapping("/users")
public String createUser() {

    return "User Created";

}

HTTP request:

POST /users

---

# 10. @PutMapping Annotation

@PutMapping handles HTTP PUT requests.

Used for updating existing resources.

Example:

@PutMapping("/users/{id}")
public String updateUser() {

    return "User Updated";

}

HTTP request:

PUT /users/1

---

# 11. @DeleteMapping Annotation

@DeleteMapping handles HTTP DELETE requests.

Used for deleting resources.

Example:

@DeleteMapping("/users/{id}")
public String deleteUser() {

    return "User Deleted";

}

HTTP request:

DELETE /users/1

---

# 12. REST Endpoint Design

Typical REST API structure:

GET /users

GET /users/1

POST /users

PUT /users/1

DELETE /users/1

Each endpoint performs a specific action.

---

# 13. Example Controller

@RestController
@RequestMapping("/api/users")
public class UserController {

    @GetMapping
    public String getUsers() {
        return "All Users";
    }

    @PostMapping
    public String createUser() {
        return "User Created";
    }

    @PutMapping("/{id}")
    public String updateUser() {
        return "User Updated";
    }

    @DeleteMapping("/{id}")
    public String deleteUser() {
        return "User Deleted";
    }

}

---

# 14. Typical Spring Boot Controller Package

Controllers should be placed in the controller package.

Example project structure:

src
└─ main
└─ java
└─ com.example.project
├─ controller
│ └─ UserController.java
│
├─ service
├─ repository
└─ model

---

# 15. Request Flow in Spring Boot

Client sends request.

Request flow:

Client
↓
DispatcherServlet
↓
Controller
↓
Service
↓
Repository
↓
Database

Response flow:

Database
↑
Repository
↑
Service
↑
Controller
↑
Client

---

# 16. DispatcherServlet

DispatcherServlet is the front controller of Spring MVC.

Responsibilities:

Receive all HTTP requests

Find correct controller

Send response back to client

---

# 17. Testing REST APIs

REST APIs can be tested using:

Postman

Insomnia

Curl command

Web browser (for GET requests)

Example test:

GET

http://localhost:8080/users

---

# 18. Advantages of REST APIs

Simple architecture

Platform independent

Uses standard HTTP

Lightweight communication

Easy integration with frontend

---

# 19. Common Use Cases

REST APIs are used for:

Mobile backends

Web application backends

Microservices

Cloud services

Enterprise systems

---

# 20. REST Controllers Cheat Sheet

@RestController

Used to create REST APIs.

@RequestMapping

Base URL mapping.

@GetMapping

Handles GET requests.

@PostMapping

Handles POST requests.

@PutMapping

Handles PUT requests.

@DeleteMapping

Handles DELETE requests.

---

# End of Day 26 Notes
