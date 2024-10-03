*From W3Schools*
## Managing Databases and Tables

```mysql
CREATE DATABASE record_company;
-- Create a database, inside of which are tables

DROP DATABASE record_company;
-- delete a database - all data 

BACKUP DATABASE databasename
TO DISK = 'filepath';
-- backup a database
WITH DIFFERNTIAL;
-- back up parts that have changed since last backup

-- select that database to work on
USE record_company;


CREATE TABLE Persons{
	PersonID int,  
    LastName varchar(255),  
    FirstName varchar(255),  
    Address varchar(255),  
    City varchar(255)
}
-- column1 datatype, etc.
-- data types: https://www.w3schools.com/sql/sql_datatypes.asp


CREATE TABLE testTable AS 
SELECT LastName, FirstName FROM Persons;
-- create a table from another table

DROP TABLE Persons;
-- delete table and data

TRUNCATE TABLE Persons;
-- delete data, not table

ALTER TABLE Customers  
ADD Email varchar(255);
-- or
DROP COLUMN Email;
-- or
RENAME City to CITY;
-- add, delete, modify columns in existing tables
-- can also rename column, syntax differs per system

CREATE TABLE _table_name_ (  
    _column1 datatype_ _constraint_,  
    _column2 datatype_ _constraint_,  
    _column3 datatype_ _constraint_,  
    ....  
);
/* Constraints - specify rules for data in table
NOT NULL	  	Ensures that a column cannot have NULL
UNIQUE			All values are different in column
PRIMARY KEY		Uniquely identifies each row in a table
FOREIGN KEY		prevents actions that would destroy links between tables
CHECK 			Ensures that the values in column satisfy specific condition
DEFAULT			set default val if none is specified
CREATE INDEX 	create and retreive data from DB quickly
*/
```

```mysql
PRIMARY KEY -- must contain UNIQUE values, cannot contain NULL
			-- table has only ONE primary key

CREATE TABLE Persons (  
    ID int NOT NULL,  
    LastName varchar(255) NOT NULL,  
    FirstName varchar(255),  
    Age int,  
    PRIMARY KEY (ID)  
);


FOREIGN KEY -- a field (or collection of fields) in one table, that refer to the PRIMARY KEY in another table

CREATE TABLE Orders (  
    OrderID int NOT NULL,  
    OrderNumber int NOT NULL,  
    PersonID int,  
    PRIMARY KEY (OrderID),  
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)  
);


```

```mysql


CREATE TABLE Persons (  
    Personid int NOT NULL AUTO_INCREMENT,  
/*  LastName varchar(255) NOT NULL,  
    FirstName varchar(255),  
    Age int, PRIMARY KEY (Personid) */ 
);
-- auto_increment 

ALTER TABLE Persons 
ADD Date_Birth DATE;
-- DATE data types
-- most common are DATE and YEAR


CREATE VIEW [Brazil Customers] AS  
SELECT CustomerName, ContactName  
FROM Customers  
WHERE Country = 'Brazil';
SELECT * FROM [Brazil Customers]
-- VIEW - a virtual table based on the result-set of an SQL statement
-- has rows and columns / which can be added and deleted 


CREATE OR REPLACE VIEW [Brazil Customers] AS  
SELECT CustomerName, ContactName, City  
FROM Customers  
WHERE Country = 'Brazil';
-- CREATE OR REPLACE VIEW - updating a VIEW / adds city column 

DROP VIEW [Brazil Customers]
```

## Working inside a Table

```mysql
SELECT * FROM Customers; 
-- all columns

SELECT CustomerName, City FROM Customers;
-- specific columns

SELECT DISTINCT Country FROM Customers; 
-- unique, non-repeating values 

SELECT COUNT(DISTINCT Country) FROM Customers;
-- count distinct
```

```mysql
SELECT * FROM Customers  
WHERE Country='Mexico'; -- select specific 
-- operators:  =,<, >, <=, >=, (<>) != , BETWEEN, LIKE, IN  
```

```mysql
SELECT * FROM Products  
ORDER BY Price ASC|DESC;
-- Ascending , descending 
-- strings are alphabetically ordered, to reverse do: DESC

SELECT * FROM Customers  
ORDER BY Country, CustomerName;
-- orders by Country, but if some rows have same Country, orders by CustomerName 

SELECT * FROM Customers  
ORDER BY Country ASC, CustomerName DESC;
-- uses both ASC and DESC
```

```mysql
-- AND
SELECT *  
FROM Customers  
WHERE Country = 'Spain' AND CustomerName LIKE 'G%';

-- OR
SELECT *  
FROM Customers  
WHERE Country = 'Germany' OR Country = 'Spain';

-- AND + OR in a statement
SELECT * FROM Customers  
WHERE Country = 'Spain' AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');

-- NOT
SELECT * FROM Customers  
WHERE NOT Country = 'Spain';
```

```mysql
INSERT INTO 

INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)  
VALUES
('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway'),  
('Greasy Burger', 'Per Olsen', 'Gateveien 15', 'Sandnes', '4306', 'Norway'),  
('Tasty Tee', 'Finn Egan', 'Streetroad 19B', 'Liverpool', 'L1 0AA', 'UK');
-- Multiple values

-- into specific columns: 
INSERT INTO Customers (CustomerName, City, Country)  
VALUES ('Cardinal', 'Stavanger', 'Norway');

```

```mysql]
IS NULL, IS NOT NULL

SELECT CustomerName, ContactName, Address  
FROM Customers  
WHERE Address IS (NOT) NULL;

```

```mysql
UPDATE -- update data in a table

UPDATE Customers  
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'  
WHERE CustomerID = 1;
-- WHERE is important, if omitted then all records will be updated to new values
```

```mysql
-- DELETE
DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';


DELETE FROM Customers;
-- delete all rows in Customers table, w/o deleting the table

```

```mysql
-- TOP / LIMIT
SELECT TOP 3 * FROM Customers;

-- mySQL looks like:
SELECT * FROM Customers  
ORDER BY CustomerName DESC  
LIMIT 3;
```

```mysql
-- Aggregate Functions
/*
MIN()
MAX()
COUNT()
SUM()
AVG()
functions igonore null values except for COUNT()
*/

SELECT SUM(Quantity) FROM OrderDetails
WHERE ProductId = 11;



-- LIKE operator
SELECT * FROM Customers  
WHERE CustomerName LIKE 'a%';
-- % = zero, one or multiple character
-- "_" = one single character



-- IN operator
SELECT * FROM Customers  
WHERE Country IN ('Germany', 'France', 'UK');

-- can also subquery

SELECT * FROM Customers  
WHERE CustomerID IN (SELECT CustomerID FROM Orders);



-- BETWEEN
SELECT * FROM Products  
WHERE Price BETWEEN 10 AND 20;
-- between a range

SELECT * FROM Products  
WHERE ProductName BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni'  
ORDER BY ProductName;
-- alphabetically between CT and Mozz


-- ALIAS (AS) - temp name to table, or a column in table
-- only exists for duration of that query
SELECT CustomerID AS ID  
FROM Customers;

-- can be written wo/ AS an still work:

SELECT CustomerID ID  
FROM Customers;

```

```mysql
JOIN -- combine rows from 2 or more tables, based on related column between them 

SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate  
FROM Orders  
INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
-- Orders (Left), Customers (Right) | order matters
-- meaning that LEFT and RIGHT JOIN are mirrors of each other
/* 
JOIN - matching on both tables
LEFT JOIN - all records from left, and matched records on right
RIGHT JOIN - all records from right, and matched records on left
FULL JOIN - all records when match is in either left or right table
*/
```
![[Pasted image 20240913161524.png]]


```mysql
UNION -- used to combine the result set of 2 or more select statements
-- Every `SELECT` statement within `UNION` must have the same number of columns
-- The columns must also have similar data types
-- The columns in every `SELECT` statement must also be in the same order
-- Selects only Distinct Values, use UNION ALL to select duplicates

SELECT City FROM Customers  
UNION  
SELECT City FROM Suppliers  
ORDER BY City;
-- returns cities from both 'Customers' and 'Suppliers' table
```

```mysql
GROUP BY -- groups rows that have the same values into summary rows
-- often used with aggregate functions

SELECT COUNT(CustomerID), Country  
FROM Customers  
GROUP BY Country
ORDER BY COUNT(CustomerID) DESC;
-- number of customers in each country, sorted high to low

SELECT Shippers.ShipperName, COUNT(Orders.OrderID) AS NumberOfOrders FROM Orders  
LEFT JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID  
GROUP BY ShipperName;
-- number of orders sent by each shipper
```

```mysql
HAVING -- added to SQL bc WHERE cannot be used with aggregate functions
-- same as WHERE

SELECT COUNT(CustomerID), Country  
FROM Customers  
GROUP BY Country  
HAVING COUNT(CustomerID) > 5;


SELECT Employees.LastName, COUNT(Orders.OrderID) AS NumberOfOrders  
FROM Orders  
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID  
WHERE LastName = 'Davolio' OR LastName = 'Fuller'  
GROUP BY LastName  
HAVING COUNT(Orders.OrderID) > 25;
-- list if employees "Davolio" OR "Fuller" have registered more than 25 orders

```

```mysql
EXISTS -- used to test for the existence of any record in a sub query

SELECT SupplierName  
FROM Suppliers  
WHERE EXISTS (SELECT ProductName FROM Products WHERE Products.SupplierID = Suppliers.supplierID AND Price < 20);
-- returns multiple records
```

```mysql
ANY, ALL -- allow you to perform a comparison between a single column value and a range of other values.

ANY -- condition will be true if the operation for any of values in the range

SELECT ProductName  
FROM Products  
WHERE ProductID = ANY  
  (SELECT ProductID  
  FROM OrderDetails  
  WHERE Quantity = 10);
-- lists the ProductName if it finds ANY records in OrderDetails table has Quantity = 10 

ALL -- will be true only if the operation is true for all values in the range

SELECT ProductName  
FROM Products  
WHERE ProductID = ALL  
  (SELECT ProductID  
  FROM OrderDetails  
  WHERE Quantity = 10);

```

```mysql
SELECT INTO -- copies data from one table into a new table
-- syntax
SELECT * |  _column1_, _column2_, _column3_, ...
INTO _newtable_ [IN _externaldb_]  
FROM _oldtable  
_WHERE _condition_;

SELECT * INTO CustomersBackup2017  
FROM Customers;

-- copy table into new table from another database
SELECT * INTO CustomersBackup2017 IN 'Backup.mdb'  
FROM Customers;


-- copes data from more than one table into a new table
SELECT Customers.CustomerName, Orders.OrderID  
INTO CustomersOrderBackup2017  
FROM Customers  
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID;
```

```mysql
INSERT INTO SELECT  -- copies data from one table and isnerts it into another table
-- source table and target table data type must match

-- Syntax
INSERT INTO _table2_ (_column1_, _column2_, _column3_, ...)  
SELECT _column1_, _column2_, _column3_, ...  
FROM _table1_  
WHERE _condition_;

INSERT INTO Customers (CustomerName, City, Country)  
SELECT SupplierName, City, Country FROM Suppliers  
WHERE Country='Germany';
```
