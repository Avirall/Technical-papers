# Joins in SQL

In SQL, a "join" is a fundamental operation used to combine data from two or more tables based on a related column between them. Joins are essential for querying and retrieving information from a relational database by creating connections between tables.

## Key Concepts

### 1. Inner Join
- An inner join returns only the rows for which there is a match in both tables.
- It combines rows from two tables where the specified condition is met.

### 2. Left (Outer) Join
- A left join returns all the rows from the left table and the matching rows from the right table.
- For rows in the left table with no matching rows in the right table, the result will contain NULL values.

### 3. Right (Outer) Join
- A right join returns all the rows from the right table and the matching rows from the left table.
- For rows in the right table with no matching rows in the left table, the result will contain NULL values.

### 4. Full (Outer) Join
- A full join returns all rows from both tables, including both matching and non-matching rows.
- If there is no match for a row, the result will contain NULL values in columns from the non-matching table.

### 5. Cross Join (Cartesian Product)
- A cross join returns the Cartesian product of two tables, generating all possible combinations of rows.
- It does not require a specific join condition.

### Syntax for Inner Join
```sql
SELECT customers.name, orders.order_id
FROM customers
INNER JOIN orders ON customers.customer_id = orders.customer_id;
