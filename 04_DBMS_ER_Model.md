# 4. Entity-Relationship (ER) Model

---

## What is an ER Model?

- **Entity-Relationship (ER) Model** is a high-level, conceptual data model used in database design.
- It visually describes data as entities, attributes, and relationships.
- ER diagrams are used to design and map the structure of a database before implementation.

---

## Key Components

| Term         | Description                                         |
|--------------|-----------------------------------------------------|
| Entity       | Real-world object or concept (e.g., Student, Book)  |
| Attribute    | Property of an entity (e.g., Name, Age)             |
| Entity Set   | Collection of similar entities (e.g., all Students) |
| Relationship | Association between entities (e.g., Enrolls)        |
| Relationship Set | Collection of similar relationships             |

---

## Types of Attributes

- **Simple Attribute:** Cannot be divided (e.g., Age)
- **Composite Attribute:** Can be divided (e.g., Address → Street, City)
- **Single-valued Attribute:** Only one value (e.g., EmployeeID)
- **Multi-valued Attribute:** Multiple values (e.g., Phone Numbers)
- **Derived Attribute:** Calculated from other attributes (e.g., Age from DOB)

---

## Types of Relationships

- **One-to-One (1:1):** Each entity in set A relates to one in set B.
- **One-to-Many (1:N):** One entity in set A relates to many in set B.
- **Many-to-One (N:1):** Many in set A relate to one in set B.
- **Many-to-Many (M:N):** Many in set A relate to many in set B.

---

## Keys in ER Model

- **Super Key:** Set of attributes uniquely identifying an entity.
- **Candidate Key:** Minimal super key (no redundant attributes).
- **Primary Key:** Chosen candidate key to uniquely identify entities.
- **Composite Key:** Key with more than one attribute.

---

## Example: ER Diagram Structure

**Entities:** Student, Course  
**Attributes:** Student (RollNo, Name), Course (CourseID, Title)  
**Relationship:** Enrolls (between Student and Course)

**ASCII Diagram:**
```
[Student]---(Enrolls)---[Course]
   |                        |
 RollNo, Name         CourseID, Title
```

---

## Cardinality and Participation

- **Cardinality:** Number of entities to which another entity can be associated (1:1, 1:N, M:N)
- **Participation:** Total (every entity involved) or Partial

---

## Interview Tips

- Be able to draw and explain a simple ER diagram.
- Understand attribute types and relationship cardinality.
- Know the difference between keys.

---

## Possible Follow-Up Questions

- What is the difference between a candidate key and a primary key?
- Explain composite and multi-valued attributes with examples.
- How do you map an ER diagram to a relational schema?
