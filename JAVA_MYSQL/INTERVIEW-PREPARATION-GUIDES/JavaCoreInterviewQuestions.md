
# Java Core Interview Questions – Complete Guide

## 📘 Core Concepts (Q1–25)

### 1. What are static blocks and static initializers in Java?
Static blocks run once when the class is loaded. Used to initialize static variables.

### 2. How do you call one constructor from another constructor in Java?
Use `this()` keyword inside the constructor.

### 3. What is method overriding in Java?
When a subclass provides a specific implementation of a method already defined in its superclass.

### 4. What is the `super` keyword in Java?
Refers to the immediate parent class. Used to access parent methods or constructors.

### 5. What is the difference between method overloading and method overriding in Java?
Overloading: same method name, different parameters (compile-time).  
Overriding: same method name and parameters in subclass (run-time).

### 6. What is the difference between an abstract class and an interface?
Abstract class: can have variables, constructors, and partial implementation.  
Interface: full abstraction, Java 8+ allows default/static methods.

### 7. Why is Java platform-independent?
Java compiles code to bytecode, which runs on the JVM on any OS.

### 8. What is method overloading in Java?
Multiple methods with the same name but different parameters.

### 9. What is the difference between C++ and Java?
Java is platform-independent, garbage collected, and pointer-free.  
C++ is platform-dependent and uses manual memory management.

### 10. What is the JIT compiler in Java?
Just-In-Time compiler converts bytecode to native machine code at runtime for better performance.

### 11. What is bytecode in Java?
Intermediate code compiled from source code, executed by the JVM.

### 12. What is the difference between `this()` and `super()` in Java?
`this()` calls the current class's constructor.  
`super()` calls the parent class's constructor.

### 13. What is a class in Java?
A template or blueprint used to create objects.

### 14. What is an object in Java?
An instance of a class with its own state and behavior.

### 15. What is a method in Java?
A block of code that performs a specific task, possibly returning a value.

### 16. What is encapsulation in Java?
Wrapping data (variables) and methods inside a class; access controlled via modifiers.

### 17. Why is the `main()` method public, static, and void in Java?
`public`: globally accessible  
`static`: runs without object creation  
`void`: doesn’t return a value

### 18. Explain the `main()` method in Java.
The starting point of a Java application:  
```java
public static void main(String[] args)
````

### 19. What is a constructor in Java?

A special method that initializes objects. No return type and same name as class.

### 20. What is the difference between `length` and `length()` in Java?

`length` is a property for arrays.
`length()` is a method for strings.

### 21. What is ASCII code?

A 7-bit character set for English characters (0–127).

### 22. What is Unicode?

A universal character encoding system supporting most languages.

### 23. What is the difference between a character constant and a string constant in Java?

Character constant: `'A'` (char)
String constant: `"A"` (String)

### 24. What are constants and how do you create them in Java?

Constants are final variables declared using the `final` keyword.
Example: `final int MAX = 100;`

### 25. What is the difference between `>>` and `>>>` operators in Java?

`>>` is signed right shift.
`>>>` is unsigned right shift (fills leftmost bits with 0).

---

## 📗 Java Coding Standards (Q26–30)

### 26. What are the Java coding standards for classes?

Class names should use PascalCase and be nouns (e.g., `StudentData`).

### 27. What are the Java coding standards for interfaces?

Use PascalCase, often naming them as capabilities (`Runnable`, `Serializable`).

### 28. What are the Java coding standards for methods?

Use camelCase, starting with a verb (`calculateSalary()`).

### 29. What are the Java coding standards for variables?

Use camelCase, meaningful names (`studentAge`).

### 30. What are the Java coding standards for constants?

Use UPPER\_CASE with underscores (`MAX_SPEED`).

---

## 📙 Inheritance and Relationships (Q31–47)

### 31. What is the difference between method overriding and method overloading?

Overloading: same method name, different parameters.
Overriding: same method, subclass provides new implementation.

### 32. What is the IS-A relationship in Java?

Represents inheritance. Example: Dog IS-A Animal.

### 33. What is the HAS-A relationship in Java?

Represents composition. Example: Car HAS-A Engine.

### 34. What is the difference between IS-A and HAS-A relationships in Java?

IS-A is inheritance; HAS-A is composition/aggregation.

### 35. What is the `instanceof` operator in Java?

Checks if an object is an instance of a class/subclass.
Example: `if (obj instanceof String)`

### 36. What does `null` mean in Java?

It indicates a reference that doesn't point to any object.

### 37. Can we have multiple classes in a single file in Java?

Yes, but only one public class is allowed per file.

### 38. What access modifiers are allowed for a top-level class in Java?

`public` and default (package-private) only.

### 39. What are packages in Java?

A way to group related classes and interfaces into namespaces.

### 40. Can we have more than one package statement in a source file in Java?

No, only one package statement is allowed and it must be the first line.

### 41. Can we define a package statement after an import statement?

No, package statement must come before all import statements.

### 42. What are identifiers in Java?

Names used for classes, methods, variables, etc.

### 43. What are access modifiers in Java?

Control access: `public`, `private`, `protected`, and default.

### 44. What is the difference between access specifiers and access modifiers?

Used interchangeably, but "access modifiers" is the official Java term.

### 45. What access modifiers can be used for classes in Java?

`public` and default (package-private).

### 46. What access modifiers can be used for methods in Java?

All: `public`, `protected`, `private`, default.

### 47. What access modifiers can be used for variables in Java?

All: `public`, `protected`, `private`, default.

---

## 📕 Advanced Concepts (Q48–52)

### 48. What is the `final` access modifier in Java?

* Final variable: constant
* Final method: can't be overridden
* Final class: can't be extended

### 49. What are abstract classes in Java?

Classes that can't be instantiated; may contain abstract and non-abstract methods.

### 50. Can we create a constructor in an abstract class?

Yes, it’s used during object creation via subclass.

### 51. What are abstract methods?

Methods without a body; must be overridden by subclasses.

### 52. What is an exception in Java?

A runtime error that disrupts normal execution flow.

---

## 📒 Exception Handling (Q53–69)

### 53. What are some situations where exceptions may arise in Java?

* Division by zero
* Null pointer access
* File not found
* Array index out of bounds

### 54. What is exception handling in Java?

A mechanism to catch and handle runtime errors using `try-catch-finally`.

### 55. What is an error in Java?

Serious issue (e.g., `OutOfMemoryError`) that can't be handled programmatically.

### 56. What are the advantages of exception handling in Java?

* Separates error-handling logic
* Prevents program from crashing
* Improves readability

### 57. In how many ways can we handle exceptions?

* Using try-catch
* Using `throws` keyword

### 58. What are five keywords related to exception handling?

`try`, `catch`, `finally`, `throw`, `throws`

### 59. What are the `try` and `catch` keywords in Java?

Used to handle exceptions. `try` wraps risky code, `catch` handles the error.

### 60. Can we have a `try` block without a `catch` block?

Yes, but only if it is followed by a `finally` block.

### 61. Can we have multiple `catch` blocks for a `try` block?

Yes, for handling different exception types.

### 62. What is the importance of the `finally` block?

Executes regardless of exception; used for cleanup.

### 63. Can we have any code between the `try` and `catch` blocks?

No, it’s a syntax error.

### 64. Can we have any code between the `try` and `finally` blocks?

No, nothing is allowed between them.

### 65. Can we catch more than one exception in a single `catch` block?

Yes, from Java 7 using pipe `|` (multi-catch block).

### 66. What are checked exceptions in Java?

Compile-time exceptions like `IOException`, `SQLException`.

### 67. What are unchecked exceptions in Java?

Runtime exceptions like `NullPointerException`, `ArithmeticException`.

### 68. What is the difference between checked and unchecked exceptions?

* Checked: must be declared/handled
* Unchecked: optional handling

### 69. What is default exception handling in Java?

If uncaught, the JVM handles the exception and prints a stack trace.

---

## 📎 License

This content is open for educational use and personal preparation.

```
