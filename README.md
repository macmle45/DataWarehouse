# DataWarehouse
University projects 

## PROJECT 1

### Used Datasets:

* Bank Marketing DataSet 
* Dow Jones Index DataSet 
* Wholesale customers DataSet 

### SQL statements

* create database

```sql
CREATE DATABASE [BusinessDataDB]
```

* create table for logging

```sql
USE [BusinessDataDB]
GO

CREATE TABLE [LoggingData] 
	(
	  [DateOfExectPackg] DATETIME
	 ,[ExectPackgName] VARCHAR (50)
	 ,[UserExectPackg] VARCHAR (50)
	);
```
