# VirtualBox安装与使用

## 概述
* VirtualBox是一款基于X86和AMD64或Intel64位的功能强大的跨平台的开源虚拟机软件，并可在Windows，Linux，Macintosh，和Solaris等大量主机上运行，并支持大量客户操作系统，包括但不限于Windows(NT 4.0,2000，XP，Server 2003，Vista，Windows 7，Windows 8，Windows 10)、DOS、Windows 3.1、Linux（2.4,2.6,3.x和4.x）、Solaris和OpenSolaris、OS/2和OpenBSD。

![图1：VirtualBox官网首页](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/1.vboxorg.png)

* VirtualBox官网语言为英语，如您对英语有阅读障碍，可使用Google Chrome浏览器打开官网可将英语翻译为您相应的母语；因是机器翻译，其准确度不佳，但不妨您理解大意。

## 下载(Download)
* 点击VirtualBox官网首页上的左侧导航栏的“Downloads”或“Download VirtualBox 5.2”的大按钮，进入下载页面。

* 我们可看到VirtualBox的最新版各平台的软件包下载链接，通过点击相应操作平台链接来下载相应版本的VirtualBox进行安装；共有如下4种平台版本：
	1. Windows hosts		(Microsoft Windows主机版本)
	2. OS X hosts			(苹果OS X主机版本)
	3. Linux distributions	(Linux各发行版主机的版本，将打开Linux发行版的专属下载页面)
	4. Solaris hosts		(Solaris主机版本)

![图2：firefox浏览器下载VirtualBox](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/2.downloadvbox.png)

## 用户手册(User Manual)
* [用户手册PDF](https://download.virtualbox.org/virtualbox/5.2.12/UserManual.pdf "VirtualBox用户手册PDF版")

* [用户手册HTML](https://www.virtualbox.org/manual "VirtualBox用户手册HTML版")

## 安装
在本指南中我们只讲解Windows系统下安装VirtualBox，其安装十分的简单，只需Next(下一步)就好。

### 执行安装
> 安装环境：Windows 10，VirtualBox版本：5.2.12，找到下载的VirtualBox(以下均简称为VBox)双击其图标进行安装，如下图所示：

![1. 双击VBox图标执行安装](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/3.vboxsetup.png)

### 欢迎界面
> 双击后，进入VBox安装的欢迎界面，直接“下一步”：

![2. VBox安装的欢迎界面](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/4.vboxwelcome.png)

### 自定义
> 自定义安装功能和安装路径设置：

![3. 设置VBox安装的功能及路径](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/5.vboxdefpath.png)

### 自定义
> 启动方式及文件关联设置：

![4. 设置VBox的启动方式及文件关联](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/6.vboxdefoption.png)

### 网络功能安装警告：

![5. VBox网络功能安装警告](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/7.vboxwarning.png)

### 确认安装

![6. VBox安装前确认](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/8.vboxready.png)

### 正在安装

![7. VBox正在安装中……](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/9.vboxinstalling.png)

### 完成安装

![8. VBox的安装过程完成](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/10.vboxcomplete.png)

### 首次启动VBox

![9. 首次启动VBox的界面](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/11.vboxstart.png)

## 使用
至此VBox的安装就完成了，下面来看下如何在VBox中新建一个Windows 10的虚拟机。

### 新建虚拟机
> 1. 在VBox管理器上点击“新建”，弹出“新建虚拟电脑”对话框
> 2. 名称唯一，我们这里是win10

![1. 新建虚拟电脑对话框](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/12.vboxnew.png)

### 虚拟机内存设置
> 虚拟机的内存如无特殊需求时，建议大小即可

![2. 虚拟机内存设置](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/13.vboxmemory.png)

### 虚拟机硬盘设置

![3. 虚拟机硬盘设置](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/14.vboxhhd.png)

### 虚拟机虚拟硬盘文件类型

![4. 虚拟机虚拟硬盘文件类型](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/15.vboxvdi.png)

### 虚拟硬盘分配形式

![5. 虚拟硬盘分配形式](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/16.vboxdynamic.png)

### 虚拟硬盘信息

![6. 虚拟硬盘信息](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/17.vboxhhdinfo.png)

### Win10虚拟机创建完成

![7. Win10虚拟机创建完成](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/18.vboxwin10.png)

### 右键菜单功能

![8. 虚拟机列表右键菜单](http://wintutorial-1254400168.cossh.myqcloud.com/install/vbox/19.vboxoptions.png)
