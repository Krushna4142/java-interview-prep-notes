# Spring Boot API Flow Diagram

This diagram explains how a request travels inside a Spring Boot application.

Understanding this flow is essential for backend development and Spring Boot interviews.

---

## API Request Flow

Client (Browser / Mobile / Postman)
│
│ HTTP Request
▼
DispatcherServlet
│
▼
Controller
│
▼
Service
│
▼
Repository
│
▼
Database
│
▲
Repository
▲
Service
▲
Controller
▲
HTTP Response
▲
Client

---

## Step-by-Step Flow

### 1. Client Request

The client sends an HTTP request to the server.

Example:

GET /api/users
POST /api/users

Clients can be:

- Web browser
- Mobile app
- Frontend application
- Postman

---

### 2. DispatcherServlet

DispatcherServlet is the **front controller of Spring MVC**.

Responsibilities:

- Receives all HTTP requests
- Determines which controller should handle the request
- Manages request flow

---

### 3. Controller Layer

The controller receives the request from DispatcherServlet.

Responsibilities:

- Map endpoints
- Receive request data
- Call service layer

Example:

@GetMapping("/users")

---

### 4. Service Layer

The service layer contains business logic.

Responsibilities:

- Process data
- Apply business rules
- Coordinate between controller and repository

Example tasks:

Validate data
Calculate values
Process operations

---

### 5. Repository Layer

The repository communicates with the database.

Responsibilities:

- Perform CRUD operations
- Execute queries
- Persist data

Example methods:

save()
findById()
delete()

---

### 6. Database Layer

Stores application data.

Common databases used with Spring Boot:

- MySQL
- PostgreSQL
- MongoDB
- Oracle

---

### 7. Response Flow

After data is processed, the response travels back:

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

## Why This Architecture is Important

Layered architecture provides:

Clear separation of concerns
Better maintainability
Improved scalability
Cleaner code structure

---

## Interview Questions

Common questions based on this topic:

What is DispatcherServlet?

Explain the request flow in Spring Boot.

What is the role of Controller layer?

Difference between Service and Repository?

Why do we use layered architecture?

---

## Quick Cheat Sheet

Client → Sends HTTP request

DispatcherServlet → Routes request

Controller → Handles API endpoints

Service → Business logic

Repository → Database communication

Database → Stores data

---
