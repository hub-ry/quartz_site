---
tags:
  - SQL
---

`SELECT * FROM Products
ORDER BY Price;`


SYNTAX: (ascending/descending example)

SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC ~ Ascending/Descending

Order Alphabetically:
`SELECT * FROM Products  `
`ORDER BY ProductName`

`SELECT * FROM Products  `
`ORDER BY ProductName DESC;`


Order by Several Columns

`SELECT * FROM Customers  `
`ORDER BY Country, CustomerName;`


Using both ASC and DESC

`SELECT * FROM Customers  `
`ORDER BY Country ASC, CustomerName DESC;`







[[SQL Intro]] and https://www.w3schools.com/sql/sql_quickref.asp