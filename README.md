# PHP留言板小程序
基于LMAP的的PHP应用 

数据库名 book_db

以下是数据库表创建语句 
## 用户注册表
```
CREATE TABLE T_USER_LOGIN( uuid INTEGER(4) ZEROFILL UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY, username VARCHAR(20) NOT NULL, password VARCHAR(128) NOT NULL, ip_reg VARCHAR(128) NOT NULL, time_reg INT NOT NULL, permission TINYINT(1) UNSIGNED NOT NULL DEFAULT 2 )engine='innodb' charset=utf8;
```
## 用户留言表
```
CREATE TABLE T_USER_MESSAGE( message_id int UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY, ip_user_post VARCHAR(128) NOT NULL, title LONGTEXT BINARY NOT NULL, content LONGTEXT BINARY NOT NULL, time_post INT NOT NULL, time_last_change INT NOT NULL , lock_message TINYINT(1) UNSIGNED NOT NULL DEFAULT 0 )engine='innodb' charset=utf8;
```
