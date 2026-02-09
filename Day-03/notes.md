# Day 03 – HTTP & REST Basics (Quick Notes)

---

## What is HTTP?

HTTP (HyperText Transfer Protocol) is a communication protocol used for data exchange between:

- Client
- Server

It defines **how requests are sent** and **how responses are returned**.

HTTP is:

- Stateless
- Text-based
- Request–Response oriented

---

## Why HTTP is Needed?

HTTP allows:

- Web browsers to talk to servers
- Frontend to communicate with backend
- APIs to exchange data

Without HTTP:

- Client and server cannot understand each other
- No standard communication rules exist

---

## HTTP Request – Key Components

An HTTP request contains:

- Request Method
- URL
- Headers
- Body (optional)

Example flow:

Client  
↓  
HTTP Request  
↓  
Server

---

## HTTP Response – Key Components

An HTTP response contains:

- Status Code
- Headers
- Body (data)

Example flow:

Server  
↓  
HTTP Response  
↓  
Client

---

## Common HTTP Methods (Very Important)

GET

- Fetch data from server
- Does not change server state

POST

- Send data to server
- Used to create resources

PUT

- Update entire resource

PATCH

- Update partial resource

DELETE

- Remove resource

Interview Tip:
GET is safe, POST modifies data.

---

## Stateless Nature of HTTP

Stateless means:

- Server does not remember previous requests
- Each request is independent

To maintain state:

- Cookies
- Sessions
- Tokens (JWT)

---

## What is REST?

REST (Representational State Transfer) is an **architecture style** for designing APIs.

REST uses:

- HTTP protocol
- Standard HTTP methods
- URL-based resource identification

---

## REST Key Principles

Client–Server separation  
Stateless communication  
Uniform interface  
Resource-based URLs

Example:

/users  
/users/101  
/orders/202

---

## REST vs Normal HTTP Usage

HTTP:

- Communication protocol

REST:

- Rules on how to use HTTP properly for APIs

REST = Discipline over HTTP

---

## Java Backend Perspective

In Java backend (Spring Boot):

- Controller handles HTTP requests
- REST APIs expose endpoints
- JSON is commonly used as data format

Flow:

Client  
↓  
HTTP Request  
↓  
@RestController  
↓  
Service  
↓  
Database

---

## Interview One-Liners

- HTTP is a stateless request–response protocol
- REST is an architectural style for APIs
- REST APIs use HTTP methods meaningfully
- Java Spring Boot uses REST extensively

---

## Common Beginner Mistakes

- Confusing REST with HTTP
- Using GET for data modification
- Ignoring stateless nature
- Poor URL naming
- Misusing POST and PUT

---

## Day 03 Summary

- HTTP enables client–server communication
- REST provides structure to HTTP APIs
- Java backend relies heavily on REST
- Strong foundation for API development

---
