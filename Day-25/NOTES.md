# Day 25 – Spring Boot Architecture Notes

# Phase 5 – Backend Development

---

# 1. What is Spring Boot?

Spring Boot is a Java framework used to build backend applications quickly.

It is built on top of the Spring Framework and simplifies application
development by reducing configuration.

Spring Boot helps developers create production-ready applications with
minimal setup.

Main idea:

Write less configuration
Focus more on business logic

---

# 2. Why Spring Boot Exists

Traditional Spring applications required a lot of setup.

Problems with old Spring:

- Heavy XML configuration
- Manual dependency management
- External server setup
- Long setup time

Spring Boot solved these problems by providing:

- Auto configuration
- Embedded servers
- Starter dependencies
- Simple project setup

---

# 3. Key Goals of Spring Boot

Spring Boot focuses on:

- Fast development
- Minimal configuration
- Production-ready features
- Easy deployment
- Microservice support

---

# 4. Key Features of Spring Boot

1. Auto Configuration
2. Embedded Server
3. Starter Dependencies
4. Production Ready Tools
5. Opinionated Defaults

---

# 5. Auto Configuration

Auto configuration automatically configures the application
based on the dependencies available in the project.

Example:

If the dependency

spring-boot-starter-web

is added, Spring Boot automatically configures:

- Spring MVC
- Tomcat server
- JSON converters

Developers do not need to configure everything manually.

---

# 6. Convention over Configuration

Spring Boot follows a principle called:

Convention over Configuration

This means:

Follow standard project structure and naming conventions
instead of writing configuration manually.

Example:

Controller classes inside "controller" package.

Service classes inside "service" package.

Spring Boot automatically understands these conventions.

---

# 7. Embedded Servers

Spring Boot applications include a built-in web server.

Common embedded servers:

- Tomcat (Default)
- Jetty
- Undertow

Advantages:

- No external server installation
- No WAR deployment
- Application runs as a standalone JAR

Run command:

java -jar application.jar

---

# 8. Spring Boot Architecture Overview

Most Spring Boot applications follow a layered architecture.

Architecture structure:

Client
↓
Controller
↓
Service
↓
Repository
↓
Database

Each layer has a specific responsibility.

---

# 9. Client Layer

The client sends HTTP requests to the backend application.

Examples of clients:

- Web browser
- Mobile application
- Frontend application
- Postman or API testing tools

The client interacts with backend APIs.

---

# 10. Controller Layer

The controller layer handles HTTP requests.

Responsibilities:

- Receive client requests
- Map requests to specific methods
- Return responses

Controllers expose REST APIs.

Example annotation:

@RestController

Example endpoint:

GET /users
POST /users
DELETE /users

---

# 11. Service Layer

The service layer contains business logic.

Responsibilities:

- Process data
- Apply business rules
- Coordinate operations

Examples:

- Payment processing
- Order calculation
- User validation

Controllers call the service layer.

---

# 12. Repository Layer

The repository layer handles database operations.

Responsibilities:

- CRUD operations
- Database queries
- Data persistence

Repository interacts with the database.

Usually implemented using:

Spring Data JPA
Hibernate

Example operations:

save()
findById()
delete()
update()

---

# 13. Database Layer

The database layer stores application data.

Common databases used with Spring Boot:

- MySQL
- PostgreSQL
- MongoDB
- Oracle
- SQL Server

Data is stored permanently in the database.

---

# 14. Spring Boot Request Flow

When a request is sent to the application,
it passes through several components.

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

# 15. DispatcherServlet

DispatcherServlet is the central component of Spring MVC.

It acts as the front controller.

Responsibilities:

- Receive all incoming requests
- Route requests to appropriate controllers
- Manage response handling

It controls the request processing workflow.

---

# 16. Spring Boot Starter Dependencies

Spring Boot provides starter dependencies.

Starter dependencies are pre-configured dependency groups.

Examples:

spring-boot-starter-web

Includes:

- Spring MVC
- Tomcat
- JSON libraries

Other examples:

spring-boot-starter-data-jpa
spring-boot-starter-security
spring-boot-starter-test

Benefits:

- Simplifies dependency management
- Reduces configuration
- Faster development

---

# 17. Spring Boot Project Structure

Typical project structure:

src
└─ main
├─ java
│ └─ com.example.project
│ ├─ controller
│ ├─ service
│ ├─ repository
│ ├─ model
│ └─ Application.java
│
└─ resources
├─ application.properties
├─ static
└─ templates

---

# 18. Controller Package

Contains API endpoints.

Example responsibilities:

- Handle HTTP requests
- Call service layer
- Return responses

Example annotation:

@RestController

---

# 19. Service Package

Contains business logic.

Responsibilities:

- Implement application rules
- Process data
- Coordinate between controller and repository

---

# 20. Repository Package

Handles database operations.

Responsibilities:

- Save data
- Fetch data
- Update data
- Delete data

Usually implemented using interfaces.

---

# 21. Model Package

Contains entity classes.

Entities represent database tables.

Example:

User
Order
Product

Each entity maps to a table in the database.

---

# 22. Resources Folder

Contains configuration files and static resources.

Common files:

application.properties
application.yml

These files store application configuration.

---

# 23. application.properties

Main configuration file for Spring Boot.

Used to configure:

- Server settings
- Database connection
- Logging
- Security

Example:

server.port=8080

spring.datasource.url=jdbc:mysql://localhost:3306/app

spring.datasource.username=root

spring.datasource.password=password

---

# 24. Production Ready Features

Spring Boot provides tools for monitoring and management.

Example features:

- Health checks
- Metrics
- Application monitoring
- Logging

These are provided using Spring Boot Actuator.

---

# 25. Why Companies Use Spring Boot

Spring Boot is widely used in industry.

Reasons:

- Fast development
- Scalable architecture
- Microservice friendly
- Strong ecosystem
- Large community support

---

# 26. Real World Applications

Spring Boot is used to build:

- REST APIs
- Microservices
- Enterprise applications
- Banking systems
- E-commerce platforms
- Cloud backend systems

---

# 27. Advantages of Spring Boot

Advantages include:

- Reduced configuration
- Embedded servers
- Easy project setup
- Faster development
- Production-ready features
- Easy deployment

---

# 28. Spring Boot Deployment

Spring Boot applications are packaged as JAR files.

Run command:

java -jar application.jar

The embedded server starts automatically.

---

# 29. Key Spring Boot Components

Important components include:

DispatcherServlet
Controller
Service
Repository
Model
Configuration files

These components work together to process requests.

---

# 30. Spring Boot Architecture Cheat Sheet

Spring Boot Architecture:

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

Core Features:

- Auto Configuration
- Embedded Server
- Starter Dependencies
- Convention over Configuration
