# স্ট্রিং অপারেশন

কোন কলামের স্ট্রিং ডাটা আপার-কেসে দেখানোর জন্য `UCASE()` ফাংশন টি ব্যবহার করা হয়।

**SQL UCASE() সিনট্যাক্স**
```sql
SELECT UCASE(column_name) FROM table_name;
```

কোন কলামের স্ট্রিং ডাটা লোয়ার-কেসে দেখানোর জন্য `LCASE()` ফাংশন টি ব্যবহার করা হয়।

**SQL LCASE() সিনট্যাক্স**
```sql
SELECT LCASE(column_name) FROM table_name;
```

কোন কলামের স্ট্রিং ডাটা ছোট করে দেখানোর জন্য `MID()` ফাংশন টি ব্যবহার করা হয়। একই কাজ `SUBSTRING()` ফাংশন দিয়েও করা যায়।

**SQL MID() সিনট্যাক্স**
```sql
SELECT MID(column_name,start,length) AS some_name FROM table_name;
```
**SQL SUBSTRING সিনট্যাক্স**
```sql
SELECT SUBSTRING(column_name,start,length) AS some_name FROM table_name;
```
উদাহরনঃ
```sql
SELECT MID(city,1,4) AS short_city
FROM customers;
```
```sql
SELECT SUBSTRING(city,1,4) AS short_city
FROM customers;
```

দুই বা ততোধিক কলামের ডাটা এক সাথে যুক্ত করার জন্য CONCAT() ফাংশনটি ব্যবহার করা হয়।

**SQL CONCAT() সিনট্যাক্স**

```sql
SELECT CONCAT(str1,str2,...) AS al_name
FROM table;
```
উদাহরনঃ
```sql
SELECT CONCAT(col_1,col_2) AS al_name
FROM table;
```

স্ট্রিং সম্পর্কিত আরও ফাংশন সম্পর্কে জানতে [এই সাইট](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html) ভিজিট করুন।
