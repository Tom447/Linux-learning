# 1.为什么需要使用Linux?

```java
Linux是一款基于Unix开源免费的操作系统,安全和稳定性极高,所有成为了软件程序运行的最佳环境.
    安全: 在Linux系统中默认情况下只有22端口对外开放
    稳定: 7*24小时可用(全天候)
作用: 部署java项目
```

# 2.操作系统分类?

```java
站在使用者角度:
	桌面版:
        windows
        Linux
    服务器版:
        Linux ★
    移动版:
        Android: 底层依赖Linux
    嵌入式版:
        路由器: Linux
根据原生程度:
	内核版
    发行版: 我们使用的都是发行版
		centos6.5 : iptables
        centos7★ : firewalld
```

# 3.虚拟机是什么?

```java
虚拟机是window平台上的一款软件,安装此软件后.此软件可以向真机索要固定的硬盘和内存空间,虚拟出一台小型计算机.
VMware 16.1
```

# 4.Linux目录结构?

```java
/ : 系统根目录
    root : 超级管理员的家目录
    home : 普通用户的家目录
        zhangsan
        liuyan
        tiansuo
    etc : 系统配置文件目录
    usr : 多用户共享目录
    tmp : 临时目录
    ....
```

# 5.Linux客户端软件

```java
作用: 通过客户端软件可以远程访问Linux系统.
finalshell:
MX:
```

# 6.Linux相关命令

## 6.1 目录切换

```sh
cd /    
cd ..
cd ../
cd home
cd /home
cd -
cd ~
```

## 6.2 创建目录

```sh
mkdir aa
mkdir -p bb/bbb
mkdir /cc
```

## 6.3 复制和剪切

```java
cp hello.txt /aa
cp /tmp/hello.txt /bb
cp /tmp/hello.txt /bb/hello.txt

cp -r aa /cc
cp -r /tmp/aa /tmp/cc
cp -r /tmp/aa /tmp/cc/abc
    
mv hello.txt /aa
mv /tmp/hello.txt /bb
mv /tmp/hello.txt /bb/hello.txt
    
mv -r aa /cc
mv -r /tmp/aa /tmp/cc
mv -r /tmp/aa /tmp/cc/abc
```

## 6.4 创建文件

```java
touch hello.txt
touch /tmp/hello.txt
```

## 6.5 删除

```sh
rm -rf hello.txt
rm -rf aa
rm -rf ./*
```

## 6.6 压缩包

```java
打包扩展名: *.tar
压缩扩展名: *.gz
注: 在Linux中打包和压缩一般是一起的 *.tar.gz
打包并压缩:
	tar -zcvf ziliao.tar.gz a.txt b.txt ....
解压缩:
	tar -zxvf ziliao.tar.gz
    tar -zxvf ziliao.tar.gz -C /tmp/bb
```

## 6.7 编辑文件(★)

```sh
vim/vi 文件名(打开文件) --->
按 i/a/o (进入编辑模式) ---> 
对文件进行编辑 ---> 
按 esc(一个键)  ---> 
按 : (进入低行模式)  ---> 
按 wq(写入并退出) 或 wq!(强制写入并退出) 或 q!(强制退出不保存)

便捷操作: 便捷操作在打开文件后进行
	G
	gg
	dd
	ndd
	u
	shift + zz
	:set nu
	:set nonu
	:n
	/要查找的关键字
```

## 6.8 查看

```java
find / -name "a*"
find ./ -name "a*"

grep [-inv] 关键字 文件名
```

# 7.写入3到5个Linux常用命令



# 8.Linux的快照是什么?有什么作用?

```java
快照: 将Linux瞬时的状态进行保存
作用: 保存了快照后,可以在Linux上进行各种操作,即便出了问题,可以进行快照恢复.
```

# 9.Linux软件安装的多种方式?

```java
二进制包安装: 直接将对应的压缩包解压即可
rpm包安装: 运行软件对应的rmp文件(需要手动解决软件的环境依赖)
yum在线安装: 本质上就是rpm安装,只不过yum会解决软件安装时的依赖问题
源码编译安装: 下载软件对应的源码,将源码编译后进行安装.
    redis(使用c语言开发):
		1.在Linux平台安装C语言环境
        2.将redis的源码上传到Linux
        3.编译源码
        4.安装软件
Docker: 码头工人
    1.下载软件对应的镜像
    2.运行镜像成容器
```

# 10.网络/防火墙管理命令

```java
ping ip地址 : 验证指定的ip是否可以被访问
ip addr : 查看网络信息
ifconfig : 查看网络信息
ps -ef : 查看Linux平台正在运行的所有进程
    ps -ef | grep tomcat | grep -v grep
systemctl start firewalld
systemctl stop firewalld
systemctl restart firewalld
systemctl status firewalld
systemctl disable firewalld
systemctl enable firewalld
....
```

# 11.手动部署项目流程

```java
1.在Linux平台搭建软件环境(jdk,mysql,tomcat)
2.将window平台上的项目打包并上传到Linux平台
3.运行项目
    java -jar xxx.jar
    nohup java-jar xxx.jar &>日志.log &
```

# 12.简述shell脚本的作用

```java
将Linux相关命令,按照指定的逻辑,编写在一个Xxx.sh文件中.
并修改权限,执行此脚本文件时,脚本文件中的Linux命令有序执行(可以理解为对Linux命令进行编排).
```

# 13.简述自动部署项目流程

```java
Idea(编写项目) --提交--> Gitee(马云仓库) ----> Git(拉取仓库中的代码) ----> 由maven进行清理,打包,运行
```

# 14.Linux文件的权限

```java
在Linux中执行 ls -l 或 ll 命令时,显示文件对应的权限信息:
- --- --- ---
  第一位:文件类型位
      - :表示文件
      d :表示文件夹
      l :链接,相当于window中的快捷方式
  2-4位:属主,文件创建者的权限位
  5-7位:属组,与主人同组,组员的权限
  8-10位:其他用户的权限
r: 读,4
w: 写,2
x: 操作,1
修改权限方式:
	chmod u=rwx,g=rw-,o=rw- 文件名
    chmod 766 文件名
```

# 15.静态IP配置

```java
IP分配模式:
	dhcp: 默认模式,随机分配ip地址,Linux开启重启可能会变动,因为是随机分配的
    static: 静态ip地址,需要在配置静态ip地址
        如下:
			cd /etc/sysconfig/network-scripts/
            vim ifcfg-ens33
```

```java
TYPE=Ethernet
PROXY_METHOD=none
BROWSER_ONLY=no
BOOTPROTO=static
DEFROUTE=yes
IPV4_FAILURE_FATAL=no
IPV6INIT=yes
IPV6_AUTOCONF=yes
IPV6_DEFROUTE=yes
IPV6_FAILURE_FATAL=no
IPV6_ADDR_GEN_MODE=stable-privacy
NAME=ens33
UUID=afd0baa3-8bf4-4e26-8d20-5bc426b75fd6
DEVICE=ens33
ONBOOT=yes
ZONE=public
    
IPADDR="192.168.163.130"        # 设置的静态IP地址
NETMASK="255.255.255.0"         # 子网掩码
GATEWAY="192.168.163.2"         # 网关地址
DNS1="192.168.163.2"            # DNS服务器
```











































