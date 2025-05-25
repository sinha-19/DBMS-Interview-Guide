# 6. SQL Basics (DDL, DML, DCL, TCL)

---

## What is SQL?

- **SQL (Structured Query Language)** is the standard language for interacting with relational databases.
- Used to create, modify, manage, and query data.

---

## Types of SQL Statements

### 1. DDL (Data Definition Language)

- Defines and modifies database structure (schema).
- **Commands:**
  - `CREATE` – Create database objects (tables, views, etc.)
  - `ALTER` – Modify structure of database objects
  - `DROP` – Delete database objects
  - `TRUNCATE` – Remove all records from table, keep structure

**Example:**
```sql
CREATE TABLE Student (
  StudentID INT PRIMARY KEY,
  Name VARCHAR(100),
  Age INT
);
```

---

### 2. DML (Data Manipulation Language)

- Used to manage data within schema objects.
- **Commands:**
  - `SELECT` – Retrieve data
  - `INSERT` – Add new records
  - `UPDATE` – Modify data
  - `DELETE` – Remove records

**Example:**
```sql
INSERT INTO Student (StudentID, Name, Age) VALUES (1, 'Alice', 20);
SELECT * FROM Student;
UPDATE Student SET Age = 21 WHERE StudentID = 1;
DELETE FROM Student WHERE StudentID = 1;
```

---

### 3. DCL (Data Control Language)

- Controls access to data in the database.
- **Commands:**
  - `GRANT` – Give user access privileges
  - `REVOKE` – Remove user access privileges

**Example:**
```sql
GRANT SELECT ON Student TO user1;
REVOKE SELECT ON Student FROM user1;
```

---

### 4. TCL (Transaction Control Language)

- Manages transactions in the database.
- **Commands:**
  - `COMMIT` – Save changes
  - `ROLLBACK` – Undo changes
  - `SAVEPOINT` – Set a point within a transaction to roll back to

**Example:**
```sql
BEGIN;
UPDATE Student SET Age = 22 WHERE StudentID = 1;
SAVEPOINT sp1;
DELETE FROM Student WHERE StudentID = 2;
ROLLBACK TO sp1;
COMMIT;
```

---

## Interview Tips

- Know the difference between DDL, DML, DCL, and TCL.
- Be able to write basic SQL statements for each category.
- Understand the purpose of transactions and transaction control.

---

## Possible Follow-Up Questions

- What is the difference between DELETE and TRUNCATE?
- How do you give and revoke privileges in SQL?
- What are transactions and why are they important?
- How does ROLLBACK work with SAVEPOINT?
