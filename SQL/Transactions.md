# Transactions in Database Management

Transactions are a fundamental concept in database management that ensure the integrity and consistency of data in a database. They represent a sequence of one or more database operations as a single, indivisible unit of work.

## Key Concepts

### 1. Atomicity
- Atomicity ensures that a transaction is treated as a single, indivisible unit.
- All the operations within a transaction must be completed successfully, or none of them are applied.

### 2. Consistency
- Consistency guarantees that a transaction takes the database from one consistent state to another.
- All data integrity rules, constraints, and triggers are satisfied before and after the transaction.

### 3. Isolation
- Isolation ensures that the operations of one transaction are isolated from the operations of other transactions.
- Concurrent transactions do not interfere with each other.

### 4. Durability
- Durability guarantees that once a transaction is committed, its effects are permanent.
- Even in the event of a system failure, the changes made by a committed transaction are not lost.

## ACID Properties

Transactions are often associated with the ACID properties:

- **Atomicity**: A transaction is an atomic unit of work.
- **Consistency**: A transaction brings the database from one consistent state to another.
- **Isolation**: Concurrent transactions are isolated from each other.
- **Durability**: Committed transactions are permanent and survive system failures.

## Practical Examples

### Bank Transactions
```sql
BEGIN TRANSACTION;

-- Deduct money from one account
UPDATE accounts SET balance = balance - 100 WHERE account_id = 123;

-- Add money to another account
UPDATE accounts SET balance = balance + 100 WHERE account_id = 456;

COMMIT;
```
