# 100pian网站数据

### 1. 网址：
http://search.100pian.com

### 2. 数据下载：
http://search.100pian.com/shuju.tar.gz

### 3. 数据恢复：
https://www.cnblogs.com/zhujunxiong/p/7631001.html

### 4. 表结构：
CREATE TABLE `shujutable` (
  `name` varbinary(200) NOT NULL DEFAULT '',
  `xueke` varbinary(20) NOT NULL DEFAULT '',
  `leibie` varbinary(40) NOT NULL DEFAULT '',
  `shijian` datetime DEFAULT NULL,
  `jihe` mediumblob,
  `nameIndex` varbinary(2000) DEFAULT NULL,
  `qianzhui` varbinary(200) DEFAULT '',
  `houzhui` varbinary(50) DEFAULT '',
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `click_cnt` int(11) DEFAULT '0',
  PRIMARY KEY (`id`),
  UNIQUE KEY `name` (`name`),
  KEY `xueke` (`xueke`),
  KEY `leibie` (`leibie`),
  KEY `click_cnt` (`click_cnt`),
  KEY `xueke_3` (`xueke`,`leibie`),
  KEY `xueke_4` (`xueke`,`click_cnt`),
  KEY `xueke_5` (`xueke`,`leibie`,`id`)
) ENGINE=InnoDB DEFAULT CHARSET=binary；

### 5. 补充说明：
nameIndex是分词后的name字段。

### 6. 数据问题联系：
微信：guangtoufangyang
