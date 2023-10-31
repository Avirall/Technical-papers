# ACID in SQL

ACID is an acronym that stands for Atomicity, Consistency, Isolation, and Durability. It is a set of properties that guarantee reliable processing of database transactions. ACID is a fundamental concept in database management systems (DBMS) to ensure data integrity and reliability.

## Key Concepts

### 1. Atomicity
- Atomicity ensures that a transaction is treated as a single, indivisible unit of work.
- A transaction is either executed in its entirety or not at all. If any part of the transaction fails, the entire transaction is rolled back to its previous state.

### 2. Consistency
- Consistency guarantees that a transaction brings the database from one consistent state to another.
- It enforces business rules and integrity constraints, preventing the database from being left in an inconsistent state.

### 3. Isolation
- Isolation ensures that concurrent transactions do not interfere with each other.
- Transactions are executed as if they were the only transactions in the system, preventing conflicts and maintaining data integrity.

### 4. Durability
- Durability guarantees that once a transaction is committed, its effects are permanent and will survive any system failures.
- The changes made by a committed transaction are stored in non-volatile memory and are not lost even in the event of a crash or power failure.

## Advantages of ACID

1. **Data Integrity**: ACID properties ensure that the data remains accurate and consistent, even in the presence of failures.

2. **Reliability**: Transactions can be trusted to maintain the integrity of the data, making systems reliable.

3. **Concurrency Control**: ACID supports concurrent access to the database without compromising data integrity.

4. **Recovery**: In the event of a system failure, ACID properties guarantee that data remains in a recoverable state.

## Examples in SQL

```sql
-- Atomicity (BEGIN, COMMIT, and ROLLBACK)
BEGIN TRANSACTION;
UPDATE accounts SET balance = balance - 100 WHERE account_id = 123;
INSERT INTO transactions (account_id, amount) VALUES (123, -100);
COMMIT;

-- Consistency (CHECK Constraint)
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    order_date DATE,
    total_amount DECIMAL,
    CHECK (total_amount >= 0)
);

-- Isolation (SELECT...FOR UPDATE)
-- Ensures that a selected row is locked and not modified by other transactions until this transaction is complete.
BEGIN TRANSACTION;
SELECT * FROM products WHERE product_id = 456 FOR UPDATE;
-- Perform updates and other operations
COMMIT;

-- Durability (Write-Ahead Logging)
-- Transactions are recorded in a transaction log, which is written to non-volatile storage before changes to the database are made.
