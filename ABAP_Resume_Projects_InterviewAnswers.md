
# 👨‍💻 SAP ABAP Resume Projects & Interview Answers

This file includes a structured summary of my ABAP profile, RAP project experience, core concepts, and HR/technical interview answers — perfect for GitHub portfolio and interviews.

---

## 🙋‍♂️ Tell Me About Yourself

"My name is **Smruti Ranjan Mohapatra**, a final-year B.Tech (CSE) student. I'm currently undergoing **SAP ABAP training under Skill Odisha**.

During my training, I built a complete **Employee Master RAP application** using **CDS**, **behavior definition**, and **OData V4**, which I successfully **deployed on SAP BTP Cloud Foundry**. I enjoy backend development and exploring new SAP technologies."

---

## 🚀 Real Project Experience: Employee Master App (RAP Model)

### 🔧 Tech Stack Used
- CDS Views
- Behavior Definition (Managed)
- Service Definition & Binding (OData V4)
- Fiori Elements
- SAP BTP Cloud Foundry
- Eclipse ADT

### 📌 Steps Taken

1. **Created DB Table**:  
   `ZTB_RAP_EMP_887` with fields like `EmpID`, `Name`, `Address`, `Dept`.

2. **CDS Root View & Projection View**:  
   Used annotations like `@UI.lineItem`, `@UI.selectionField`.

3. **Behavior Definition & Implementation**:  
   Defined CRUD operations with `managed implementation`.

4. **Service Definition & Binding**:  
   Created `ZUI_EMP_SRV`, exposed via OData V4.

5. **Fiori Integration**:  
   Used Fiori List Report + Object Page templates.

6. **Deployment**:  
   Used **"Deploy to SAP BTP"** via Eclipse ADT.

### 🧠 What I Learned
This project helped me understand:
- End-to-end RAP architecture
- Cloud deployment via SAP BTP
- CDS annotations & Fiori integration

---

## 📚 Mini Project Experience

- **ALV Report**: Displayed `MARA` data using `REUSE_ALV_GRID_DISPLAY`.
- **CDS + OData**: Built a CDS View → Exposed via `@OData.publish: true` → Registered in `/IWFND/MAINT_SERVICE`.

---

## ✅ Core ABAP Concepts & Syntax

### 1. DATA vs TYPES
- `DATA`: Declare variables  
- `TYPES`: Define custom types/structures

### 2. FORM vs Function Module
- `FORM`: Local subroutines  
- `FUNCTION MODULE`: Global, reusable, with exceptions (SE37)

### 3. ALV Report
- Used for interactive output  
- Supports sorting, totals, filtering

```abap
CALL FUNCTION 'REUSE_ALV_GRID_DISPLAY'
  EXPORTING i_structure_name = 'ZEMPLOYEE'
  TABLES t_outtab = lt_employee.
````

### 4. Debugging in ABAP

* Use `/h` in command field to enter debugger
* Set breakpoints
* Step through using F5 (step in), F6 (step over), F7 (return)

---

## ✅ Common ABAP Syntax

### SELECT

```abap
SELECT * FROM ztb_employee INTO TABLE lt_employee.
```

### LOOP

```abap
LOOP AT lt_employee INTO ls_employee.
  WRITE: / ls_employee-name.
ENDLOOP.
```

### FORM

```abap
FORM display_data.
  WRITE: / 'Hello, SAP!'.
ENDFORM.
```

### Internal Table Declaration

```abap
DATA: lt_employee TYPE TABLE OF ztb_employee,
      ls_employee TYPE ztb_employee.
```

---

## 📘 CDS, OData & RAP Summary

### CDS (Core Data Services)

* Used for DB abstraction and semantic modeling.
* Views: **Root View**, **Projection View**, **Basic**, **Consumption**

```abap
@AbapCatalog.sqlViewName: 'ZCDS_VIEW'
@EndUserText.label: 'Material View'
define view ZCDS_Material as select from mara {
  matnr, ersda, mtart, matkl
}
```

### Expose CDS via OData

```abap
@OData.publish: true
define view ZI_EMPLOYEE as select from ZTB_EMPLOYEE
```

* Register in `/IWFND/MAINT_SERVICE`

### RAP (RESTful ABAP Programming)

* Modern framework to build Fiori-ready apps using:

  * **CDS Root View Entity**
  * **Behavior Definition (managed)**
  * **Service Definition & Binding**

```abap
define behavior for ZI_EMPLOYEE
persistent table ZTB_EMPLOYEE {
  create;
  update;
  delete;
}
```

```abap
define service ZUI_EMP_SRV {
  expose ZC_EMPLOYEE;
}
```

---

## ☁️ SAP BTP Deployment

* Right-click project → Deploy to SAP BTP (Cloud Foundry)
* Access app via Fiori Launchpad

---

## 🛠️ Debugging & Tools

* `/h` to trigger debugger
* Use **breakpoints**, **watch variables**, and **step logic**
* Useful in testing RAP behaviors and field values

---

## 📊 Reports in ABAP

### Classical Report

```abap
WRITE: / 'Employee Name:', lv_name.
```

### ALV Report

Interactive, professional-looking reports using:

* `REUSE_ALV_GRID_DISPLAY`
* SALV classes (Object-Oriented ALV)

---

## 🧠 ABAP Concept Summary

| Topic               | Notes                                                      |
| ------------------- | ---------------------------------------------------------- |
| **Internal Tables** | Standard, Sorted, Hashed                                   |
| **Modularization**  | FORM, FM, METHODS                                          |
| **Events**          | `INITIALIZATION`, `START-OF-SELECTION`, `END-OF-SELECTION` |
| **Enhancements**    | User Exits, BADIs, Implicit/Explicit                       |

---

## ❓ HR / Soft Skill Interview Answers

### Q: Tell me about yourself

> "My name is Smruti Ranjan Mohapatra, a B.Tech CSE final-year student. I'm training in SAP ABAP under Skill Odisha. I’ve built an Employee Master RAP app using CDS, behavior definition, and deployed it on SAP BTP. I enjoy backend development and learning new SAP technologies."

### Q: Why SAP?

> "SAP is a global ERP leader. It combines business logic with technical architecture. I enjoy its structured development flow using RAP, CDS, and Fiori."

### Q: A challenge you faced?

> "I initially struggled with CDS annotations. With documentation and hands-on practice, I overcame it and later helped peers understand it better."

### Q: Are you a team player?

> "Yes! I collaborated with peers to debug RAP logic, share learnings, and complete project tasks together."

---

## 👨‍💻 Author

**Smruti Ranjan Mohapatra**
📌 Final-Year B.Tech (CSE)
🎓 Skill Odisha – SAP ABAP Trainee
🌐 GitHub: [smrutiranjan003](https://github.com/smrutiranjan003)

---
