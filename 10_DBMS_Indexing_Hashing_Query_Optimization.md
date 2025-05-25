# 10. Indexing, Hashing, and Query Optimization

---

## Indexing

- **Index:** A data structure that improves the speed of data retrieval on a database table.
- Similar to an index in a book; lets you quickly find data without scanning every row.

### Types of Indexes

| Type                 | Description                                                         |
|----------------------|---------------------------------------------------------------------|
| Primary Index        | Built on the primary key, unique for each record                    |
| Secondary Index      | Built on non-primary key attributes, may have duplicates            |
| Clustered Index      | Sorts and stores table rows according to the index key              |
| Non-Clustered Index  | Has a separate structure from the table, with pointers to the data  |
| Unique Index         | Ensures all values in the indexed column are unique                 |
| Composite Index      | Built on two or more columns                                        |

**Example (SQL):**
```sql
CREATE INDEX idx_name ON Student(Name);
```

---

## Hashing

- **Hashing:** Technique to convert a search key into a location in the storage (using a hash function).
- Used in hash indexes for fast equality searches (e.g., finding a row by exact key).

**Types:**
- **Static Hashing:** Fixed number of buckets; may lead to overflow
- **Dynamic Hashing:** Buckets can grow/shrink (e.g., extendible hashing)

**Pros:** Very fast for exact match queries  
**Cons:** Not efficient for range queries

---

## Query Optimization

- **Query Optimization:** Process of choosing the most efficient way to execute a SQL query.
- DBMS uses the **query optimizer** to generate and compare possible execution plans.

### Techniques

- **Cost-based Optimization:** Chooses plan with lowest estimated cost (I/O, CPU)
- **Heuristic-based Optimization:** Uses rules (e.g., push selection early)
- **Use of Indexes:** Optimizer may use indexes to speed up queries

### Steps in Query Processing

1. **Parsing:** Check query syntax and semantics
2. **Translation:** Convert into internal representation
3. **Optimization:** Find most efficient execution plan
4. **Execution:** Run the query

---

## Interview Tips

- Know when and why to use indexes; explain pros/cons.
- Understand difference between clustered and non-clustered indexes.
- Be able to explain how hashing works for search.
- Discuss why query optimization is crucial for performance.

---

## Possible Follow-Up Questions

- What is the difference between clustered and non-clustered index?
- How does hashing help in searching?
- What factors does the query optimizer consider?
- Can indexes slow down performance? When?
