# 📄 INTERVIEW PREPARATION DOCUMENT

---

## 1. Tell Me About Yourself
I'm currently pursuing my BTech in [Your Branch] from [Your College]. I have a strong interest in technology and software development. I've recently been learning SAP ABAP and also exploring stock trading in my free time. I enjoy taking on new challenges and believe in continuous learning. I'm looking forward to applying my skills and growing with a company like HCL.

---

## 2. Tell Me About Your Project Step-by-Step

During my training, I built an Employee Master application using the RAP (RESTful Application Programming) model.

1. **Database Table**: Created ZTB_RAP_EMP_887 with employee details (ID, Name, Address, Department).
2. **CDS Views**:
   - Root View Entity
   - Projection View with UI annotations like `@UI.lineItem`, `@UI.selectionField`
3. **Behavior Definition**:
   - Enabled Create, Update, Delete with managed implementation
4. **Service Definition and Binding**:
   - Exposed CDS views via OData V4
   - Integrated with Fiori Elements (List Report/Object Page)
5. **Deployment**:
   - Deployed to SAP BTP Cloud Foundry via Eclipse ADT

This gave me end-to-end RAP hands-on experience including backend logic and frontend exposure.

---

## 3. Types of CDS Views?
- **ABAP CDS Views**: 
  - Basic View 
  - Composite View 
  - Consumption View
- **HANA CDS Views**

---

## 4. Types of Internal Tables?
- Standard Table
- Sorted Table
- Hashed Table

---

## 5. What is Data Dictionary?
Data Dictionary is a central repository for metadata and schema definition in SAP. Used to define tables, views, types, and relationships.

---

## 6. How Do We Create a Database Table?
**Path**: Package → Other ABAP Repository Object → Dictionary → Database Table

---

## 7. Use of Behavior and Service Definition?

| Layer               | Purpose                                               |
|--------------------|--------------------------------------------------------|
| CDS Entity          | Defines table/data model                              |
| Behavior Definition | Business logic (Create/Update/Delete)                 |
| Service Definition  | Expose specific CDS views                             |
| Service Binding     | Activate service (OData V4)                           |

---

## 8. How to Create a Table (Parameters to Consider)?
Via Eclipse → New → Database Table
- Fields (ID, Name, Email)
- Primary Key
- Technical Settings (buffering, logging)
- Delivery Class, Data Class, Size Category

---

## 9. Transparent vs Cluster Table
- **Transparent**: 1:1 mapping with DB table
- **Cluster**: Obsolete in HANA, used for grouped tables

---

## 10. Transparent vs Pooled vs Cluster Table

| Type         | Mapping     | Usage                      |
|--------------|-------------|----------------------------|
| Transparent  | 1:1         | Common data                |
| Pooled       | Many:1      | Internal, control tables   |
| Cluster      | Many:1      | Logical grouped tables     |

---

## 11. Data Element vs Domain

| Concept       | Role                                       |
|---------------|--------------------------------------------|
| Domain        | Technical attributes (type, length)        |
| Data Element  | Semantic meaning (field label, doc)        |

---

## 12. Master Data vs Transactional Data

- **Master Data**: Static, reused (e.g., Employee)
- **Transactional Data**: Dynamic, day-to-day (e.g., Sales)

---

## 13. SELECT Query Syntax

```abap
SELECT * FROM zemployee INTO TABLE @DATA(it_emp).
LOOP AT it_emp INTO DATA(wa_emp).
  WRITE: / wa_emp-emp_id, wa_emp-name.
ENDLOOP.
```

---

## 14. Internal Table vs Work Area

```abap
DATA: it_emp TYPE TABLE OF zemployee,
      wa_emp TYPE zemployee.
```

---

## 15. ABAP Program to Print Hello World

```abap
REPORT z_hello_world.
WRITE: 'Hello World'.
```

---

## 16. What is a Transaction Code?

Shortcode to access SAP functionality
- SE11: Data Dictionary
- SE38: ABAP Editor
- SE80: Object Navigator

---

## 17. Types of Tables in SAP

- Transparent
- Pooled
- Cluster

---

## 18. What is a Selection Screen?

Used for user inputs before processing

```abap
PARAMETERS: p_id TYPE zemp_id.
```

---

## 19. Events in ABAP Program

- INITIALIZATION
- AT SELECTION-SCREEN
- START-OF-SELECTION
- END-OF-SELECTION

---

## 20. LOOP Statement

```abap
LOOP AT it_emp INTO DATA(wa).
  WRITE: / wa-name.
ENDLOOP.
```

---

## 21. SAP HANA DB Table

- In-memory
- Columnar
- Real-time analytics

---

## 22. Primary Key in Table

Uniquely identifies each record; avoids duplicates

---

## 23. Client-Dependent vs Client-Independent

- Client-Dependent: Field `MANDT` present
- Client-Independent: No `MANDT` field

---

## 24. Types of Joins

| Join Type       | Description                                     |
|-----------------|-------------------------------------------------|
| INNER JOIN      | Only matching records                           |
| LEFT OUTER JOIN | All left + matched right records                |
| RIGHT OUTER JOIN| All right + matched left records (rare)         |

---

## 25. Delivery Class and Data Class

- **Delivery Class**: Controls transport between systems
- **Data Class**: Defines physical DB storage

---

## 26. How to Insert Data in Table

```abap
DATA(wa_emp) = VALUE zemployee( emp_id = 'E101' name = 'John Doe' ).
INSERT zemployee FROM wa_emp.
```

---

## 27. What is SAP HANA?

High-performance in-memory DB for real-time applications.

---

## 28. Code Pushdown

Move logic to DB layer using:
- CDS Views
- AMDPs

---

## 29. Types of Enhancements

- User Exits
- Customer Exits
- BADIs
- Enhancement Points

---

## 30. Types of Views in Data Dictionary

| View Type       | Description                                           |
|------------------|------------------------------------------------------|
| Database View    | Join of transparent tables                           |
| Projection View  | Subset of table fields                               |
| Maintenance View | Table maintenance UI                                 |
| Help View        | Used in Search Helps                                 |

---

## 31. Why CDS in ABAP?

- Modeling
- Annotation
- Reuse
- DB-level execution (pushdown)

---

## 32. Use of Reports

- Data extraction
- Analysis
- Business reporting

---

## 33. Foreign Key

- Links two tables
- Enforces referential integrity
- Points to Primary Key of another table

---

## 34. OOPs Concepts

- **Polymorphism**: Same object, different behaviors
- **Inheritance**: Child class inherits parent
- **Abstraction**: Hide complexity, expose necessary

---

## 35. ABAP Cloud Project

**Path**: File → New → ABAP Cloud Project  
Used for BTP and S/4HANA Cloud development (SE80 not supported)

---
