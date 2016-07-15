# সময় ও তারিখ এর ব্যবহার

SQL NOW() Syntax
SELECT NOW() FROM table_name;


Syntax
CURDATE()
Example
The following SELECT statement:

SELECT NOW(),CURDATE(),CURTIME()


he DATE() function extracts the date part of a date or date/time expression.

Syntax
DATE(date)

SELECT ProductName, DATE(OrderDate) AS OrderDate
FROM Orders
WHERE OrderId=1