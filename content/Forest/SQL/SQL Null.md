---
tags:
  - SQL
---

A field with a NULL value is a field with no value.

If a field in a table is optional, it is possible to insert a new record or update a record without adding a value to this field. 

`IS NULL`

`IS NOT NULL`


```
IS NULL SYNTAX

SELECT column_names  
FROM table_name  
WHERE column_name IS NULL;

EXAMPLE

SELECT CustomerName, ContactName, Address  
FROM Customers  
WHERE Address IS NULL;
```

```
IS NOT NULL SYNTAX

SELECT column_names  
FROM table_name 
WHERE column_name IS NOT NULL;


SELECT CustomerName, ContactName, Address  
FROM Customers  
WHERE Address IS NOT NULL;
```








[[SQL Intro]] and https://www.w3schools.com/sql/sql_quickref.asp