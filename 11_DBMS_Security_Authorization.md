# 11. Database Security & Authorization (Privileges, SQL Injection, etc.)

---

## Why is Database Security Important?

- Protects sensitive data from unauthorized access, modification, or destruction.
- Ensures privacy, integrity, and availability of data.

---

## Authorization & Privileges

- **Authorization:** Process of granting/restricting user access to database objects and operations.
- **Privileges:** Rights to perform actions (SELECT, INSERT, UPDATE, DELETE, etc.).

**Example (SQL):**
```sql
GRANT SELECT, INSERT ON Student TO user1;
REVOKE INSERT ON Student FROM user1;
```

- **Role-Based Access Control (RBAC):** Privileges grouped in roles, assigned to users (e.g., 'admin', 'readonly').

---

## Authentication

- Verifies the identity of users before granting access.
- Methods: Passwords, tokens, certificates, multi-factor authentication.

---

## Common Security Threats

### 1. SQL Injection

- Malicious input alters SQL queries to access or manipulate data.
- **Prevention:**
  - Use prepared statements and parameterized queries.
  - Validate and sanitize user input.

**Example (Vulnerable):**
```sql
SELECT * FROM Users WHERE username = '$input';
```

**Example (Safe):**
```sql
SELECT * FROM Users WHERE username = ?;
```

---

### 2. Privilege Escalation

- User gains higher privileges than allowed.
- **Prevention:** Principle of least privilege (give only necessary rights).

---

### 3. Data Leakage

- Sensitive data accidentally exposed.
- **Prevention:** Data encryption (at rest and in transit), auditing, masking.

---

### 4. Denial of Service (DoS)

- Overloading the DBMS to make it unavailable.
- **Prevention:** Resource limits, monitoring, throttling.

---

## Best Practices for Database Security

- Use strong authentication and password policies.
- Limit privileges to minimum required (least privilege).
- Regularly audit database activities and access logs.
- Encrypt sensitive data and connections.
- Keep DBMS and applications up to date with security patches.
- Use firewalls and network segmentation.

---

## Interview Tips

- Understand how to grant/revoke privileges in SQL.
- Know what SQL injection is and how to prevent it.
- Be able to explain RBAC and principle of least privilege.
- Mention encryption and auditing as part of best practices.

---

## Possible Follow-Up Questions

- What is the difference between authentication and authorization?
- How do you prevent SQL injection?
- What are common ways to audit database activity?
- Why is encryption important for databases?
