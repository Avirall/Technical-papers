# Aggregations and Filters in SQL Queries

SQL queries often require more than just retrieving data from tables. Aggregations and filters play a critical role in summarizing and refining the data, enabling complex analysis and reporting.

## Aggregations

Aggregations are operations that perform calculations on sets of values to return a single result. Common aggregation functions include:

### 1. `COUNT()`
- Counts the number of rows that meet the specified condition.

### 2. `SUM()`
- Calculates the sum of numeric values in a column.

### 3. `AVG()`
- Computes the average of numeric values in a column.

### 4. `MIN()`
- Finds the minimum value in a column.

### 5. `MAX()`
- Retrieves the maximum value in a column.

### 6. `GROUP BY`
- Groups rows based on the values in one or more columns.
- Used with aggregation functions to perform calculations within each group.

### 7. `HAVING`
- Filters grouped results based on specified conditions.

## Filters

Filters are used to limit the result set by specifying conditions that rows must meet to be included in the query results. Common filtering techniques include:

### 1. `WHERE`
- Filters rows based on one or more conditions.
- Used with the `SELECT` statement to retrieve specific rows that meet the criteria.

### 2. `AND` and `OR`
- Combines multiple conditions to create complex filtering logic.

### 3. `BETWEEN`
- Filters rows where a column value falls within a specified range.

### 4. `LIKE`
- Searches for a specified pattern in a column.
- Wildcard characters (e.g., `%` and `_`) are used for pattern matching.

### 5. `IN`
- Filters rows where a column value matches any value in a specified list.

### 6. `IS NULL` and `IS NOT NULL`
- Filters rows where a column value is (or is not) NULL.

## Example

```sql
SELECT department, COUNT(employee_id) AS employee_count
FROM employees
WHERE name LIKE 'John'
GROUP BY department
HAVING employee_count > 5;
```
