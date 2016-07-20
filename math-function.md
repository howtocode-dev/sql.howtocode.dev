# গাণিতিক অপারেশন


কোন কলামের ডাটাসমূহের গড় বের করার জন্য `AVG()` ফাংশনটি ব্যবহার করা হয়।

**`SQL AVG()` সিনট্যাক্স**
```sql
SELECT AVG(column_name) FROM table_name
```
উদাহরনঃ
```sql
SELECT product_name, price FROM products
WHERE price>(SELECT AVG(price) FROM products);
```

কোন কলামের ডাটাসমূহের থেকে সর্বোচ্চ মান বের করার জন্য `MAX()` ফাংশনটি ব্যবহার করা হয়।

**`SQL MAX()` সিনট্যাক্স**
```sql
SELECT MAX(column_name) FROM table_name;
```
উদাহরনঃ
```sql
SELECT MAX(price) AS max_price FROM products;
```

কোন কলামের ডাটাসমূহের থেকে সর্বনিম্ন মান বের করার জন্য `MIN()` ফাংশনটি ব্যবহার করা হয়।

**`SQL MIN()` সিনট্যাক্স**
```sql
SELECT MIN(column_name) FROM table_name;
```
উদাহরনঃ
```sql
SELECT MIN(price) AS min_price FROM products;
```

কোন কলামের ডাটাসমূহের যোগফল বের করার জন্য `SUM()` ফাংশনটি ব্যবহার করা হয়।

**`SQL SUM()` সিনট্যাক্স**
```sql
SELECT SUM(column_name) FROM table_name;
```
উদাহরনঃ
```sql
SELECT SUM(quantity) AS total_order FROM orders;
```
কোন কলামের ডাটাকে দশমিকের নির্দিষ্ট ঘর অথবা দশমিক সংখ্যাকে পূর্ণসংখ্যা হিসাবে দেখানোর জন্য `ROUND()` ফাংশনটি ব্যবহার করা হয়।

**`SQL ROUND()` সিনট্যাক্স**
```sql
SELECT ROUND(column_name,decimals) FROM table_name;
```
উদাহরনঃ
```sql
// price = 21.3545
SELECT products, ROUND(price,2) AS new_price
FROM products; // price = 21.35

SELECT products, ROUND(price) AS new_price
FROM products; // price = 21
```
