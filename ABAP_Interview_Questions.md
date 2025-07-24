# 💼 SAP ABAP Interview Questions & Answers

Your one-stop guide to beginner-level ABAP interview preparation. This list covers key Data Dictionary, SAP HANA, and programming concepts commonly asked during interviews for fresher and junior ABAP roles.

---

## 1. How to create a Table? What parameters should we consider?

To create a table in SE11 (Data Dictionary):
- Go to SE11 → Enter name → Choose "Database Table" → Create.
- Set:
  - **Delivery Class** (e.g., A for Application data)
  - **Data Class** (e.g., APPL0, APPL1)
  - **Size Category**
  - **Fields**: Name, Data Element, Key fields
  - **Technical settings**: Buffering, logging
  - **Primary Key**

---

## 2. What is a Transparent Table and Cluster Table?

- **Transparent Table**: Directly corresponds to a single DB table, 1:1 relationship.
- **Cluster Table**: Logical tables stored together in a single physical table. Optimized for performance in storing similar data.

---

## 3. Difference: Transparent vs Pool vs Cluster Table?

| Feature         | Transparent         | Pooled             | Cluster            |
|-----------------|---------------------|---------------------|--------------------|
| DB Representation | 1:1 with DB table | Many-to-1           | Many-to-1          |
| Access Speed     | High               | Moderate            | High               |
| Used For         | App data (Master/Trans.) | Internal control | Clustered data storage |

---

## 4. What is Data Element and Domain?

- **Domain**: Technical type – defines data type, length, and value range.
- **Data Element**: Semantic layer – describes the meaning, field labels, and documentation.

---

## 5. Master Data vs Transaction Data?

- **Master Data**: Static information (e.g., Customer, Material).
- **Transaction Data**: Day-to-day operations (e.g., Sales Orders, Invoices).

---

## 6. What is a SELECT query? Syntax?

Used to read records from DB tables.

```abap
SELECT * FROM ztable INTO TABLE @DATA(lt_data).
````

---

## 7. What is Internal Table and Work Area?

* **Internal Table**: In-memory table to store multiple records.
* **Work Area**: Single row buffer used for processing one record at a time.

---

## 8. Hello World Program in ABAP

```abap
REPORT zhello_world.
WRITE: 'Hello World'.
```

Run via **SE38** or **SA38**.

---

## 9. What is a Transaction Code (T-Code)?

A shortcut to launch a specific task or screen. E.g., SE11, SE80, VA01.

---

## 10. Types of Data Tables in SAP?

* Transparent Tables
* Pooled Tables
* Cluster Tables
* Buffer Tables
* Temporary Tables

---

## 11. What is a Selection Screen?

User input screen for parameters and select-options.

```abap
PARAMETERS: p_matnr TYPE matnr.
```

---

## 12. Events in ABAP Report Program?

* `INITIALIZATION`
* `AT SELECTION-SCREEN`
* `START-OF-SELECTION`
* `END-OF-SELECTION`
* `TOP-OF-PAGE`, `END-OF-PAGE`

---

## 13. What is a Selection Screen?

It's the input area where users provide selection criteria for reports.

---

## 14. What is LOOP in ABAP?

Iterates over internal tables.

```abap
LOOP AT lt_data INTO ls_data.
  WRITE: / ls_data-field.
ENDLOOP.
```

---

## 15. What is a SAP HANA Database Table?

Columnar, in-memory database table used in HANA optimized scenarios.

---

## 16. What is a Primary Key?

Unique identifier(s) for a record in the table. It avoids duplication.

---

## 17. Client Dependent vs Independent Tables?

* **Client Dependent**: First field is `MANDT` (client).
* **Client Independent**: No MANDT field; shared across all clients.

---

## 18. How to identify Client Dependent table?

If the first field is `MANDT`, it's client-dependent.

---

## 19. Types of Joins in ABAP?

* INNER JOIN
* LEFT OUTER JOIN
* RIGHT OUTER JOIN (rare)
* FOR ALL ENTRIES (FAE)

```abap
SELECT a~field1 b~field2 FROM ztable1 AS a INNER JOIN ztable2 AS b ON a~id = b~id INTO TABLE @DATA(result).
```

---

## 20. What is Delivery Class and Data Class?

* **Delivery Class**: Controls transport behavior.

  * A: App data, C: Customizing
* **Data Class**: Controls physical storage location.

---

## 21. How to insert data into a table?

```abap
INSERT ztable FROM ls_data.
```

---

## 22. What is HANA?

High-Performance Analytic Appliance – SAP's in-memory database that stores and processes data in RAM.

---

## 23. What is Code Push Down in HANA?

Push logic to DB layer using CDS Views, AMDPs, instead of ABAP loops. Increases performance.

---

## 24. Types of Enhancements?

* User Exits
* Customer Exits
* BADI
* Implicit & Explicit Enhancements
* Enhancement Spots

---

## 25. Types of Views in DDIC?

* Database View
* Projection View
* Maintenance View
* Help View
* CDS View (Core Data Services)

---

## 26. Why CDS in ABAP?

* Push logic to DB layer
* Improved performance
* Data modeling with annotations
* Simplifies access to related data

---

## 27. Why use Reports in SAP?

To extract, analyze, and display data for business insights. Includes ALV, classical reports.

---

📘 **Bonus Tip**: Practice writing SELECT queries, using loops, and building simple reports using SE38/SE80.

---

👨‍💻 Created by: [Smruti Ranjan](https://github.com/smrutiranjan003)

````
