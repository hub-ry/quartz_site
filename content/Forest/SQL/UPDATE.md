
Modify existing records in a table.

```
SYNTAX

UPDATE table_name
SET column1 = value1, column2 = value2, ...   
WHERE condition;

EXAMPLE


UPDATE Customers  
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'  
WHERE CustomerID = 1;
```


UPDATE MULTIPLE RECORDS

```
UPDATE Customers  
SET ContactName='Juan'  
WHERE Country='Mexico';
```



Be careful when updating records. If you omit the `WHERE` clause, ALL records will be updated!




[[SQL Intro]] and https://www.w3schools.com/sql/sql_quickref.asp