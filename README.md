# Database Normalization Assignment

 📌 Overview
This repository contains solutions for a Database Management Systems (DBMS) assignment on **Database Normalization**. The assignment demonstrates how to identify normalization issues in database tables and convert them into higher normal forms to reduce redundancy and improve data integrity.

## 📖 Topics Covered
- First Normal Form (1NF)
- Second Normal Form (2NF)
- Third Normal Form (3NF)
- Partial Dependency
- Transitive Dependency
- Database Decomposition
- Reducing Data Redundancy
- Improving Database Design

## 📂 Assignment Contents

### 1. Employee Table Normalization
**Original Table**
```
EMPNO, ENAME, SAL, DEPTNO, DNAME, LOC
```

#### Analysis
- Table is in **1NF**
- Table is in **2NF**
- Not in **3NF** due to transitive dependency:
  - `DEPTNO → DNAME, LOC`

#### Converted Tables
**Employee**
```
EMPNO (PK)
ENAME
SAL
DEPTNO

#**Department**
```
DEPTNO (PK)
DNAME
LOC

### 2. Student Table Normalization
**Original Table**
```
ROLLNO, NAME, AGE, EXAM, GRADE
```

#### Analysis
- Table is in **1NF**
- Not in **2NF** because of partial dependency
- Further normalized into **3NF**

#### Converted Tables

**Student**
```
ROLLNO (PK)
NAME
AGE
```

**Student_Exam**
```
ROLLNO
EXAM
GRADE
```

**Grade**
```
GRADE
MARKS
```

---

### 3. Employee Project Table
**Original Table**
```
EMPNO, PROJECT_NO, NO_OF_DAYS, CUSTOMERNAME
```

Composite Primary Key:
```
(EMPNO, PROJECT_NO)
```

#### Analysis
- Table is in **1NF**
- Not in **2NF** because:
  - `PROJECT_NO → CUSTOMERNAME`

#### Converted Tables

**Employee_Project**
```
EMPNO
PROJECT_NO
NO_OF_DAYS
```

**Project**
```
PROJECT_NO
CUSTOMERNAME
```

---

## ✅ Advantages of Normalization
- Eliminates data redundancy
- Prevents insertion anomalies
- Prevents update anomalies
- Prevents deletion anomalies
- Improves data consistency
- Simplifies database maintenance

## 🛠 Technologies Used
- Database Management System (DBMS)
- SQL Concepts
- Database Normalization

## 🎯 Learning Outcomes
After completing this assignment, I learned:
- How to identify normalization levels.
- How to detect partial and transitive dependencies.
- How to decompose tables into higher normal forms.
- Best practices for designing efficient relational databases.

## 📚 References
- Database Management System by Korth
- Oracle SQL Documentation
- DBMS Course Material

---
**Author:** Vyshnavi Upputholla
