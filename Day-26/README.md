<div align="center">

# 📅 Day 26 – REST Controllers & Annotations

## 🚀 Phase 5 – Spring Boot Backend Development

<img src="https://img.shields.io/badge/Day-26-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Topic-REST%20Controllers-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Phase-5-green?style=for-the-badge" />
<img src="https://img.shields.io/badge/Focus-Spring%20Boot%20Annotations-orange?style=for-the-badge" />

</div>

---

# 📘 Day 26 – REST Controllers & Annotations

Today we start building **actual REST APIs using Spring Boot**.

You will learn how backend applications **handle HTTP requests and return responses** using **controllers and annotations**.

This is one of the **most important topics in backend development**.

---

# 🎯 Goal of Today

Understand how Spring Boot handles **REST API requests** using controllers.

Topics covered today:

✔ What is a REST API
✔ What is a Controller
✔ @RestController
✔ @RequestMapping
✔ @GetMapping
✔ @PostMapping
✔ @PutMapping
✔ @DeleteMapping
✔ Request & Response handling

---

# 🌐 What is a REST API?

REST stands for:

Representational State Transfer

A REST API allows **clients and servers to communicate using HTTP**.

Example request:

GET /users

Example response:

[
{ "id": 1, "name": "Alice" },
{ "id": 2, "name": "Bob" }
]

REST APIs usually return **JSON data**.

---

# 🧩 What is a Controller?

A controller is a **Java class that handles HTTP requests**.

Responsibilities:

Receive request
Process request
Return response

Controllers expose **API endpoints**.

Example endpoint:

GET /users
POST /users
DELETE /users

---

# ⚙️ @RestController

`@RestController` is used to create REST APIs.

It combines:

@Controller + @ResponseBody

Meaning:

Return data directly as JSON

Example:

```java
@RestController
public class HelloController {

    @GetMapping("/hello")
    public String sayHello() {
        return "Hello Spring Boot";
    }

}

Access API:

http://localhost:8080/hello

Response:

Hello Spring Boot
🧭 @RequestMapping

Used to map HTTP requests to controller classes or methods.

Example:

@RestController
@RequestMapping("/users")
public class UserController {

}

Now all endpoints start with:

/users

Example:

/users/all
/users/1
/users/create
📥 @GetMapping

Used for reading data.

Example:

@GetMapping("/users")
public String getUsers() {
    return "All Users";
}

HTTP request:

GET /users
📤 @PostMapping

Used for creating data.

Example:

@PostMapping("/users")
public String createUser() {
    return "User Created";
}

HTTP request:

POST /users
🔄 @PutMapping

Used for updating existing data.

Example:

@PutMapping("/users/{id}")
public String updateUser() {
    return "User Updated";
}

HTTP request:

PUT /users/1
❌ @DeleteMapping

Used for deleting data.

Example:

@DeleteMapping("/users/{id}")
public String deleteUser() {
    return "User Deleted";
}

HTTP request:

DELETE /users/1
🔄 REST API HTTP Methods
GET    → Read data
POST   → Create data
PUT    → Update data
DELETE → Delete data

Example API design:

GET    /users
GET    /users/1
POST   /users
PUT    /users/1
DELETE /users/1
🧠 Controller Example
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
📦 Typical Controller Package
src/main/java
   └── com.example.project
          └── controller
                └── UserController.java

Controllers should always be placed inside the controller package.

🧠 Interview Questions

You should now be able to answer:

What is a REST API?
What is a Controller in Spring Boot?
Difference between @Controller and @RestController?
What is @RequestMapping?
Difference between GET, POST, PUT, DELETE?
📁 Folder Structure (Day 26)
Day-26-REST-Controllers
│
├── README.md
├── notes.md
└── controller-example.md
🚀 What Comes Next
Day 27 – RequestBody, PathVariable & RequestParam

You will learn how to receive real data from API requests.

Examples:

POST /users
{
  "name": "John",
  "email": "john@email.com"
}

This is where real backend API development begins.

<div align="center">
💬 "Controllers are the entry point of every backend API."
</div>

<br/>

[➡️ Go to Day 26](../Day-26/README.md)

</div>

```
