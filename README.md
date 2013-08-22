freebsd
=======

Freebsd PHP5.3, PHP5.4, PHP5.5 同时安装. 快速切换PHP版本. 非3版本同时运行

学习SHELL写的脚本, 只是方便切换PHP版本 并不是3个版本同时运行.

Apache Mysql Postgresql 都是用ports安装

分别编译php5.3 php5.4 php5.5 并安装在不同的目录


Virtualbox Freebsd 9.1-p5 测试

bsd-config  sh脚本, 判断ports perl python wget vim bash安装状态, 添加ports安装选项到/etc/make.conf

bsd-appmm   bash脚本, 判断apache24 mysql55-server postgresql92-server安装状态, 判断php依赖组件并从ports安装. 
            
            PHP版本依从于/usr/ports/lang/php5, ports/lang/php53, ports/lang/php55 中对应的版本
            
            自动编译配置安装在/usr/local目录下 分别为 php-5.3, php-5.4, php-5.5
            

默认没开启php加载, 需手动修改/usr/local/etc/apache24/httpd.conf最下面

#Include etc/apache24/extra/php-5.3.conf
#Include etc/apache24/extra/php-5.4.conf
#Include etc/apache24/extra/php-5.5.conf

使用哪个版本加载哪个conf即可

 
