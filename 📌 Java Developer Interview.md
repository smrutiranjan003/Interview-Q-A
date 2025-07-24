
# 📌 Java Developer Interview – My Experience

Recently attended an interview for a **Java Developer** role and wanted to share the questions that were asked. I hope this helps others who are preparing for similar roles!

---

## 🕒 Duration
**~45 minutes**

## 🛠️ Topics Covered
- Core Java (Java 8)
- Stream API
- Multithreading
- Collections
- Microservices

---

## 🔹 Core Java Questions

1. **What are the features of Java 8?**
   - Lambda Expressions  
   - Stream API  
   - Functional Interfaces  
   - Optional Class  
   - Date and Time API  
   - Default and Static Methods in Interfaces  

2. **What is the Optional class?**
   - A container object used to contain not-null objects. Helps avoid `NullPointerException`.

3. **What is a Functional Interface?**
   - An interface with exactly one abstract method. E.g., `Runnable`, `Comparator`.

4. **What is a Lambda expression and its syntax?**
   - Lambda is an anonymous function used to implement functional interfaces.
   - Syntax: `(parameters) -> expression or { statements }`

5. **Create a Functional Interface and implement it**
   ```java
   @FunctionalInterface
   interface MyFunc {
       int operate(int a, int b);
   }

   public class Main {
       public static void main(String[] args) {
           MyFunc add = (a, b) -> a + b;
           System.out.println(add.operate(10, 5)); // Output: 15
       }
   }
````

6. **What is Serialization? What is serialVersionUID?**

   * Serialization is converting an object into a byte stream.
   * `serialVersionUID` ensures version compatibility during deserialization.

7. **Internal working of HashMap**

   * Uses an array of buckets, each bucket stores a linked list or tree.
   * Hashcode and equals method are used to store/retrieve keys.

8. **What is Multithreading? Different thread states?**

   * Allows concurrent execution. States: New, Runnable, Running, Blocked, Waiting, Timed Waiting, Terminated.

9. **What is Deadlock and how to prevent it?**

   * When two threads wait for each other’s resources.
   * Prevention: lock ordering, try-locks, timeout locks.

---

## 🔹 Stream API Questions

1. **Find a list of names starting with the letter 'A'**

   ```java
   names.stream()
        .filter(name -> name.startsWith("A"))
        .collect(Collectors.toList());
   ```

2. **Find the highest salaried employee from a list**

   ```java
   Optional<Employee> emp = employees.stream()
        .max(Comparator.comparing(Employee::getSalary));
   ```

3. **Return a Map with ID as key and salary as value from list of employees**

   ```java
   Map<Integer, Double> salaryMap = employees.stream()
        .collect(Collectors.toMap(Employee::getId, Employee::getSalary));
   ```

---

## 🔹 Microservices Questions

1. **What are the components of Microservices?**

   * API Gateway
   * Service Registry (Eureka)
   * Config Server
   * Discovery Client
   * Load Balancer
   * Circuit Breaker (Hystrix/Resilience4j)

2. **What is an API Gateway?**

   * Single entry point for client requests; handles routing, authentication, rate limiting.

3. **What is Service Discovery?**

   * Dynamic registration of services (like Eureka) so they can discover and communicate with each other.

4. **What is the use of a Circuit Breaker?**

   * Prevents service failure cascades by stopping calls to a failing service.

5. **Best way to store credentials needed by multiple services?**

   * Use **Spring Cloud Config Server** with encrypted values or external secrets manager (e.g., Vault, AWS Secrets Manager).

6. **How to log a response body along with HTTP status code after every API call?**

   * Implement a **custom filter/interceptor** or use **logging libraries** like Logback with HTTP logging middleware.

---

## ✅ Final Tip

If you're preparing for Java interviews, revise Java 8, practice with `Streams`, and get familiar with microservices architecture and Spring Boot concepts.


