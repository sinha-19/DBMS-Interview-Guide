# 2. DBMS Architecture (1-tier, 2-tier, 3-tier)

---

## What is DBMS Architecture?

- **DBMS Architecture** describes how users interact with the database, and how data flows between users and the storage system.
- It defines the structure and components of a DBMS.

---

## 1-Tier Architecture

- Database is directly accessible to the user.
- All processing happens on a single machine.
- Rarely used in modern applications (example: MS Access).
- **Pros:** Simplicity  
- **Cons:** Poor security, not scalable.

**Diagram:**
```
[User] <----> [DBMS] <----> [Database]
```

---

## 2-Tier Architecture (Client-Server)

- Application (client) interacts with DBMS (server) directly.
- Used in small client-server applications.

**Diagram:**
```
[Client Application] <----Network----> [DBMS Server] <----> [Database]
```

- **Examples:** ODBC/JDBC connections, desktop apps with remote DB.

**Pros:** Faster than 1-tier, some security  
**Cons:** Business logic often mixed with client, less scalable

---

## 3-Tier Architecture

- Adds a middle layer (application server) between client and DBMS.
- Layers:
  - **Presentation Layer:** User interface (client)
  - **Application Layer:** Business logic (server)
  - **Data Layer:** DBMS and database

**Diagram:**
```
[Client] <--> [Application Server] <--> [DBMS Server] <--> [Database]
```

- **Examples:** Web applications (browser <-> web server <-> DB server)

**Pros:**  
- Improved security (DBMS not directly exposed)
- Scalability
- Easier maintenance (separate logic layers)

**Cons:**  
- More complex setup

---

## Levels of Data Abstraction

1. **Physical Level:** How data is stored (files, indexes)
2. **Logical Level:** What data is stored, relationships (schemas)
3. **View Level:** User interaction/views (subsets of database)

---

## Interview Tips

- Be able to diagram and explain each architecture.
- Know the pros/cons and where each is used.
- Understand how architecture affects security and scalability.

---

## Possible Follow-Up Questions

- What are the advantages of 3-tier architecture?
- Why is 1-tier not used for enterprise applications?
- What is the role of middleware in DBMS?
- Explain levels of data abstraction.
