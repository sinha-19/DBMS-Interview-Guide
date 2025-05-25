# 1. Introduction to DBMS

---

## What is a DBMS?

A **Database Management System (DBMS)** is software that enables users to define, create, maintain, and control access to databases.  
It provides an interface for storing, retrieving, and manipulating data.

---

## Why Use a DBMS?

- **Data redundancy control:** Avoids unnecessary duplication.
- **Data consistency & integrity:** Maintains data accuracy and validity.
- **Data security:** Restricts unauthorized access.
- **Efficient data access:** Optimizes query and update performance.
- **Backup and recovery:** Protects data from failures.
- **Concurrent access:** Supports multiple users simultaneously.

---

## Key Terms

| Term       | Description                                                      |
|------------|------------------------------------------------------------------|
| Database   | Organized collection of related data                             |
| DBMS       | Software to manage databases                                     |
| Data       | Raw facts and figures                                            |
| Information| Processed data, meaningful to users                              |
| Query      | Request to access/manipulate data in DBMS                        |
| Schema     | Structure of the database (tables, fields, relationships)        |
| Instance   | The data in the database at a particular moment                  |

---

## DBMS vs. File System

| Feature          | File System                      | DBMS                           |
|------------------|----------------------------------|--------------------------------|
| Data Redundancy  | High                             | Low                            |
| Data Access      | Procedural (manual programming)  | Declarative (SQL, queries)     |
| Integrity        | Hard to enforce                  | Enforced via constraints       |
| Security         | Weak                             | Strong (user/password, roles)  |
| Backup/Recovery  | Manual                           | Automatic tools                |
| Concurrency      | Poor                             | Good (locking, transactions)   |

---

## Types of DBMS

- **Hierarchical DBMS:** Data organized in tree-like structure (e.g., IBM IMS)
- **Network DBMS:** Data organized as a graph (e.g., IDMS)
- **Relational DBMS (RDBMS):** Data in tables (e.g., MySQL, PostgreSQL, Oracle)
- **Object-oriented DBMS:** Data as objects (e.g., db4o, ObjectDB)

---

## Popular DBMS Examples

- MySQL, PostgreSQL, Oracle, MS SQL Server, MongoDB, SQLite

---

## Interview Tips

- Be able to explain what a DBMS is and why it is used.
- Know advantages of DBMS vs. file systems.
- Be familiar with different DBMS types.

---

## Possible Follow-Up Questions

- What is the difference between data and information?
- What are the main functions of a DBMS?
- Why is data abstraction important in DBMS?
- Can you name some popular DBMS software?
