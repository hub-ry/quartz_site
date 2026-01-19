---
tags:
  - SQL
---

The `ALTER TABLE` statement is used to add, delete, or modify columns in an existing table.

The `ALTER TABLE` statement is also used to add and drop various constraints on an existing table.

```
SYNTAX

ALTER TABLE table_name  
ADD column_name datatype;

EXAMPLE

ALTER TABLE Customers  
ADD Email varchar(255);

  
ALTER TABLE Employees ADD Email varchar(255);
```

To delete a column in a table, use the following syntax (notice that some database systems don't allow deleting a column):

```
ALTER TABLE Customers  
DROP COLUMN Email;
```








[[DataBase]] and https://www.w3schools.com/sql/sql_quickref.asp