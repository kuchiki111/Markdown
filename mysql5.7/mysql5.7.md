# CentOS 7使用rpm命令安装mysql5.7

CentOS 7的yum源中已经没有mysql-server的安装文件如果使用

```
yum install mysql-community-server -y
```
会发现安装的并不是mysql，而是Mariadb。MariaDB是mysql的分支，只要是由开源社区来维护，MariaDB是完全兼容mysql的，在日常的开发过程中也不会有很大的区别。但是很多人并不能一下接受这个新的，依旧想装mysql。