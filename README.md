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
USE [master]
GO

IF DB_ID('BusinessDataDB') IS NOT NULL DROP DATABASE BusinessDataDB
GO

CREATE DATABASE [BusinessDataDB]
GO
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
## PROJECT 2

### Used Datasets:

* WizyWydane.csv

### SQL statements

* create database 

```sql
USE [master]
GO

IF DB_ID('VisaDB') IS NOT NULL DROP DATABASE VisaDB
GO

CREATE DATABASE [VisaDB]
GO
```