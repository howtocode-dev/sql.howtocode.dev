# টেবিল
##টেবিল তৈরী

CREATE TABLE কমান্ড দিয়ে টেবিল তৈরী করতে হয়। নিচে এটি টেবিল তৈরী করার জন্য SQL কমাড লেখা হয়েছে।
  বলা হয়েছে যদি `table_name` নামে কোন টেবিল না থাকে তবে টেবিল তৈরী করতে, যার ইঞ্জিন MyISAM, ডিফল্ট ক্যারেটার সেট utf8 এবং কোলেট utf8_unicode_ci। 
```sql
CREATE TABLE IF NOT EXISTS `table_name` (
 `id` int(11) NOT NULL AUTO_INCREMENT,
 `column_name1` varchar(100) NOT NULL,
 `column_name2` varchar(100) NOT NULL,
 `column_name3` varchar(50) NOT NULL,
 PRIMARY KEY (`id`)
) ENGINE=MyISAM  DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci ;
```


##টেবিল সম্পাদনা

##টেবিল মুছে ফেলা
