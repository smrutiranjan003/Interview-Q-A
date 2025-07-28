
# 💡 Java + MySQL Interview Questions & Answers for Freshers

This guide contains 50 essential questions and answers that commonly appear in Java + MySQL interviews for freshers.

---

## 🟩 Java Basics

### 1. What is Java?
Java is a high-level, object-oriented programming language known for its portability, security, and strong memory management.

### 2. What is the JDK?
JDK (Java Development Kit) is a software development kit that includes the JRE, compiler (`javac`), and tools like `javadoc`.

### 3. What is the JVM?
JVM (Java Virtual Machine) provides the runtime environment to execute Java bytecode.

### 4. What is JRE?
JRE (Java Runtime Environment) includes JVM and libraries required to run Java programs.

### 5. What are the features of Java?
- Simple
- Object-Oriented
- Platform Independent
- Secure
- Robust
- Multithreaded
- High Performance

---

## 🟦 JDBC & MySQL

### 6. What is JDBC?
JDBC (Java Database Connectivity) is an API for connecting and executing queries with databases from Java.

### 7. What are JDBC drivers?
JDBC drivers are implementations for connecting Java apps to databases. Types:
- JDBC-ODBC Bridge
- Native API
- Network Protocol
- Thin Driver

### 8. How do you connect to MySQL using JDBC?
```java
Class.forName("com.mysql.cj.jdbc.Driver");
Connection con = DriverManager.getConnection(url, user, password);
````

### 9. What is a ResultSet?

A ResultSet is a table of data returned by executing a SQL query.

### 10. What are Statement and PreparedStatement?

* `Statement`: Executes static SQL queries.
* `PreparedStatement`: Executes parameterized, precompiled queries (faster and safer).

### 11. How do you prevent SQL injection in JDBC?

Use `PreparedStatement` to bind parameters securely.

### 12. What is `Class.forName` used for?

It loads and registers the JDBC driver class dynamically.

### 13. What is a transaction in JDBC?

A transaction is a group of operations treated as a single unit of work.

### 14. How do you handle transactions in JDBC?

```java
conn.setAutoCommit(false);
conn.commit(); // or conn.rollback();
```

### 15. What is the use of DriverManager?

Manages a list of JDBC drivers and establishes DB connections.

### 16. How do you handle exceptions in JDBC?

Using `try-catch` blocks and catching `SQLException`.

### 17. Difference between `executeQuery()` and `executeUpdate()`?

* `executeQuery()` for SELECT
* `executeUpdate()` for INSERT, UPDATE, DELETE

### 18. What is a connection pool?

A pool of DB connections reused to improve performance.

---

## 🟨 Java OOP & Core Concepts

### 19. What is a Java Bean?

A JavaBean is a reusable component with:

* No-arg constructor
* Getters and setters
* Serializable

### 20. What are access modifiers?

Keywords that define scope: `public`, `private`, `protected`, and default.

### 21. What is inheritance?

Mechanism to acquire properties and methods of another class using `extends`.

### 22. What is polymorphism?

Ability of a method to behave differently based on the object.

* Compile-time: Overloading
* Runtime: Overriding

### 23. What is encapsulation?

Binding data and methods together in a class and controlling access with modifiers.

### 24. What is abstraction?

Hiding internal implementation and showing only necessary details.

### 25. What is an interface?

A reference type with abstract methods and constants.

### 26. Difference between interface and abstract class?

* Interface: all methods are abstract (till Java 8).
* Abstract class: can have both abstract and concrete methods.

### 27. What is method overloading?

Defining multiple methods with the same name but different parameters.

### 28. What is method overriding?

Redefining a parent class method in a subclass with the same signature.

### 29. What is a constructor?

A special method called during object creation to initialize the object.

### 30. What is the `final` keyword?

Used to:

* Make a variable constant
* Prevent method overriding
* Prevent class inheritance

### 31. What is a package in Java?

A namespace that organizes related classes and interfaces.

---

## 🟪 Exception Handling, Threads, Collections

### 32. What is exception handling?

Managing runtime errors using `try`, `catch`, `finally`, and `throw`.

### 33. Difference between checked and unchecked exceptions?

* Checked: Checked at compile time (`IOException`)
* Unchecked: At runtime (`NullPointerException`)

### 34. What is the use of finally block?

Code inside `finally` always executes after try-catch.

### 35. What is a thread in Java?

A lightweight process used for multitasking. Created using `Thread` or `Runnable`.

### 36. What is synchronization?

A way to control thread access to shared resources.

### 37. Difference between `==` and `equals()`?

* `==`: compares references
* `equals()`: compares content

### 38. What is a HashMap?

A key-value pair collection that allows one `null` key and multiple `null` values.

### 39. What is a List in Java?

An ordered collection that allows duplicates.
Examples: `ArrayList`, `LinkedList`.

### 40. Purpose of `toString()` method?

Returns a string representation of the object.

### 41. What is garbage collection?

Automatic memory management — destroys unused objects.

### 42. What is the use of `super` keyword?

Used to refer to the parent class and its constructor/methods.

---

## 🟥 MySQL Concepts

### 43. Types of joins in MySQL?

* `INNER JOIN`
* `LEFT JOIN`
* `RIGHT JOIN`
* `FULL JOIN` (via UNION)
* `CROSS JOIN`
* `SELF JOIN`

### 44. What is normalization?

Organizing data to minimize redundancy and improve integrity.

### 45. What is a primary key?

A column (or combination) that uniquely identifies rows.

### 46. What is a foreign key?

A column that references the primary key of another table.

### 47. How do you execute a stored procedure in JDBC?

Using `CallableStatement` and `execute()` or `executeQuery()`.

### 48. What is SQL injection?

A security issue where attackers modify SQL queries via input fields.

### 49. How to improve JDBC performance?

* Connection pooling
* Batch processing
* Use `PreparedStatement`
* Optimize queries

### 50. What is indexing in MySQL?

Improves read performance by creating quick lookup data structures. Uses additional memory.

---

📘 **Tip for Freshers**:

* Master Java fundamentals first
* Practice basic JDBC CRUD operations
* Learn SQL joins and subqueries
* Write code to connect Java with MySQL locally

```
