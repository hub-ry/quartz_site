---
tags:
  - SQL
---

Constraints can be specified when the table is created with the `CREATE TABLE` statement, or after the table is created with the `ALTER TABLE` statement.

```
CREATE TABLE _table_name_ (  
    column1 datatype constraint,  
    column2 datatype constraint,  
    column3 datatype constraint,  
    ....  
);
```


SQL constraints are used to specify rules for the data in a table.

Constraints are used to limit the type of data that can go into a table. This ensures the accuracy and reliability of the data in the table. If there is any violation between the constraint and the data action, the action is aborted.

- `[NOT NULL](https://www.w3schools.com/sql/sql_notnull.asp)` - Ensures that a column cannot have a NULL value
- `[UNIQUE](https://www.w3schools.com/sql/sql_unique.asp)` - Ensures that all values in a column are different
- `[PRIMARY KEY](https://www.w3schools.com/sql/sql_primarykey.asp)` - A combination of a `NOT NULL` and `UNIQUE`. Uniquely identifies each row in a table
- `[FOREIGN KEY](https://www.w3schools.com/sql/sql_foreignkey.asp)` - Prevents actions that would destroy links between tables
- `[CHECK](https://www.w3schools.com/sql/sql_check.asp)` - Ensures that the values in a column satisfies a specific condition
- `[DEFAULT](https://www.w3schools.com/sql/sql_default.asp)` - Sets a default value for a column if no value is specified
- `[CREATE INDEX](https://www.w3schools.com/sql/sql_create_index.asp)` - Used to create and retrieve data from the database very quickly


**NOT NULL CONSTRAINT**

The `NOT NULL` constraint enforces a column to NOT accept NULL values.

```
The following SQL ensures that the "ID", "LastName", and "FirstName" columns will NOT accept NULL values when the "Persons" table is created:

CREATE TABLE Persons (  
    ID int NOT NULL,  
    LastName varchar(255) NOT NULL,  
    FirstName varchar(255) NOT NULL,  
    Age int  
);

```















[[DataBase]] and https://www.w3schools.com/sql/sql_quickref.asp