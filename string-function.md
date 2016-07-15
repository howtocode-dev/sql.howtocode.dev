# স্ট্রিং অপারেশন

SQL UCASE()
```sql
SELECT UCASE(column_name) FROM table_name;
```

SQL LCASE()

```sql
SELECT LCASE(column_name) FROM table_name;
```


SQL MID() 
```sql
SELECT MID(column_name,start,length) AS some_name FROM table_name;
```
```sql
SELECT MID(City,1,4) AS ShortCity
FROM Customers;
```

SQL SUBSTRING
```sql
SELECT SUBSTRING(column_name,start,length) AS some_name FROM table_name;
```