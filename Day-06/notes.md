# Day 06 – Monolithic vs Microservices Architecture

Topic: Architecture Comparison

---

1. STUDENT INFORMATION

---

Goal of Today:
Understand the difference between Monolithic and Microservices architecture.
Learn when to use each.
Prepare for architecture-based interview questions.

Why This Topic is Important:
This is one of the most commonly asked system design questions in interviews.
Almost every backend or system design interview includes this comparison.

---

2. WHAT YOU SHOULD PREPARE BEFORE READING

---

You should already know:

- What is System Architecture
- Basic Client-Server Model
- What is API
- What is Backend Application
- Basic understanding of Scaling

If not:
Revise Day 01 to Day 05 before moving forward.

---

3. MONOLITHIC ARCHITECTURE

---

Definition:
A Monolithic Architecture is a single unified application where all modules
(UI, Business Logic, Database Access) are tightly coupled and deployed together.

Structure:

Client → Single Application → Single Database

All features exist in one codebase.
One build.
One deployment.

Core Characteristics:

1. Single Codebase
2. Single Deployment Unit
3. Shared Database
4. Tightly Coupled Modules
5. Simple to Develop Initially

Advantages:

- Easy to develop for beginners
- Simple deployment
- Easier debugging
- No network communication between services
- Lower infrastructure cost initially

Disadvantages:

- Hard to scale specific modules
- Entire app redeployed even for small change
- Difficult for large teams
- Technology stack locked
- Risky deployments

When to Use:

- Small projects
- Startup MVP
- College projects
- Early stage products
- Limited team size

---

4. MICROSERVICES ARCHITECTURE

---

Definition:
Microservices Architecture is a design approach where an application is
divided into small independent services that communicate via APIs.

Structure:

Client → API Gateway → Multiple Services → Separate Databases

Each service:

- Has its own codebase
- Has its own database
- Is independently deployable

Core Characteristics:

1. Independent Services
2. Loosely Coupled
3. Separate Database per Service
4. Independent Deployment
5. Technology Diversity Allowed

Advantages:

- Independent scaling
- Faster deployments
- Fault isolation
- Better for large teams
- Flexibility in tech stack

Disadvantages:

- Complex architecture
- Network latency
- DevOps overhead
- Hard debugging
- Distributed system challenges

When to Use:

- Large scale applications
- High traffic systems
- Enterprise level systems
- Teams with strong DevOps knowledge
- Long-term scalable products

---

5. DIRECT COMPARISON (INTERVIEW READY)

---

Deployment:
Monolith → Single deployment
Microservices → Multiple independent deployments

Scaling:
Monolith → Scale entire application
Microservices → Scale individual services

Database:
Monolith → Shared database
Microservices → Separate database per service

Team Structure:
Monolith → Small team friendly
Microservices → Large team friendly

Failure Impact:
Monolith → Entire app may crash
Microservices → Only one service may fail

Complexity:
Monolith → Low complexity
Microservices → High complexity

---

6. MOST IMPORTANT INTERVIEW NOTES (1% FILTER)

---

If interviewer asks:
"Which architecture is better?"

Correct Answer:
There is no universally better architecture.
It depends on:

- Project size
- Team size
- Scalability needs
- Budget
- Timeline

Golden Rule:
Start with Monolith.
Move to Microservices when scaling becomes difficult.

Never suggest Microservices for small applications.
That shows lack of practical understanding.

---

7. COMMONLY ASKED INTERVIEW QUESTIONS

---

Q1: Why do companies move from Monolith to Microservices?
Answer:
To improve scalability, deployment speed, and team independence.

Q2: What are challenges in Microservices?
Answer:

- Service communication
- Data consistency
- Network failures
- Monitoring and logging

Q3: Can Microservices share database?
Answer:
No. Each service should have its own database.

Q4: Is Microservices always scalable?
Answer:
Yes, but only if properly designed.

---

8. ARCHITECTURE DECISION FRAMEWORK

---

Use Monolith If:

- Early stage startup
- Budget constraint
- Small team
- Low traffic
- Fast development needed

Use Microservices If:

- Rapid scaling required
- Independent teams
- High availability required
- Large traffic
- Long-term growth focus

---

9. REAL WORLD EXAMPLES

---

Monolithic:

- Early Facebook
- Early Instagram
- Many college ERP systems

Microservices:

- Netflix
- Amazon
- Uber
- Paytm
- Swiggy

---

10. QUICK REVISION SUMMARY

---

Monolith = Simple but hard to scale.
Microservices = Complex but highly scalable.

Interview Tip:
Always explain trade-offs.
Never give one-sided answers.

Architecture choice is a business decision,
not just a technical decision.

---

End of Day 06 Notes
