# notes.md

# Day 14 – Core Java Cheat Sheet (Interview Rapid Revision)

────────────────────────────────────────────────────────

JAVA EXECUTION FLOW

.java → javac → .class → ClassLoader → Bytecode Verifier → JVM → Execution Engine → Output

JDK = JRE + Development Tools  
JRE = JVM + Core Libraries

Platform independence → Bytecode runs on any JVM

────────────────────────────────────────────────────────

JVM MEMORY STRUCTURE

Heap

- Objects
- Instance variables
- Shared across threads

Stack

- Method calls
- Local variables
- One per thread

Method Area

- Class metadata
- Static variables
- Runtime constant pool

PC Register

- Current executing instruction

Native Method Stack

- Native calls

────────────────────────────────────────────────────────

DATA TYPES

Primitive → value stored directly  
byte short int long float double char boolean

Non-Primitive → reference stored in stack, object in heap  
String, Array, Class, Interface

Default values (instance):
int → 0  
boolean → false  
reference → null

Local variables → no default value

────────────────────────────────────────────────────────

TYPE CASTING

Widening → automatic  
int → long

Narrowing → manual  
long → int

────────────────────────────────────────────────────────

CONTROL STATEMENTS

Selection
if  
if–else  
switch

Loop
for  
while  
do–while

Jump
break  
continue  
return

────────────────────────────────────────────────────────

OOP PILLARS

Encapsulation  
→ Data hiding  
→ Achieved using private + getters/setters

Inheritance  
→ IS-A relationship  
→ Code reusability

Polymorphism  
Compile-time → Method overloading  
Runtime → Method overriding

Abstraction  
→ Hiding implementation  
→ abstract class / interface

────────────────────────────────────────────────────────

CONSTRUCTOR FLOW

Object creation steps:

1. Memory allocation
2. Instance variables → default values
3. Constructor execution
4. Object reference returned

Rules:

- Same name as class
- No return type
- Called automatically

Types:
Default  
Parameterized

this() → constructor chaining

────────────────────────────────────────────────────────

KEYWORDS – INTERVIEW CORE

this

- Current object reference
- Call constructor
- Access instance variables

super

- Parent class reference
- Call parent constructor

static

- Belongs to class
- Loaded once
- Access without object

final
Variable → constant  
Method → cannot override  
Class → cannot inherit

────────────────────────────────────────────────────────

STATIC vs INSTANCE

Static

- Class level
- Single copy
- Stored in method area

Instance

- Object level
- Separate copy per object
- Stored in heap

────────────────────────────────────────────────────────

STRING MEMORY

String → immutable → stored in SCP

String str = "Java" → SCP  
String str = new String("Java") → Heap

StringBuilder → mutable → fast → non-thread-safe  
StringBuffer → mutable → thread-safe

────────────────────────────────────────────────────────

OVERLOADING vs OVERRIDING

Overloading

- Same method name
- Different parameters
- Compile-time
- In same class

Overriding

- Same signature
- Runtime polymorphism
- IS-A relationship required

────────────────────────────────────────────────────────

ACCESS MODIFIERS

private → same class  
default → same package  
protected → package + subclass  
public → everywhere

────────────────────────────────────────────────────────

OBJECT vs CLASS

Class → blueprint  
Object → instance

────────────────────────────────────────────────────────

INTERFACE vs ABSTRACT CLASS

Interface

- 100% abstraction
- Multiple inheritance
- Variables → public static final

Abstract class

- 0–100% abstraction
- Single inheritance
- Can have constructor

────────────────────────────────────────────────────────

MEMORY QUICK MAP

Stack → methods, local variables  
Heap → objects  
Method Area → static + metadata

────────────────────────────────────────────────────────

INTERVIEW RAPID QUESTIONS

Why Java is platform independent?  
Difference between JDK JRE JVM?  
Stack vs Heap?  
Why String is immutable?  
Can we override static method?  
Why main is static?  
Difference between overloading & overriding?  
Constructor vs method?

────────────────────────────────────────────────────────

1-MINUTE REVISION FLOW

JVM → Memory → OOP → Constructor → Keywords → String → Access Modifiers → Polymorphism
