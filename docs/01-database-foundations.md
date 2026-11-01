# Database foundations

Relational databases organize structured information into tables containing rows and columns. Primary keys identify rows; foreign keys can reference rows in related tables. A schema describes database objects and their organization.

## Application-to-database flow

```text
Browser/client -> HTTP request -> Web application -> SQL driver -> DBMS
Browser/client <- HTTP response <- Web application <- query result <- DBMS
```

Unsafe applications may concatenate untrusted request values into SQL strings. If values are not safely bound as data, input may affect SQL syntax or logic.

## SQL fluency exercises

```sql
SHOW DATABASES;
USE employees;
SHOW TABLES;
DESCRIBE employees;

SELECT * FROM employees.employees
WHERE first_name LIKE 'Bar%' AND hire_date = '1990-01-01';

SELECT COUNT(*) FROM employees.titles
WHERE emp_no > 10000 OR title NOT LIKE '%engineer%';
```

`AND` requires both conditions to be true; `OR` requires at least one; `LIKE` performs pattern matching; `COUNT(*)` counts matching rows. Understanding the intended query and expected result makes application behavior easier to interpret.
