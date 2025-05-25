# 12. Distributed Databases & NoSQL (CAP Theorem, Types, Examples)

---

## Distributed Databases

- **Definition:** A database in which data is stored across multiple physical locations (machines or sites).
- **Goal:** Improve availability, reliability, scalability, and performance.

### Key Concepts

- **Data Fragmentation:** Dividing data into smaller pieces (fragments) and storing them at different sites.
- **Replication:** Copying data to multiple sites for fault tolerance and availability.
- **Transparency:** Distribution is hidden from users; system appears as a single database.

---

## CAP Theorem

- **C**onsistency: Every node has the same data view at the same time.
- **A**vailability: Every request gets a (non-error) response, without guarantee that it contains the most recent data.
- **P**artition Tolerance: Database continues to operate even if network partitions occur.

**Theorem:** In a distributed system, you can only guarantee two of the three at any time.

| Combination        | Systems Focused On                        |
|--------------------|-------------------------------------------|
| CA (No Partition)  | Single-site databases (rare in practice)  |
| CP (No Availability)| HBase, MongoDB (in some configs)          |
| AP (No Consistency)| Couchbase, DynamoDB, Cassandra             |

---

## NoSQL Databases

- **NoSQL** stands for "Not Only SQL" — databases designed for flexible, scalable, and high-performance data storage beyond traditional relational models.

### Types of NoSQL Databases

| Type           | Description                                      | Examples                |
|----------------|--------------------------------------------------|-------------------------|
| Key-Value      | Simple pairs of keys and values                  | Redis, DynamoDB, Riak   |
| Document       | Store data as documents (usually JSON/BSON/XML)  | MongoDB, CouchDB        |
| Column-Family   | Store data in columns, not rows                  | Cassandra, HBase        |
| Graph          | Nodes and edges for highly connected data        | Neo4j, ArangoDB         |

---

## Relational vs NoSQL

| Relational DB (SQL)      | NoSQL DB                   |
|--------------------------|----------------------------|
| Fixed schemas            | Dynamic/flexible schemas   |
| ACID transactions        | BASE (Basically Available, Soft state, Eventual consistency) |
| Scales vertically        | Scales horizontally        |
| Better for complex queries| Better for large, unstructured, distributed datasets |

---

## Interview Tips

- Understand the CAP theorem and be able to give real-world examples.
- Know at least two types of NoSQL databases and their use-cases.
- Be able to explain the main differences between SQL and NoSQL.

---

## Possible Follow-Up Questions

- What is eventual consistency?
- Give an example use-case for a graph database.
- How does sharding work in distributed databases?
- When would you choose NoSQL over SQL?
