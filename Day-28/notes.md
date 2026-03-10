# Day 28 – Spring Boot API Flow Notes

# Phase 5 – Backend Architecture

---

# 1. What is API Flow?

API flow describes how a request travels through different layers of a backend application.

In Spring Boot, requests move through a layered architecture.

Typical layers include:

Client

DispatcherServlet

Controller

Service

Repository

Database

---

# 2. Client Layer

The client sends an HTTP request to the backend server.

Examples of clients:

Web browsers

Mobile applications

Frontend frameworks

API testing tools like Postman

Example request:

GET /api/users

---

# 3. DispatcherServlet

DispatcherServlet is the front controller in Spring MVC.

It is responsible for handling all incoming HTTP requests.

Responsibilities include:

Receiving HTTP requests

Finding the appropriate controller

Managing request processing

Returning responses

---

# 4. Controller Layer

The controller layer handles HTTP requests.

Responsibilities:

Receive client requests

Map endpoints

Call service methods

Return responses

Example:

@GetMapping("/users")

---

# 5. Service Layer

The service layer contains business logic.

Responsibilities:

Processing application rules

Validating data

Coordinating operations

Communicating with repository layer

Example operations:

Process orders

Validate user input

Apply business calculations

---

# 6. Repository Layer

The repository layer interacts with the database.

Responsibilities:

CRUD operations

Query execution

Data persistence

Usually implemented using:

Spring Data JPA

Example methods:

save()

findById()

delete()

---

# 7. Database Layer

The database stores application data.

Examples:

MySQL

PostgreSQL

MongoDB

Oracle

Data is stored permanently.

---

# 8. Request Flow in Spring Boot

When a client sends a request, the following flow occurs:

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

---

# 9. Response Flow

After the database processes the request, the response flows back.

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

# 10. Benefits of Layered Architecture

Layered architecture provides:

Better code organization

Separation of concerns

Improved maintainability

Easy testing

Better scalability

---

# 11. Example API Flow

Example API request:

GET /api/users

Flow:

Client sends request

DispatcherServlet receives request

Controller handles endpoint

Service processes logic

Repository fetches data

Database returns data

Response sent back to client

---

# 12. Spring Boot Architecture Cheat Sheet

Client → Sends HTTP request

DispatcherServlet → Routes request

Controller → API endpoints

Service → Business logic

Repository → Database communication

Database → Data storage

---

# End of Day 28 Notes
