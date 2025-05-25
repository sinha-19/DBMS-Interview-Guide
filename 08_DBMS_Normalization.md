# 8. Normalization & Normal Forms (1NF–BCNF, 3NF, etc.)

---

## What is Normalization?

- **Normalization** is the process of organizing data in a database to reduce redundancy and improve data integrity.
- Achieved by dividing large tables into smaller ones and defining relationships.

---

## Objectives of Normalization

- Eliminate redundant data
- Ensure data dependencies make sense
- Simplify data structures

---

## Normal Forms

### 1. First Normal Form (1NF)

- Each cell contains only a single (atomic) value.
- All entries in a column are of the same data type.
- No repeating groups or arrays.

**Example (Not in 1NF):**
| Student | Courses        |
|---------|---------------|
| Alice   | Math, Science |

**Converted to 1NF:**
| Student | Course   |
|---------|----------|
| Alice   | Math     |
| Alice   | Science  |

---

### 2. Second Normal Form (2NF)

- Must be in 1NF.
- No partial dependency (no non-prime attribute is dependent on part of a candidate key).
- Applies mainly to tables with composite primary keys.

---

### 3. Third Normal Form (3NF)

- Must be in 2NF.
- No transitive dependency (non-prime attribute depends only on candidate key, not on another non-prime attribute).

---

### 4. Boyce-Codd Normal Form (BCNF)

- Stricter version of 3NF.
- For every functional dependency X → Y, X should be a super key.

---

### Higher Normal Forms

- **4NF:** Removes multi-valued dependencies.
- **5NF:** Removes join dependencies.

---

## Example Table (Normalization Steps)

**Unnormalized (UNF):**
| OrderID | Customer | Items           |
|---------|----------|----------------|
| 1       | John     | Pen, Pencil    |

**1NF:**
| OrderID | Customer | Item   |
|---------|----------|--------|
| 1       | John     | Pen    |
| 1       | John     | Pencil |

**2NF:**
Suppose composite key (OrderID, Item), no partial dependency.

**3NF:**
If Customer info is separated (no transitive dependency):

| CustomerID | CustomerName |
|------------|-------------|
| 101        | John        |

| OrderID | CustomerID | Item   |
|---------|------------|--------|
| 1       | 101        | Pen    |

---

## Interview Tips

- Be able to define and identify each normal form.
- Practice converting tables between normal forms.
- Understand functional, partial, and transitive dependencies.

---

## Possible Follow-Up Questions

- What is the difference between 3NF and BCNF?
- Why is normalization important?
- What is a functional dependency?
- Can you give an example of denormalization?
