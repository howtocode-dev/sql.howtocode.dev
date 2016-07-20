# JOIN
দুই বা ততোধিক টেবিলের  রো একসাথে যুক্ত করতে `SQL JOIN` ব্যবহার করা হয়। SQL এ JOIN মোট ৪ প্রকারের।

##INNER JOIN
INNER JOIN কি-ওয়ার্ড দিয়ে দুই বা ততোধিক টেবিলের রো একসাথে যুক্ত করতে হলে বাম ও ডান কলামের মান সমান হতে হয়।

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


## LEFT JOIN
`LEFT JOIN` কি-ওয়ার্ড দিয়ে দুই বা ততোধিক টেবিলের রো একসাথে যুক্ত করতে হলে বাম কলামের রো এর ডাটার সাথে ডান কলামের রো এর ডাটা তুলনা করা হয় । যেসব স্থানে উভয় কলামের রো এর ডাটা সমান নয় সেসকল ক্ষেত্রে শুধুমাত্র বাম কলামের ডাটা সিলেক্ট করা হয় , আর যেসব স্থানে উভয় কলামের রো এর ডাটা সমান সে ক্ষেত্রে উভয় কলামের রো এর ডাটা সিলেক্ট করা হয়।

**`SQL LEFT JOIN` সিনট্যাক্স**
```sql

SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name=table2.column_name;
```
অথবা,

```sql
SELECT column_name(s)
FROM table1
LEFT OUTER JOIN table2
ON table1.column_name=table2.column_name;
```
উদাহরনঃ
```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders
ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;
```

## RIGHT JOIN

`RIGHT  JOIN` কি-ওয়ার্ড দিয়ে দুই বা ততোধিক টেবিলের রো একসাথে যুক্ত করতে হলে বাম কলামের রো এর ডাটার সাথে ডান কলামের রো এর ডাটা তুলনা করা হয় । যেসব স্থানে উভয় কলামের রো এর ডাটা সমান নয় সেসকল ক্ষেত্রে শুধুমাত্র ডান কলামের ডাটা সিলেক্ট করা হয় , আর যেসব স্থানে উভয় কলামের রো এর ডাটা সমান সে ক্ষেত্রে উভয় কলামের রো এর ডাটা সিলেক্ট করা হয়। এটি `LEFT JOIN` এর বিপরীত।

**`SQL RIGHT JOIN` সিনট্যাক্স**
```sql
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name=table2.column_name;
```
অথবা,

```sql
SELECT column_name(s)
FROM table1
RIGHT OUTER JOIN table2
ON table1.column_name=table2.column_name;
```

উদাহরনঃ
```sql
SELECT Orders.OrderID, Employees.FirstName
FROM Orders
RIGHT JOIN Employees
ON Orders.EmployeeID=Employees.EmployeeID
ORDER BY Orders.OrderID;
```


## FULL JOIN

`FULL JOIN` মূলত `LEFT JOIN` এবং `RIGHT JOIN` এর ফলাফল একসাথে যুক্ত করে প্রকাশ করে।

**`SQL FULL OUTER JOIN` সিনট্যাক্স**
```sql
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name=table2.column_name;
```

উদাহরনঃ
```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders
ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;
```
