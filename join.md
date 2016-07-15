# JOIN
দুই বা ততোধিক টেবিলের  রো একসাথে যুক্ত করতে `SQL JOIN` ব্যবহার করা হয়। SQL এ JOIN মোট ৪ প্রকারের।

##INNER JOIN
INNER JOIN কীওয়ার্ড দিয়ে দুই বা ততোধিক টেবিলের রো একসাথে যুক্ত করতে হলে তুলনাকারী কলামের মান সমান হতে হয়। অনেকটা কমন নেওয়ার মত।
 
**`SQL INNER JOIN` সিনট্যাক্স**
```sql
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name=table2.column_name;
```
অথবা,

```sql
SELECT column_name(s)
FROM table1
JOIN table2
ON table1.column_name=table2.column_name;
```

উদাহরনঃ
```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
INNER JOIN Orders
ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;
```