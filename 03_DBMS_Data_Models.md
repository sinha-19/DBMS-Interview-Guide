# 3. Data Models in DBMS

---

## What is a Data Model?

A **data model** is a conceptual way of structuring and organizing data, relationships, and constraints in a database system. It defines how data is stored, connected, and accessed.

---

## Main Types of Data Models

### 1. Hierarchical Data Model

- Data is organized in a tree-like structure (parent-child relationship).
- Each child has only one parent, but a parent can have multiple children.
- Example: Organizational chart, file systems.

**Diagram:**
```
        [Root]
         /   \
      [A]   [B]
      /
    [C]
```

**Pros:** Simple, fast access for hierarchical data  
**Cons:** Not flexible for complex relationships; data redundancy

---

### 2. Network Data Model

- Data organized in a graph; supports many-to-many relationships.
- Records connected via links (pointers).

**Diagram:**
```
    [A]-----[B]
     |      /
    [C]---/
```

**Pros:** More flexible than hierarchical, supports complex relationships  
**Cons:** Complex to design and maintain

---

### 3. Relational Data Model

- Most widely used.
- Data represented in tables (relations) of rows and columns.
- Relationships via keys (primary, foreign).

**Example Table:**

| StudentID | Name    | Course  |
|-----------|---------|---------|
| 1         | Alice   | Math    |
| 2         | Bob     | Science |

**Pros:** Simple, powerful queries (SQL), easy maintenance, minimal redundancy  
**Cons:** Can be slower for very large or unstructured data

---

### 4. Entity-Relationship (ER) Model

- High-level, conceptual model.
- Data represented as entities (objects) and relationships.
- Used in database design (ER diagrams).

**Example:**

- Entity: Student
- Entity: Course
- Relationship: Enrolls

---

### 5. Object-Oriented Data Model

- Data as objects (like in OOP languages).
- Objects have attributes and methods.
- Supports inheritance, encapsulation, polymorphism.

**Example:**
- Object: Car (attributes: color, speed; methods: drive(), brake())

---

## Interview Tips

- Know characteristics and use-cases for each model.
- Be able to draw and interpret simple diagrams.
- Relational model is most important for SQL-based interviews.

---

## Possible Follow-Up Questions

- What are the limitations of the hierarchical model?
- How does the relational model differ from the network model?
- What is an ER diagram and why is it used?
- Can you give real-world examples of each model?
