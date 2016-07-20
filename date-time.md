# সময় ও তারিখ এর ব্যবহার

মাইসিকুয়েল এ সময় এবং তারিখ নিয়ে কাজ করার জন্য বেশ কিছু বিল্ট-ইন ফাংশন আছে।
<br><br>

**`NOW()`** ফাংশনটি বর্তমান সময় `Y-m-d H:i:s` ফরম্যাটে রিটার্ন করে।

উদাহরনঃ

```sql
SELECT NOW() FROM table_name;
```
<br>

**`CURDATE()`** ফাংশনটি বর্তমান তারিখ `Y-m-d` ফরম্যাটে রিটার্ন করে।

উদাহরনঃ

```sql
SELECT * FROM table_name WHERE date_col = CURDATE();
```
<br>

**`CURTIME()`** ফাংশনটি বর্তমান সময় `H:i:s` ফরম্যাটে রিটার্ন করে।

উদাহরনঃ

```sql
SELECT * FROM table_name WHERE date_col = CURTIME();
```
<br>

**`DATE()`** ফাংশনটি ডাটা থেকে `Y-m-d ` ফরম্যাটে তারিখ  রিটার্ন করে।

উদাহরনঃ

```sql
SELECT ProductName, DATE(OrderDate) AS OrderDate
FROM Orders
WHERE OrderId=1
```

<br>
**`DATEDIFF()`**  ফাংশনটি দুইটি তারিখের মধ্যবর্তী সময়/দিন প্রকাশ করে।

উদাহরনঃ

```sql
SELECT DATEDIFF('2014-11-29','2014-11-30') AS DiffDate
```
