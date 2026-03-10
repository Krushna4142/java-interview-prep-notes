<div align="center">

# 📅 Day 28 – Spring Boot API Flow Diagram

### Understanding Request Flow Inside a Spring Boot Application

<img src="https://img.shields.io/badge/Day-28-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Difficulty-Medium-success?style=for-the-badge" />
<img src="https://img.shields.io/badge/Focus-Backend%20Architecture-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />

</div>

---

## 🔗 Quick Navigation

- [🎯 Goal of the Day](#-goal-of-the-day)
- [🧠 What You’ll Learn](#-what-youll-learn)
- [📌 Why This Topic Matters](#-why-this-topic-matters)
- [📁 Folder Structure](#-folder-structure)
- [🔄 Spring Boot API Flow](#-spring-boot-api-flow)
- [🎯 Interview Preparation](#-interview-preparation-day-28)
- [⏭️ What’s Next?](#️-whats-next)

---

## 🎯 Goal of the Day

The goal of **Day 28** is to clearly understand **how a request flows inside a Spring Boot application**.

Today focuses on understanding the **backend architecture layers** and how they interact.

You will learn how a request travels through:

- Client
- Controller
- Service
- Repository
- Database

And how the response comes back to the client.

---

## 🧠 What You’ll Learn

By the end of this day, you will understand:

- How API requests enter a Spring Boot application
- The role of **DispatcherServlet**
- How controllers handle HTTP requests
- How the **Service layer processes business logic**
- How the **Repository layer interacts with the database**
- The full **request-response lifecycle**

📌 Detailed explanations and diagrams are available in **notes.md**.

---

## 📌 Why This Topic Matters

Understanding API flow is extremely important for:

- Spring Boot backend interviews
- System design discussions
- Debugging backend applications
- Writing scalable backend services

Interviewers often ask questions like:

- How does a request reach a controller?
- What is DispatcherServlet?
- What is the role of service layer?
- How does Spring Boot interact with databases?

This topic helps demonstrate **real backend system understanding**.

---

## 📁 Folder Structure

Day-28-SpringBoot-API-Flow<br>
│<br>
├── README.md # Overview and architecture explanation<br>
├── notes.md # Detailed backend flow explanation<br>
└── flow-diagram.md # Visual flow diagram<br>

---

## 🔄 Spring Boot API Flow

A typical Spring Boot API request flow looks like this:

Client (Browser / Mobile / Postman)
↓
HTTP Request
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
↑
Repository
↑
Service
↑
Controller
↑
HTTP Response
↑
Client

Each layer has a specific responsibility.

---

### Controller Layer

Responsible for:

- Receiving HTTP requests
- Mapping endpoints
- Calling service methods
- Returning responses

Example:

GET /users
POST /users

---

### Service Layer

Responsible for:

- Business logic
- Processing application rules
- Coordinating between controller and repository

Example:

Validate data
Apply business rules
Call repository methods

---

### Repository Layer

Responsible for:

- Database communication
- CRUD operations
- Query execution

Example:

Save user
Find user by ID
Delete user

---

### Database Layer

Stores application data.

Examples:

- MySQL
- PostgreSQL
- MongoDB
- Oracle

---

## 🎯 Interview Preparation (Day 28)

You should now be able to answer:

- What is the Spring Boot request flow?
- What is DispatcherServlet?
- Difference between Controller and Service?
- What does Repository layer do?
- Why do we separate layers in backend architecture?

📌 These concepts are frequently asked in **Spring Boot interviews**.

---

## 🔗 Helpful References

- https://spring.io/projects/spring-boot
- https://docs.spring.io/spring-framework/docs/current/reference/html/web.html
- https://www.geeksforgeeks.org/spring-boot-architecture/

---

## ⏭️ What’s Next?

<div align="center">

### 👉 **Day 29 – API Design Best Practices**

Learn about:

- REST API naming conventions
- Clean API structure
- Proper status codes
- Real-world API design strategies

<br/>

[➡️ Go to Day 29](../Day-29/README.md)

</div>

---
