![](https://statict.cn/store/uploads/tinymce/images/88d5d4826cd05d72ea11b1a44b6ff7fa63f8c7619862c.png)

在安装之前请在对应数据库执行Sql：
```sql
SET NAMES utf8mb4;
SET FOREIGN_KEY_CHECKS = 0;

DROP TABLE IF EXISTS admin_extension_histories;
CREATE TABLE admin_extension_histories (
  id int(10) unsigned NOT NULL AUTO_INCREMENT,
  name varchar(100) NOT NULL,
  type tinyint(4) NOT NULL DEFAULT '1',
  version varchar(20) NOT NULL DEFAULT '0',
  detail text,
  created_at datetime DEFAULT NULL,
  updated_at datetime DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8mb4;

DROP TABLE IF EXISTS admin_extensions;
CREATE TABLE admin_extensions (
  id int(10) unsigned NOT NULL AUTO_INCREMENT,
  name text,
  version text,
  is_enabled tinyint(4) DEFAULT NULL,
  options text,
  created_at datetime DEFAULT NULL,
  updated_at datetime DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8mb4;

SET FOREIGN_KEY_CHECKS = 1;
```
