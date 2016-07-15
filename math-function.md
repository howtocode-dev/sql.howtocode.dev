# গানিতিক অপারেশন

SQL AVG() Syntax
```sql
SELECT AVG(column_name) FROM table_name
```
```sql
SELECT ProductName, Price FROM Products
WHERE Price>(SELECT AVG(Price) FROM Products);
```

SQL MAX() Syntax
```sql
SELECT MAX(column_name) FROM table_name;
```
```sql
SELECT MAX(Price) AS HighestPrice FROM Products;
```
SQL MIN() Syntax
```sql
SELECT MIN(column_name) FROM table_name;
```
```sql
SELECT MIN(Price) AS SmallestOrderPrice FROM Products;
```
SQL SUM() Syntax
```sql
SELECT SUM(column_name) FROM table_name;
```
```sql
SELECT SUM(Quantity) AS TotalItemsOrdered FROM OrderDetails;
```

SQL ROUND() Syntax
```sql
SELECT ROUND(column_name,decimals) FROM table_name;
```
```sql
SELECT ProductName, ROUND(Price,0) AS RoundedPrice
FROM Products;
```