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

* Obszar.csv
* Pracownik.csv
* Sklep.csv

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
USE [StoreDB]
GO

DROP TABLE IF EXISTS [dbo].[DimStoreReload];

CREATE TABLE [DimStoreReload] (
    [StoreKey] int IDENTITY(1,1) NOT NULL PRIMARY KEY,
    [FirstName] varchar(50),
    [LastName] varchar(50),
    [Title] varchar(50),
    [ContinentName] varchar(50),
    [CityName] varchar(50),
    [StateProvinceName] varchar(50),
    [RegionCountryName] varchar(50),
    [StoreBusinessId] int,
    [StoreName] varchar(50),
    [StoreDescription] varchar(50),
    [Status] varchar(50),
	[LoadDate]  datetime NULL DEFAULT (GETDATE()),
	[LoadUser] varchar (100) NULL DEFAULT (SUSER_SNAME())
)
```

* create table [DimStoreSCD2]

```sql
USE [StoreDB]
GO

DROP TABLE IF EXISTS [dbo].[DimStoreSCD2];

CREATE TABLE [dbo].[DimStoreSCD2] (
	[StoreKey] int IDENTITY(1,1) NOT NULL PRIMARY KEY,
    [FirstName] varchar(50),
    [LastName] varchar(50),
    [Title] varchar(50),
    [ContinentName] varchar(50),
    [CityName] varchar(50),
    [StateProvinceName] varchar(50),
    [RegionCountryName] varchar(50),
    [StoreBusinessId] int,
    [StoreName] varchar(50),
    [StoreDescription] varchar(50),
    [Status] varchar(50),
	[DateFrom] datetime NULL,
	[DateTo] datetime NULL	DEFAULT (NULL),
	[Tech_LoadDate] datetime NULL DEFAULT (GETDATE()),
	[Tech_LoadUser] varchar(100) NULL DEFAULT (SUSER_SNAME())
)
```