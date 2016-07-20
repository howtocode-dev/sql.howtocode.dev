# টেবিল
## টেবিল তৈরি

CREATE TABLE কমান্ড দিয়ে টেবিল তৈরি করতে হয়। নিচে এটি টেবিল তৈরি করার জন্য SQL কমান্ড লেখা হয়েছে।
  বলা হয়েছে যদি `table_name` নামে কোন টেবিল না থাকে তবে টেবিল তৈরি করতে, যার ইঞ্জিন MyISAM, ডিফল্ট ক্যারেক্টার সেট utf8 এবং কোলেট utf8_unicode_ci।
```sql
CREATE TABLE IF NOT EXISTS `table_name` (
 `id` int(11) NOT NULL AUTO_INCREMENT,
 `column_name1` varchar(100) NOT NULL,
 `column_name2` varchar(100) NOT NULL,
 `column_name3` varchar(50) NOT NULL,
 PRIMARY KEY (`id`)
) ENGINE=MyISAM  DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci ;
```


## টেবিল সম্পাদনা

`ALTER TABLE` কমান্ড দিয়ে টেবিলের স্কিমা/স্ট্রাকচার পরিবর্তন করা যায়।

**উদাহরনঃ** টেবিলে `name` নামে একটি নতুন কলাম যুক্ত করা হয়েছে নিচের কমান্ড দিয়ে।
```sql
ALTER TABLE `table_name` ADD `name` VARCHAR(50) NOT NULL AFTER `id`;
```

## টেবিল মুছে ফেলা

`DROP TABLE` কমান্ড দিয়ে টেবিল ডাটাবেস থেকে মুছে ফেলা যায়।
```sql
DROP TABLE table_name
```
