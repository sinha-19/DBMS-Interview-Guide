# 7. SQL Joins, Subqueries, and Views

---

## SQL Joins

**Joins** combine rows from two or more tables based on related columns.

### Types of Joins

| Join Type      | Description                                                              |
|----------------|--------------------------------------------------------------------------|
| INNER JOIN     | Returns rows with matching values in both tables.                        |
| LEFT JOIN      | Returns all rows from left table + matched rows from right; null if none.|
| RIGHT JOIN     | Returns all rows from right table + matched rows from left; null if none.|
| FULL OUTER JOIN| Returns rows when there is a match in one of the tables.                 |
| CROSS JOIN     | Returns Cartesian product (all combinations of rows).                    |
| SELF JOIN      | Join a table to itself.                                                  |

**Example (INNER JOIN):**
```sql
SELECT Student.Name, Course.Title
FROM Student
INNER JOIN Enrollment ON Student.StudentID = Enrollment.StudentID
INNER JOIN Course ON Enrollment.CourseID = Course.CourseID;
```

---

## SQL Subqueries

A **subquery** is a query nested within another query.

**Types:**
- **Scalar Subquery:** Returns a single value.
- **Row Subquery:** Returns a single row.
- **Table Subquery:** Returns a table (used with IN, EXISTS, etc.).

**Example:**
```sql
SELECT Name
FROM Student
WHERE StudentID IN (SELECT StudentID FROM Enrollment WHERE CourseID = 101);
```

---

## SQL Views

A **view** is a virtual table based on the result of a SQL query.

**Why use views?**
- Simplifies complex queries
- Provides data security (restrict columns/rows)
- Represents derived or aggregated data

**Example:**
```sql
CREATE VIEW StudentCourses AS
SELECT Student.Name, Course.Title
FROM Student
JOIN Enrollment ON Student.StudentID = Enrollment.StudentID
JOIN Course ON Enrollment.CourseID = Course.CourseID;
```
To use:
```sql
SELECT * FROM StudentCourses;
```

---

## Interview Tips

- Know JOIN syntax and when to use each type.
- Practice writing subqueries for filtering and aggregation.
- Understand the difference between a view and a table.

---

## Possible Follow-Up Questions

- What is the difference between INNER JOIN and LEFT JOIN?
- Can you update data through a view?
- When would you use a subquery vs. a JOIN?
- What are the limitations of SQL views?
