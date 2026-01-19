---
tags:
  - SQL
---

note: select **is** the same as SELECT

Example:

Return data from the customers table:

`SELECT CustomerName, City FROM Customer`

Syntax: 

`SELECT column1, column2, ... FROM table_name`




**DISTINCT**

This selected all the different entires. 
`SELECT DISTINCT Country FROM Customers`

can be paired with COUNT

`SELECT COUNT(DISTINCT Country) 
FROM Customers;`



**WHERE**

`SELECT * FROM Customers
WHERE Country='Mexico'`

[[WHERE]] ~ can be used with more than SELECT, you just happen to get the introduction. 

`SELECT * FROM Customers  
`WHERE CustomerID > 80;

|   |   |   |
|---|---|---|
|=|Equal||
|>|Greater than||
|<|Less than||
|>=|Greater than or equal||
|<=|Less than or equal||
|<>|Not equal. **Note:** In some versions of SQL this operator may be written as !=||
|BETWEEN|Between a certain range||
|LIKE|Search for a pattern||
|IN|To specify multiple possible values for a column|

[[ORDER BY]] (SORT)








[[SQL Intro]] and https://www.w3schools.com/sql/sql_quickref.asp