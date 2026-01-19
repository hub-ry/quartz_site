---
tags:
  - SQL
---


The `WHERE` clause can contain one or many `AND` operators.

```
SELECT *  
FROM Customers  
WHERE Country = 'Spain' AND CustomerName LIKE 'G%';
```

You'd Never Guess what the OR operator does, it's NOT exclusive btw.

Select all Spanish customers that starts with either "G" or "R":
```
SELECT * FROM Customers  
WHERE Country = 'Spain' AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');
```




NOT 

```
Example: 

SELECT * FROM Customers  
WHERE NOT Country = 'Spain';

Syntax:

SELECT column1, column2, ...
FROM table_name 
WHERE NOT condition;

```

NOT LIKE

```
SELECT * FROM Customers  
WHERE CustomerName NOT LIKE 'A%';

Selects customers that does not start with the letter 'A'
```

NOT BETWEEN

```
SELECT * FROM Customers  
WHERE CustomerID NOT BETWEEN 10 AND 60;
```

NOT IN
```
SELECT * FROM Customers  
WHERE City NOT IN ('Paris', 'London');
```

NOT Greater Than
```
SELECT * FROM Customers  
WHERE NOT CustomerID > 50;
```

NOT Less Than
```
SELECT * FROM Customers  
WHERE NOT CustomerId < 50;
```









[[SQL Intro]] and https://www.w3schools.com/sql/sql_quickref.asp