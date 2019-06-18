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
其中两个字段说明：<name>标识集合名称，<jihe>表示集合内容，<nameIndex>是分词后的<name>，举个例子：
  name: C语言complex库函数
  jihe: cacos|||cacosf|||cacosl|||casin|||casinf|||casinl|||catan|||catanf|||catanl|||ccos|||ccosf|||ccosl|||csin|||csinf|||csinl|||ctan|||ctanf|||ctanl|||cacosh|||cacoshf|||cacoshl|||casinh|||casinhf|||casinhl|||catanh|||catanhf|||catanhl|||ccosh|||ccoshf|||ccoshl|||csinh|||csinhf|||csinhl|||ctanh|||ctanhf|||ctanhl|||cexp|||cexpf|||cexpl|||clog|||clogf|||clogl|||cabs|||cabsf|||cabsl|||cpow|||cpowf|||cpowl|||csqrt|||csqrtf|||csqrtl|||carg|||cargf|||cargl|||cimag|||cimagf|||cimagl|||cong|||congf|||congl|||cproj|||cprojf|||cprojl|||creal|||crealf|||creall
  nameIndex: C,语言,complex,库,函数,
  
### 5. 补充说明：
nameIndex是分词后的name字段。

### 6. 数据问题联系：
微信：guangtoufangyang
