# লিনাক্স/*nix

টার্মিনালে নিচের কমান্ড দিয়ে রিপো আপডেট করুন।
```sh
sudo apt-get update
```
টার্মিনালে নিচের কমান্ড দিয়ে MySQL সার্ভার ইন্সটল করুন।
```sh
sudo apt-get install mysql-server
```
টার্মিনালে নিচের কমান্ড দিয়ে MySQL কনফিগার করুন।
```sh
sudo mysql_secure_installation
```
টার্মিনালে `mysql --version` কমান্ড দিয়ে দেখুন MySQL এর কোন ভার্শন ইন্সটল হয়েছে।


# ম্যাক

টার্মিনালে নিচের কমান্ড দিয়ে MySQL সার্ভার ইন্সটল করুন।
```sh
sudo port install mysql5-server && sudo -u _mysql /opt/local/bin/mysql_install_db5
```
MySQL সার্ভার চালু করতে টার্মিনালে নিচের কমান্ড দিন।
```sh
sudo port load mysql5-server
```

MySQL সার্ভার বন্ধ করতে টার্মিনালে নিচের কমান্ড দিন।
```sh
sudo port unload mysql5-server
```

# উইন্ডোজ

MySQL এর [অফিশিয়াল সাইট](http://dev.mysql.com/downloads/installer/) থেকে ইন্সটলার নামিয়ে ইন্সটল করুন।


## phpmyadmin
গ্রাফিক্যাল ইন্টারফেস দিয়ে MySQL ব্যবহার করতে চাইলে phpmyadmin ইন্সটল করতে পারেন। তবে এর জন্য পিএইচপি এবং Apache/Nginx/Web সার্ভার ইন্সটল করা থাকতে হবে। phpmyadmin ইন্সটল করতে টার্মিনালে নিচের কমান্ড দিন।

```sh
sudo apt-get install phpmyadmin
```

উইন্ডোজ এর জন্য [WAMP](http://www.wampserver.com/en/)/[XAMPP](https://www.apachefriends.org/download.html) ব্যবহার করুন।
