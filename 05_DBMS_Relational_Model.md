# 5. Relational Model (Schema, Tuples, Attributes, Keys, Integrity)

---

## What is the Relational Model?

- The **Relational Model** represents data as tables (relations) consisting of rows and columns.
- Proposed by E.F. Codd in 1970; forms the foundation of most modern databases (RDBMS).

---

## Basic Terminology

| Term           | Description                                               |
|----------------|-----------------------------------------------------------|
| Relation       | Table with rows and columns                               |
| Tuple          | Row in a table (record)                                   |
| Attribute      | Column in a table (field/property)                        |
| Domain         | Set of valid values for an attribute                      |
| Degree         | Number of attributes (columns) in a relation              |
| Cardinality    | Number of tuples (rows) in a relation                     |
| Schema         | Structure/definition of the database (tables, keys, etc.) |
| Instance       | The actual contents/data of the database at a point in time|

---

## Example Table

| StudentID | Name   | Age |
|-----------|--------|-----|
| 1         | Alice  | 20  |
| 2         | Bob    | 21  |

- **Relation:** Student
- **Tuples:** (1, Alice, 20), (2, Bob, 21)
- **Attributes:** StudentID, Name, Age

---

## Types of Keys

- **Super Key:** Any combination of attributes that uniquely identifies a row.
- **Candidate Key:** Minimal super key (no unnecessary attributes).
- **Primary Key:** Chosen candidate key for unique identification.
- **Alternate Key:** Candidate keys not chosen as primary.
- **Foreign Key:** Attribute in one table that refers to the primary key of another table.
- **Composite Key:** Key with more than one attribute.

---

## Integrity Constraints

- **Entity Integrity:** Primary key cannot be NULL.
- **Referential Integrity:** Foreign key must refer to existing row in another table or be NULL.
- **Domain Integrity:** Attributes must have valid values as per their domain.
- **Unique Constraint:** Values in a column(s) must be unique.

---

## Relational Schema Example

```
Student(StudentID [PK], Name, Age)
Enrollment(EnrollID [PK], StudentID [FK], CourseID [FK])
Course(CourseID [PK], Title)
```

- [PK] = Primary Key
- [FK] = Foreign Key

---

## Interview Tips

- Be able to define tuple, relation, attribute with examples.
- Explain different types of keys and constraints.
- Understand difference between schema & instance.

---

## Possible Follow-Up Questions

- What is the difference between a primary key and a unique key?
- Why is referential integrity important?
- What happens if a table has no candidate key?
- Explain composite and foreign keys with an example.
