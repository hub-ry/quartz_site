---
tags:
  - SQL
---

```
CREATE DATABASE databasename;
```


SQL DROP DATABASE

The `DROP DATABASE` statement is used to drop an existing SQL database.

```
DROP DATABASE databasename;
```



SQL BACKUP DATABASE for SQL Server

The `BACKUP DATABASE` statement is used in SQL Server to create a full back up of an existing SQL database.

A differential back up only backs up the parts of the database that have changed since the last full database backup.

```
WITH DIFFERENTIAL

BACKUP DATABASE databasename  
TO DISK = 'filepath'  
WITH DIFFERENTIAL;


EXAMPLE WITHOUT DIFF

BACKUP DATABASE testDB  
TO DISK = 'D:\backups\testDB.bak';

EXAMPLE WITH

BACKUP DATABASE testDB  
TO DISK = 'D:\backups\testDB.bak'  
WITH DIFFERENTIAL;

```







[[DataBase]] and https://www.w3schools.com/sql/sql_quickref.asp