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
CREATE TABLE [DimStoreReload] (
    [FirstName] varchar(50),
    [LastName] varchar(50),
    [Title] varchar(50),
    [ContinentName] varchar(50),
    [CityName] varchar(50),
    [StateProvinceName] varchar(50),
    [RegionCountryName] varchar(50),
    [StoreBusinessId] tinyint,
    [StoreName] varchar(50),
    [StoreDescription] varchar(50),
    [Status] varchar(50)
)
```

* create table [DimStoreSCD2]

```sql
```