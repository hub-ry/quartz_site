

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