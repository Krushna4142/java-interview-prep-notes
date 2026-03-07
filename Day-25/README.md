<div align="center">

# 📅 Day 25 – Spring Boot Architecture

## 🚀 Welcome to Phase 5 – Backend Development with Spring Boot

<img src="https://img.shields.io/badge/Day-25-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Topic-Spring%20Boot-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Phase-5-green?style=for-the-badge" />
<img src="https://img.shields.io/badge/Focus-Backend%20Architecture-orange?style=for-the-badge" />

</div>

---

# 🚀 Phase 5 Begins – Spring Boot & Real Backend Development

You have completed:

Phase 1 → Java Fundamentals
Phase 2 → Object-Oriented Programming
Phase 3 → Collections Framework
Phase 4 → JVM, Multithreading & Core Internals

Now begins the **most important phase**:

# ⚡ Phase 5 – Backend Development with Spring Boot

This phase focuses on building **real backend systems** used in production.

---

# 🎯 Goal of Day 25

Understand the **architecture of Spring Boot applications**.

You will learn:

✔ What Spring Boot is
✔ Why Spring Boot exists
✔ Core Spring Boot architecture
✔ Layered backend architecture
✔ Spring Boot request flow
✔ Real-world backend structure

This is the **foundation of modern Java backend development**.

---

# 🌱 What is Spring Boot?

Spring Boot is a **Java framework used to build production-ready backend applications quickly**.

It is built on top of:

Spring Framework

Spring Boot simplifies:

Configuration
Dependency Management
Server Setup
Application Bootstrapping

---

# ⚡ Why Spring Boot Was Created

Traditional Spring applications required:

✔ Heavy XML configuration
✔ Manual dependency setup
✔ External server configuration
✔ Complex project structure

Spring Boot solves this by providing:

✔ Auto Configuration
✔ Embedded Server
✔ Starter Dependencies
✔ Production-ready features

---

# 🧠 Core Concepts of Spring Boot

Spring Boot is built on three key principles:

1️⃣ Auto Configuration
2️⃣ Convention over Configuration
3️⃣ Embedded Server

---

# 🏗 Spring Boot Architecture

Typical Spring Boot application follows **Layered Architecture**.

Client
↓
Controller Layer
↓
Service Layer
↓
Repository Layer
↓
Database

---

# 📦 Layered Architecture Explained

### 1️⃣ Controller Layer

Handles HTTP requests.

Responsibilities:

Receive API requests
Send API responses
Call service layer

Example:

@GetMapping("/users")

---

### 2️⃣ Service Layer

Contains **business logic**.

Responsibilities:

Process data
Apply business rules
Coordinate between layers

---

### 3️⃣ Repository Layer

Handles **database operations**.

Responsibilities:

CRUD operations
Database communication
Data persistence

---

### 4️⃣ Database Layer

Stores application data.

Examples:

MySQL
PostgreSQL
MongoDB

---

# 🔄 Spring Boot Request Flow

When a request hits the application:

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

# ⚙️ Key Components in Spring Boot

Spring Boot Starter
Spring Boot Auto Configuration
Spring Boot CLI
Spring Boot Actuator
Spring Boot DevTools

---

# 🧩 Embedded Server

Spring Boot includes embedded servers such as:

Tomcat (default)
Jetty
Undertow

Meaning:

No need to deploy WAR file
Application runs directly

Run application using:

java -jar application.jar

---

# 📁 Typical Spring Boot Project Structure

src
└─ main
├─ java
│ └─ com.example.app
│ ├─ controller
│ ├─ service
│ ├─ repository
│ └─ model
│
└─ resources
├─ application.properties
├─ static
└─ templates

---

# 🧠 Why Backend Engineers Use Spring Boot

Spring Boot is used for building:

REST APIs
Microservices
Enterprise applications
Cloud backend systems
Banking platforms
E-commerce platforms

Companies using Spring Boot:

Netflix
Amazon
Alibaba
Uber
Google (some services)

---

# 📁 Folder Structure (Today)

Day-25-SpringBoot-Architecture
│
├── README.md
├── notes.md
└── architecture-diagram.md

---

# 🎯 Interview Questions

You should be able to answer:

What is Spring Boot?
Why is Spring Boot used?
Difference between Spring and Spring Boot?
What is layered architecture?
What is embedded server?
What is DispatcherServlet?

---

# 🚀 What’s Coming Next

Day 26 – Spring Boot Project Setup

You will learn:

✔ Spring Initializr
✔ Maven project setup
✔ First Spring Boot application
✔ Running REST API

This is where **real backend coding begins**.

---

<div align="center">

### 💬 “Core Java builds the foundation.

### Spring Boot builds real-world backend systems.”

</div>
<br/>

[➡️ Go to Day 26](../Day-26/README.md)

</div>

---
