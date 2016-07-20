# বেসিক এসকিউএল কমান্ড'স

## সিলেক্ট

** `SQL SELECT` সিনট্যাক্স **
```sql
SELECT column_name,column_name
FROM table_name;
```
এবং
```sql
SELECT * FROM table_name;
```

## ইনসার্ট

** `SQL INSERT INTO` সিনট্যাক্স **

কলামের নাম ছাড়া
```sql
INSERT INTO table_name
VALUES (value1,value2,value3,...);
```
কলামের নাম সহ
```sql
INSERT INTO table_name (column1,column2,column3,...)
VALUES (value1,value2,value3,...);
```

## আপডেট

** `SQL UPDATE` সিনট্যাক্স **
```sql
UPDATE table_name
SET column1=value1,column2=value2,...
WHERE some_column=some_value;
```

## ডিলিট

** `SQL DELETE` সিনট্যাক্স **
```sql
DELETE FROM table_name
WHERE some_column=some_value;
```

## WHERE

**`SQL WHERE` সিনট্যাক্স **
```sql
SELECT field1, field2,...fieldN table_name1, table_name2...
[WHERE condition1 [AND [OR]] condition2.....
```

WHERE এর অপারেটর সমূহঃ

| অপারেটর | বর্ণনা |
| -- | -- |
| = | সমান বোঝাতে |
| <> | সমান নয় বোঝাতে  |
| != | সমান নয় বোঝাতে  |
| > | বৃহত্তর  বোঝাতে |
|<| ক্ষুদ্রতর বোঝাতে  |
|>=|বৃহত্তর  অথবা সমান বোঝাতে |
|<=| ক্ষুদ্রতর অথবা সমান বোঝাতে  |
|BETWEEN| দুইয়ের মধ্যে আছে বোঝাতে  |
|LIKE| খোজা বোঝাতে |
|IN| একাধিক সম্ভাব্য মান আছে বোঝাতে |


উদাহরনঃ
```sql
SELECT * FROM Customers
WHERE Country='Bangladesh';
```
```sql
SELECT * FROM Customers
WHERE Id=1;
```
```sql
SELECT * FROM Customers
WHERE Id=1 AND Country='Bangladesh';
```
```sql
SELECT * FROM Customers
WHERE Id=1 OR Country='Bangladesh';
```

## ORDER BY
এক বা একাধিক কলামের ডাটা সর্ট করতে ORDER BY ক্লস ব্যবহৃত হয়ে থাকে। ডিফল্ট ORDER ASC এসেন্ডিং (আরোহী)।

**ASC = Ascending / আরোহী / উর্ধক্রম **<br>
**DESC = Descending / অবরোহী / নিম্নক্রম**

**`SQL ORDER BY` সিনট্যাক্স **
```sql
SELECT column_name, column_name
FROM table_name
ORDER BY column_name ASC|DESC, column_name ASC|DESC;
```

উদাহরনঃ
```sql
SELECT * FROM Customers
ORDER BY Country;
```

```sql
SELECT * FROM Customers
ORDER BY Country DESC;
```

```sql
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;
```

## GROUP BY

একই ধরনের ডাটার GROUP তৈরি করতে GROUP BY ক্লস ব্যবহৃত হয়ে থাকে।

**`SQL ORDER BY` সিনট্যাক্স **
```sql
SELECT column_name, aggregate_function(column_name)
FROM table_name
WHERE column_name operator value
GROUP BY column_name;
```
উদাহরনঃ
```sql
SELECT Shippers.ShipperName,COUNT(Orders.OrderID) AS NumberOfOrders FROM Orders
LEFT JOIN Shippers
ON Orders.ShipperID=Shippers.ShipperID
GROUP BY ShipperName;
```

```sql
SELECT Shippers.ShipperName, Employees.LastName,
COUNT(Orders.OrderID) AS NumberOfOrders
FROM ((Orders
INNER JOIN Shippers
ON Orders.ShipperID=Shippers.ShipperID)
INNER JOIN Employees
ON Orders.EmployeeID=Employees.EmployeeID)
GROUP BY ShipperName,LastName;
```

## SQL Alias

আপনি চাইলে কোন টেবিল অথবা কলামের নাম সাময়িক ভাবে পরিবর্তন করতে পারেন এলিয়াস  ব্যবহার করে।

**`SQL Alias` সিনট্যাক্স **
```sql
SELECT column_name AS alias_name
FROM table_name;
```
উদাহরনঃ
```sql
SELECT column_name(s)
FROM table_name AS alias_name;
```

```sql
SELECT CustomerName AS Customer, ContactName AS Contact_Person
FROM Customers;
```

```sql
SELECT CustomerName, CONCAT(Address,', ',City,', ',PostalCode,', ',Country) AS Address
FROM Customers;
```
