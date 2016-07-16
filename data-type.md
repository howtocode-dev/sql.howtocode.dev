# ডাটা টাইপ

| ডাটা টাইপ |  বর্ননা | ডাটা সাইজ |
| -- | -- | -- |
|char(n)|Fixed width character string. Maximum 8,000 characters|Defined width|
|varchar(n)|Variable width character string. Maximum 8,000 characters|2 bytes + number of chars|
|varchar(max)|Variable width character string. Maximum 1,073,741,824 characters|2 bytes + number of chars|
|text|Variable width character string. Maximum 2GB of text data|4 bytes + number of chars|
|nchar|Fixed width Unicode string. Maximum 4,000 characters|Defined width x 2|
|nvarchar|Variable width Unicode string. Maximum 4,000 characters|0|
|nvarchar(max)|Variable width Unicode string. Maximum 536,870,912 characters| 0 |
|ntext|Variable width Unicode string. Maximum |2GB of text data|
|bit|Allows 0, 1, or NULL|
|binary(n)|Fixed width binary string. Maximum 8,000 bytes|
|varbinary|Variable width binary string. Maximum 8,000 bytes|
|varbinary(max)|Variable width binary string. Maximum 2GB|
|image|Variable width binary string. Maximum 2GB|
|tinyint|Allows whole numbers from 0 to 255|1 byte|
|smallint|Allows whole numbers between -32,768 and 32,767|2 bytes|
|int|Allows whole numbers between -2,147,483,648 and 2,147,483,647|4 bytes|
|bigint|Allows whole numbers between -9,223,372,036,854,775,808 and 9,223,372,036,854,775,807|8 bytes|
|decimal(p,s)|Fixed precision and scale numbers. Allows numbers from -10^38 +1 to 10^38 –1. The p parameter indicates the maximum total number of digits that can be stored (both to the left and to the right of the decimal point). p must be a value from 1 to 38. Default is 18.The s parameter indicates the maximum number of digits stored to the right of the decimal point. s must be a value from 0 to p. Default value is 0|5-17 bytes|
|numeric(p,s)|Fixed precision and scale numbers. Allows numbers from -10^38 +1 to 10^38 –1.The p parameter indicates the maximum total number of digits that can be stored (both to the left and to the right of the decimal point). p must be a value from 1 to 38. Default is 18.The s parameter indicates the maximum number of digits stored to the right of the decimal point. s must be a value from 0 to p. Default value is 0||5-17 bytes|
|smallmoney|Monetary data from -214,748.3648 to 214,748.3647|4 bytes|
|money|Monetary data from -922,337,203,685,477.5808 to 922,337,203,685,477.5807|8 bytes|
|float(n)|Floating precision number data from -1.79E + 308 to 1.79E + 308.|
|The n parameter indicates whether the field should hold 4 or 8 bytes. float(24) holds a 4-byte field and float(53) holds an 8-byte field. Default value of n is 53.|4 or 8 bytes|
|real|Floating precision number data from -3.40E + 38 to 3.40E + 38|4 bytes|
|datetime|From January 1, 1753 to December 31, 9999 with an accuracy of 3.33 milliseconds|8 bytes|
|datetime2|From January 1, 0001 to December 31, 9999 with an accuracy of 100 nanoseconds|6-8 bytes|
|smalldatetime|From January 1, 1900 to June 6, 2079 with an accuracy of 1 minute|4 bytes|
|date|Store a date only. From January 1, 0001 to December 31, 9999|3 bytes|
|time|Store a time only to an accuracy of 100 nanoseconds|3-5 bytes|
|datetimeoffset|The same as datetime2 with the addition of a time zone offset|8-10 bytes|
|timestamp|Stores a unique number that gets updated every time a row gets created or modified. The timestamp value is based upon an internal clock and does not correspond to real time. Each table may have only one timestamp variable|