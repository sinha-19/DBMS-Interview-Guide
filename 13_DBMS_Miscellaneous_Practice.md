# 13. DBMS Miscellaneous Topics & Interview Practice

---

## Other Important Topics

### 1. Triggers

- **Trigger:** A special procedure that automatically executes in response to certain events on a table (e.g., INSERT, UPDATE, DELETE).
- **Use-cases:** Auditing, enforcing business rules, automatic updates.

**Example:**
```sql
CREATE TRIGGER update_timestamp
BEFORE UPDATE ON Student
FOR EACH ROW
SET NEW.updated_at = NOW();
```

---

### 2. Stored Procedures & Functions

- **Stored Procedure:** Precompiled SQL code that can be executed multiple times.
- **Function:** Similar, but returns a value and is often used in queries.

---

### 3. Cursors

- **Cursor:** Database object used to retrieve, manipulate, and navigate through a result set row by row.

---

### 4. Views vs. Materialized Views

- **View:** Virtual table, not storing data physically.
- **Materialized View:** Stores the result physically; needs refreshing.

---

### 5. Data Warehousing & OLAP

- **Data Warehouse:** Centralized repository for integrated data from multiple sources.
- **OLAP (Online Analytical Processing):** Tools for analyzing data in multiple dimensions (e.g., sales by region, time).

---

### 6. Backup & Recovery

- **Backup:** Copying data to prevent loss.
- **Recovery:** Restoring data after a failure.

---

## Sample DBMS Interview Questions

1. Explain the difference between DELETE, TRUNCATE, and DROP.
2. What is a foreign key? Give an example.
3. How do you prevent SQL injection?
4. What is normalization? Why is it important?
5. Difference between clustered and non-clustered indexes.
6. Describe ACID properties with examples.
7. What is the difference between a view and a materialized view?
8. What is the use of triggers in DBMS?
9. Explain CAP theorem.
10. Describe steps to recover a crashed database.

---

## General Interview Tips

- Practice writing SQL queries and explaining output.
- Draw ER diagrams and normalization steps by hand.
- Revise DBMS terminology—be comfortable with definitions and examples.
- Prepare real-life scenarios for normalization, transaction failures, indexing, etc.
- Be ready for both theoretical and practical questions.

---

## Further Resources

- Standard DBMS textbooks (Korth, Navathe, Silberschatz)
- Official documentation for MySQL, PostgreSQL, SQL Server, MongoDB
- Leetcode/GeeksforGeeks for SQL and DBMS interview problems

---

**Congratulations! You've completed the DBMS interview prep series.**
