# Day 04 – HTTP Status Codes & API Design Basics (Quick Notes)

---

## What are HTTP Status Codes?

HTTP Status Codes are **standard numeric codes** sent by the server to indicate:

- Result of the client request
- Success or failure of an API call
- Type of error (if any)

They help the client understand **what happened** after making a request.

---

## Why HTTP Status Codes are Important?

Status codes:

- Improve API clarity
- Help frontend handle responses correctly
- Are critical for debugging
- Show backend maturity in interviews

Interviewers expect:

- Correct usage
- Logical understanding
- Real-world examples

---

## Status Code Categories (High Level)

HTTP status codes are divided into:

- 1xx → Informational
- 2xx → Success
- 3xx → Redirection
- 4xx → Client Error
- 5xx → Server Error

In interviews, focus mainly on:
2xx, 4xx, 5xx

---

## 2xx – Success Responses

Used when the request is **successfully processed**.

Common 2xx codes:

200 OK

- Request successful
- Used for GET, PUT, DELETE

201 Created

- Resource successfully created
- Mostly used with POST

204 No Content

- Request successful but no response body
- Used in DELETE operations

Interview Tip:  
POST → 201  
GET → 200

---

## 3xx – Redirection Responses

Used when client needs to take **additional action**.

Common examples:

301 Moved Permanently  
302 Found

Mostly handled by browsers, not common in REST interviews.

---

## 4xx – Client Error Responses

Indicates **problem with client request**.

Common 4xx codes:

400 Bad Request

- Invalid request data
- Missing or incorrect parameters

401 Unauthorized

- Authentication required
- Token missing or invalid

403 Forbidden

- Access denied
- Authenticated but not allowed

404 Not Found

- Resource does not exist

Interview Tip:  
4xx means → Client mistake

---

## 5xx – Server Error Responses

Indicates **problem at server side**.

Common 5xx codes:

500 Internal Server Error

- Generic server failure

502 Bad Gateway

- Invalid response from upstream server

503 Service Unavailable

- Server temporarily unavailable

Interview Tip:  
5xx means → Server issue

---

## Difference Between 4xx and 5xx (Very Important)

4xx:

- Client sent wrong request
- Client must fix request

5xx:

- Server failed to process valid request
- Backend issue

This difference is frequently asked in interviews.

---

## REST API Design Basics

Good REST APIs:

- Use meaningful URLs
- Use correct HTTP methods
- Return proper status codes
- Provide clear error responses

Bad APIs:

- Always return 200
- Use GET for data modification
- Hide errors inside response body

---

## Example API Response Design

Success response:

- Status: 200
- Body: Data

Error response:

- Status: 400 / 404 / 500
- Body: Error message

Status code should reflect **actual result**, not just success.

---

## Java Backend Perspective

In Java (Spring Boot):

- Status codes are returned using:
  - ResponseEntity
  - @ResponseStatus

Spring automatically maps:

- Exceptions → status codes
- Controller responses → HTTP responses

Proper status handling shows **professional backend design**.

---

## Common Interview Questions

- What are HTTP status codes?
- Difference between 200 and 201?
- When do you use 400 vs 404?
- Difference between 401 and 403?
- Difference between 4xx and 5xx?
- Why status codes are important in APIs?

---

## Common Beginner Mistakes

- Returning 200 for every response
- Using wrong status codes
- Ignoring error handling
- Mixing client and server errors

Avoid these mistakes in interviews.

---

## Day 04 Summary

- Status codes describe API results
- Correct usage improves API quality
- 2xx → Success
- 4xx → Client error
- 5xx → Server error
- Essential for Java backend interviews

---
