# 💼 SAP ABAP Interview Questions & Answers

Your one-stop guide to beginner-level ABAP interview preparation. This list covers key Data Dictionary, SAP HANA, and programming concepts commonly asked during interviews for fresher and junior ABAP roles.

---

## 1. How to create a Table? What parameters should we consider?

To create a table in SE11 (Data Dictionary) in ABAP:
- Go to transaction **SE11** → Enter name → Choose *Database Table* → Click *Create*.
- Important settings:
  - **Delivery Class** (e.g., A for Application data)
  - **Data Class** (e.g., APPL0, APPL1)
  - **Size Category**
  - **Fields**: Add field name, data element, mark primary key fields
  - **Technical settings**: Set *Data Class*, *Size Category*, enable *Buffering*
  - **Primary Key**
  - **Save and activate**

📌 *Explain to interviewer:* “I make sure to define the key fields, choose correct technical settings, and activate the table properly.”

---

## 2. What is a Transparent Table and Cluster Table?

- **Transparent Table**: 1:1 mapping with DB table. Common for master/transaction data.
- **Cluster Table**: Combines multiple logical tables into one physical table for performance optimization.

---

## 3. Difference: Transparent vs Pool vs Cluster Table

| Type        | Structure          | Use Case           |
|-------------|--------------------|---------------------|
| Transparent | 1:1 with DB        | Master/Trans. Data |
| Pooled      | Many:1 (grouped)   | Internal data (texts, logs) |
| Cluster     | Many:1 (compressed)| Similar grouped data |

---

## 4. What is Domain and Data Element?

- **Domain**: Defines *technical type* (length, type, value range)
- **Data Element**: Adds *semantic meaning* like field label, documentation

📌 “Domain controls how data is stored; data element controls how it's displayed.”

---

## 5. What is Master Data vs Transaction Data?

- **Master Data**: Constant info (e.g., Material, Vendor)
- **Transaction Data**: Daily activities (e.g., Sales Orders, Deliveries)

---

## 6. What is SELECT query? Syntax?

Used to fetch records from tables.

```abap
SELECT * FROM zemployee INTO TABLE @DATA(lt_emp).
````

---

## 7. What is Internal Table and Work Area?

* **Internal Table**: Holds multiple rows temporarily in memory
* **Work Area**: Single row used for operations (like buffer)

---

## 8. Simple ABAP "Hello World" Program

```abap
REPORT zhello_world.
WRITE: 'Hello World'.
```

📌 Run in **SE38** or **SA38**

---

## 9. What is a Transaction Code (T-Code)?

A shortcut to access SAP functionality.
Examples:

* SE11 → Data Dictionary
* SE38 → Program Editor
* VA01 → Create Sales Order

---

## 10. Types of Tables in SAP

* Transparent Table
* Pooled Table
* Cluster Table
* Temporary Table
* Buffer Table

---

## 11. What is a Selection Screen?

It’s where user gives input before running the program.

```abap
PARAMETERS: p_matnr TYPE matnr.
```

---

## 12. Events in ABAP Reports

* **INITIALIZATION**: Before screen loads
* **AT SELECTION-SCREEN**: Validations
* **START-OF-SELECTION**: Main logic
* **END-OF-SELECTION**: Final actions
* **TOP-OF-PAGE**: Page headers

---

## 13. Difference: Selection Screen vs Report Output

* *Selection Screen*: Input area
* *Report Output*: Output after logic is executed

---

## 14. What is a LOOP in ABAP?

Used to process internal table line-by-line.

```abap
LOOP AT lt_emp INTO ls_emp.
  WRITE: / ls_emp-name.
ENDLOOP.
```

---

## 15. What is a SAP HANA Table?

HANA tables are:

* Column-based
* In-memory
* Faster than classic DB tables
  Used in modern SAP systems (S/4HANA).

---

## 16. What is a Primary Key?

* Uniquely identifies each row
* Avoids duplicate entries

---

## 17. Client Dependent vs Client Independent Tables

* **Client Dependent**: First field is *MANDT*
* **Client Independent**: No MANDT field, shared across all clients

---

## 18. How to check if a table is client dependent?

If MANDT exists as the first key field, then it is **client dependent**.

---

## 19. Types of Joins in ABAP

* **INNER JOIN**
* **LEFT OUTER JOIN**
* **RIGHT OUTER JOIN**
* **FOR ALL ENTRIES** (FAE)

Example:

```abap
SELECT a~id b~name
  FROM ztable1 AS a
  INNER JOIN ztable2 AS b
  ON a~id = b~id
  INTO TABLE @DATA(lt_result).
```

---

## 20. Delivery Class vs Data Class

* **Delivery Class**: Transport behavior (A = App data, C = Customizing)
* **Data Class**: Physical storage location (APPL0, APPL1)

---

## 21. How to insert data in a table?

```abap
INSERT ztable FROM ls_data.
```

---

## 22. What is SAP HANA?

* In-memory DB
* Super fast read/write
* Used in SAP S/4HANA systems

---

## 23. What is Code Push Down?

Instead of processing logic in ABAP (slow), we shift it to HANA DB using:

* CDS Views
* AMDPs

Faster performance!

---

## 24. Types of Enhancements in ABAP

* **User Exits**
* **Customer Exits**
* **BADIs**
* **Implicit/Explicit Enhancements**
* **Enhancement Spots**

---

## 25. Types of Views in Data Dictionary

* **Database View**
* **Projection View**
* **Help View**
* **Maintenance View**
* **CDS View**

---

## 26. Why use CDS Views?

* Better performance (code pushdown)
* DB-level joins, filters, associations
* Simplifies UI5/Fiori apps

---

## 27. Why create Reports in SAP?

To:

* Display business data
* Analyze records
* Automate processes (e.g., ALV reports, Classic reports)

---

## 📘 Bonus Tips

✅ Practice writing `SELECT`, `LOOP`, and building small reports

✅ Learn how to navigate SE11, SE38, SE80 confidently

✅ Understand internal tables, joins, and views

---

## 👨‍💻 Created By:

**Smruti Ranjan Mohapatra**
GitHub: [@smrutiranjan003](https://github.com/smrutiranjan003)

---
