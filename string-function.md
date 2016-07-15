# স্ট্রিং অপারেশন

কোন কলামের স্ট্রিং ডাটা আপারকেসে দেখানোর জন্য `UCASE()` ফাংশন টি ব্যবহার করা হয়।

**SQL UCASE() সিনট্যাক্স**
```sql
SELECT UCASE(column_name) FROM table_name;
```

কোন কলামের স্ট্রিং ডাটা লোয়ারকেসে দেখানোর জন্য `LCASE()` ফাংশন টি ব্যবহার করা হয়।

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
FROM Customers;
```
