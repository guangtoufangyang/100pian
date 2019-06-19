# 100pian网站数据

### 1. 数据说明：
此份数据为 http://search.100pian.com 搜索使用的原始数据，共220w+条记录。

### 2. 数据下载：
直接下载： http://search.100pian.com/shuju.tar.gz  
百度网盘： https://pan.baidu.com/s/1EQ1KOnRIjVLpT48xR5Kz8Q ，提取码：gedd

### 3. 表结构：
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
  
### 4. 数据字段说明：
 【name】标识集合名称，【jihe】表示集合内容，【nameIndex】是分词后的【name】，【xueke】和【leibie】用于数据分类，举个例子：  
 【name】: C语言complex库函数  
 【jihe】: cacos|||cacosf|||cacosl|||casin|||casinf|||casinl|||catan|||catanf|||catanl  
 【nameIndex】: C,语言,complex,库,函数,  
  
### 5. 数据问题联系：
微信：guangtoufangyang
