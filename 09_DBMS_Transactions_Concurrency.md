# 9. Transactions & Concurrency Control (ACID, Schedules, Deadlock)

---

## What is a Transaction?

- A **transaction** is a sequence of one or more SQL operations executed as a single unit.
- Transactions ensure reliability and consistency in databases.

---

## ACID Properties

- **A**tomicity: All steps of a transaction are completed, or none are (all-or-nothing).
- **C**onsistency: The database moves from one valid state to another.
- **I**solation: Concurrent transactions do not interfere with each other.
- **D**urability: Once committed, changes are permanent even after a failure.

---

## Transaction States

- **Active:** Transaction is in progress.
- **Partially Committed:** All operations done, but changes not yet permanent.
- **Committed:** Changes saved to the database.
- **Failed:** Transaction cannot proceed.
- **Aborted:** All changes rolled back.

---

## Concurrency Control

- **Purpose:** Manage simultaneous transactions to prevent conflicts and ensure data consistency.

### Problems in Concurrency

- **Lost Update:** Two transactions overwrite each other’s changes.
- **Dirty Read:** Transaction reads uncommitted data from another transaction.
- **Unrepeatable Read:** Same query gives different results within one transaction.
- **Phantom Read:** New rows appear/disappear in repeated queries.

---

## Schedules

- **Schedule:** Order in which operations of transactions are executed.
- **Serial Schedule:** Transactions executed one after another (no overlap).
- **Concurrent Schedule:** Operations from multiple transactions interleave.
- **Serializable Schedule:** Equivalent to some serial schedule (ensures consistency).

---

## Deadlock

- **Deadlock:** Two or more transactions wait forever for resources locked by each other.
- **Prevention:** Timeout, resource ordering, deadlock detection and victim selection.

---

## Interview Tips

- Be able to define and explain the ACID properties with examples.
- Know different concurrency issues and how they are handled.
- Understand the concept of serializability and deadlock.

---

## Possible Follow-Up Questions

- What is the difference between atomicity and durability?
- How is isolation achieved in databases?
- Give an example of a deadlock in SQL.
- What are the different types of schedules in transaction management?
