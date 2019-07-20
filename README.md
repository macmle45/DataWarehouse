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
## PROJECT 3

### Used Datasets:

*
*
*

### SQL statements

* create database for DimStore

```sql
USE [master]
GO

IF DB_ID('StoreDB') IS NOT NULL DROP DATABASE StoreDB
GO

CREATE DATABASE [StoreDB]
GO
```

* create table [DimStoreReload]

```sql
```

* create table [DimStoreSCD2]

```sql
```