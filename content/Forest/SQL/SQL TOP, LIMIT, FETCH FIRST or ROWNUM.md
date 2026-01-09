
EACH THING HERE IS BECAUSE DIFFERENT SQL'S USE DIFFERENT SYNTAX

The `SELECT TOP` clause is used to specify the number of records to return.

The `SELECT TOP` clause is useful on large tables with thousands of records. Returning a large number of records can impact performance.

```
Select only the first 3 records of the Customers table:

SELECT TOP 3 * FROM Customers;
```



**Note:** Not all database systems support the `SELECT TOP` clause. MySQL supports the `LIMIT` clause to select a limited number of records, while Oracle uses `FETCH FIRST _n_ ROWS ONLY` and `ROWNUM`.








[[SQL Intro]] and https://www.w3schools.com/sql/sql_quickref.asp