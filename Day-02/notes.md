# Day 02 – Client–Server Architecture (Quick Notes)

---

## 🔹 What is Client–Server Architecture?

Client–Server Architecture is a software model where:

- A **client** sends a request
- A **server** processes the request
- The server sends a **response** back to the client

The client and server are **separate systems** with clearly defined roles.

---

## 👤 Client – Key Points

A **client** is responsible for:

- Taking user input
- Sending requests to the server
- Displaying responses to the user

Common client examples:

- Web browsers (Chrome, Firefox)
- Mobile applications
- Frontend frameworks (React, Angular)

Important note:

Clients do **not** handle business logic or database operations.

---

## 🖥️ Server – Key Points

A **server** is responsible for:

- Receiving client requests
- Processing business logic
- Communicating with databases
- Sending responses back to clients

Examples of servers:

- Java Spring Boot application
- Java Servlet-based application
- REST API backend

In this repository:

Java Backend Application = Server

---

## 🔄 Request–Response Flow

Basic communication flow:

Client → Request → Server  
Client ← Response ← Server

Key points:

- Communication usually happens via **HTTP**
- Client waits for server response
- One server can handle multiple clients

---

## ☕ Java Backend Perspective (Very Important)

In a typical Java backend system:

Client  
↓  
Controller Layer  
↓  
Service Layer  
↓  
Repository Layer  
↓  
Database

Important rules:

- Java backend acts as the **server**
- Database is accessed **only by the server**
- Client never communicates directly with the database

---

## 🔐 Why Database Should Not Be Accessed by Client

Reasons:

- Security risks
- Data manipulation threats
- No business rule enforcement
- Difficult to manage consistency

Server acts as a **security and logic gatekeeper**.

---

## 🎤 Interview One-Liners

- Client–Server architecture separates UI and logic
- Client sends requests, server processes them
- Java backend applications act as servers
- Database access is restricted to server only

---

## ⚠️ Common Beginner Mistakes

- Treating frontend and backend as the same
- Writing business logic in client
- Allowing direct database access from client
- Thinking one server handles only one client
- Ignoring request–response lifecycle

---

## ✅ Day 02 Summary

- Client sends request, server sends response
- Client handles UI, server handles logic
- Java backend = server
- Database is protected behind server
- Foundation of backend and system design

---
