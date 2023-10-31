# Normalization in Database Design

Normalization is a systematic process in database design that organizes data in a relational database to minimize data redundancy and dependency. The primary goal of normalization is to ensure data integrity and improve database performance.

## Key Concepts

### 1. Data Redundancy
- Data redundancy occurs when the same piece of data is stored in multiple places within a database.
- Redundant data can lead to inconsistencies and anomalies.

### 2. Anomalies
- Anomalies are problems that arise from data redundancy, including insertion, update, and deletion anomalies.

### 3. Normal Forms
- Normal forms are a set of rules that define how data should be structured in a relational database.
- Each normal form has specific criteria that data must meet to be considered well-organized.

## Common Normal Forms

### 1. First Normal Form (1NF)
- Each table cell must contain a single, atomic (indivisible) value.
- All entries in a column must be of the same data type.

### 2. Second Normal Form (2NF)
- The table must already be in 1NF.
- It eliminates partial dependencies by ensuring that non-key attributes depend on the whole primary key.

### 3. Third Normal Form (3NF)
- The table must already be in 2NF.
- It eliminates transitive dependencies by ensuring that non-key attributes are not dependent on other non-key attributes.

### 4. Boyce-Codd Normal Form (BCNF)
- A more strict version of 3NF that ensures all determinants are superkeys.

### 5. Fourth Normal Form (4NF) and Beyond
- These address multi-valued and join dependencies and are used in more complex scenarios.
