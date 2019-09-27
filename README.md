# Ubuntu_Buglist


```
sudo apt-get update 
```
这一步是更新你的源列表，换源后必须执行。
这个命令，会访问源列表里的每个网址，并读取软件列表，然后保存在本地电脑。我们在软件包管理器里看到的软件列表，都是通过update命令更新的。
```
sudo apt-get upgrade
```
这个命令，会把本地已安装的软件，与刚下载的软件列表里对应软件进行对比，如果发现已安装的软件版本太低，就会提示你更新。
```
清屏  $ clear
```
[install ubuntu]:(http://wiki.ros.org/kinetic/Installation/Ubuntu)
桌面完整版安装：（推荐） 包含ROS、rqt、rviz、通用机器人函数库、2D/3D仿真器、导航以及2D/3D感知功能。

可以在终端查看主机名：Ubuntu16.04 sudo:无法解析主机 解决方案
``
hostname
```
install Vim :https://itsfoss.com/vim-8-release-install/
```

# 1.查看版本:
opencv：
```
	pkg-config --modversion opencv
```
gazebo:
```
	git branch  #显示分支列表
	得到了：master 
	git checkout v1.6.5  #退出原有分支，并切换到v1.6.5 分支。
```
cmake:
```
	cmake -version
```
make:
```
	make -v
```
ros:
```
	1、先在终端输入roscore
	2、打开新终端，再输入，rosparam list//这一步是为了查看命令，不是必须的
	3、再输入rosparam get /rosdistro就能得到版本

	或者直接：
	rosversion -d
	输出：kinetic
```
查看内核版本
```
uname -r
```
发行号：
```
cat /etc/issue
```
查看disk空间：
```
	df   -h
```

查看Qt版本：
```
	qmake -v
```
gcc:
```
	gcc -v
```
g++:
```
	g++ -v
```
ubuntu 查看python版本:
```
	python 
	ctrl + D
```
查看已安装的ssh
```
ubuntu
$ dpkg -l | grep ssh
```
# 2.安装：########


git clone 克隆git上面的到本地电脑，默认/home


dpkg
```
deb包的管理是比较优秀的包管理工具，用的linux系统有 debian ubuntu;
dpkg命令的使用：
dpkg -i *.deb文件的安装
dpkg -r *.deb文件的卸载;
```
添加说明：
最常用的就是-i，-r。简单，安装／卸载。


解压缩命令
```
unzip xx.zip 解压，
```
...


安装用户和组图形化管理界面
```
sudo apt-get install gnome-system-tools
```
APT 命令行工具的使用
```
命令apt-get 会自动帮助用户下载并安装所需的程序包或代码。 apt-get 命令一般需要root权限执行，所有还要使用sudo 命令。
sudo apt-get [选项] 子命令

apt-get update //获取最新的软件包列表，同步/etc/apt/sources.list 和/etc/apt/sources.list.d 中列出的源的索引，以确保用户能够获取最新的软件包。
apt-get upgrade //更新当前系统中所有已经安装的软件包，并同时更新这些软件包所依赖的软件包
apt-get install //下载、安装软件包并自动解决依赖关系
apt-get remove //卸载指定的软件包
```
...
# 3 root权限 #######

1.打开一个root权限的终端 直接输入 sudo su［注意：不是 su］
终端提示输入密码时输入 root用户的密码

2.终端下临时使用root权限 直接输入 sudo + 你要执行的命令,根据提示输入当前用户密码

# 4 一些工具 #######

    5分钟入手Terminator

[5分钟入手Terminator](https://www.jianshu.com/p/cee2de32ca28)


2. vim : Vim不需要费劲去按esc的几个方法。 -[ CSDN博客 ](https://blog.csdn.net/mangonova/article/details/51533741)

# 5 install
## Nvidia卡
```
sudo apt-get upgrade
#for case1: original driver installed by apt-get:

sudo apt-get remove --purge nvidia*
#for case2: original driver installed by runfile:

 sudo update-initramfs -u
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt-get update

sudo apt-get install nvidia-418
sudo apt-get install mesa-common-dev 
 sudo apt-get update

sudo apt-get upgrade
cd 桌面/

sudo apt-get update
```
## visual studio code
到微软的vscode网站  （下载地址）https://code.visualstudio.com/Download，即可安装，可以使用（  命令行输入code .  在任何目录中打开该编辑器，只用deb安装的可以命令行打开，其他不行） 推荐使用这种方法，bug最少，启动最方便

# bug
检测到系统程序问题
```
sudo gedit /etc/default/apport
```
将enabled = 1 修改为 0
