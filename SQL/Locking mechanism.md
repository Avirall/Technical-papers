# Locking Mechanisms in Database Management

Locking mechanisms are a fundamental concept in database management that control and coordinate access to shared resources, such as database records, to ensure data integrity in multi-user database environments. Locks prevent concurrent transactions from causing data inconsistencies and conflicts.

## Key Concepts

### 1. Lock Types
- Locks can be of different types, including shared locks and exclusive locks.
- A shared lock allows multiple transactions to read the locked resource simultaneously but prevents any transaction from writing to it.
- An exclusive lock allows one transaction to modify the locked resource while preventing any other transaction from reading or writing to it.

### 2. Lock Granularity
- Locks can be applied at different levels of granularity, such as table-level locks, row-level locks, or even page-level locks.
- Row-level locks are the most fine-grained and flexible, allowing concurrent access to different rows in the same table.

### 3. Deadlocks
- Deadlocks occur when two or more transactions are waiting for each other to release locks, causing a standstill.
- Database management systems often use algorithms to detect and resolve deadlocks.

### 4. Lock Management
- Locks are managed by the database management system (DBMS) and can be automatically acquired and released.
- Developers and administrators may specify lock hints to control the locking behavior.

## Common Locking Scenarios

### 1. Read-Write Locks
- Multiple transactions can read the same data concurrently.
- Only one transaction can write to the data, preventing concurrent writes.

### 2. Exclusive Locks
- A transaction obtains an exclusive lock when it intends to modify data, ensuring that other transactions cannot read or write the locked data.

### 3. Lock Timeouts
- To avoid indefinite blocking, transactions can set lock timeouts, specifying how long they are willing to wait for a lock to be released.

## Practical Examples

```sql
-- Example of applying an exclusive lock for an update
BEGIN TRANSACTION;

-- Acquire an exclusive lock
UPDATE products SET quantity = quantity - 1 WHERE product_id = 789;

COMMIT;

-- Example of a shared lock for reading
BEGIN TRANSACTION;

-- Acquire a shared lock
SELECT product_name, quantity FROM products WHERE category = 'Electronics';

COMMIT;
```
