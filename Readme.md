# wJa环境
jdk 1.8
# 靶场测试环境
本地mysql开启   3306端口
user：root
pass：root
创建shoot数据库
执行如下sql：
```SQL
USE `shoot`;
CREATE TABLE IF NOT EXISTS `users`(
   `id` INT UNSIGNED AUTO_INCREMENT,
   `username` VARCHAR(255) NOT NULL,
   `password` VARCHAR(255) NOT NULL,
   PRIMARY KEY (`id`)
)ENGINE=InnoDB DEFAULT CHARSET=utf8;
INSERT INTO `users` VALUES (1, 'admin', 'admin123');
INSERT INTO `users` VALUES (2, 'joychou', 'joychou123');
```

# 使用的实战环境
实战给大家带的是华夏erp的项目：https://github.com/jishenghua/jshERP
需要进行简单的配置mysql和redis
配置起来想对比较简单，大家可以自行clone然后打包，或者不进行黑盒衔接，只是白盒审计的话可以直接使用我给大家打包好的jar包

# Issus

希望大家能够提出宝贵的建议，如果程序出现一些问题能够尽早的反馈给我，我会在两到三天时间进行修复和解答，感谢大家的支持。

视频观看地址：https://www.bilibili.com/video/BV19m4y1Q75X/

# 更新历史

2022.1.3:增加获取方法参数个数，可以有效对接口所有参数进行测试

2022.1.4:修复溢出等多个已知问题

2022.1.5:修复追踪递归问题，修复反编译中if中最后while循环导致if转为while的问题

2022.1.5:增加xml文件操作类库

2022.1.6:优化追踪算法，实现完全流式追踪算法

2022.1.10:优化部分代码，对于函数部分显示正常，更加精准的展示函数分类，更新了cheetah脚本代码

2022.1.11:增加插桩IAST，通过javaagent获取真正函数流，修复对于while(true)无法反编译的bug

2022.1.13:修复switch包在while底部的错误，以及switch未排序问题

2022.1.15:增加配置选项，优化皮肤