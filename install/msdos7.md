# MS-DOS 7.1安装

## 概述
* 本章是关于MS-DOS 7.1的安装过程，后续的Windows 3.1、Windows 95/95/ME均是在此版本虚拟机上安装。

* 新建虚拟机的步骤仅文本来呈现，上一章节中有新建虚拟机的教程。

* MS-DOS 7.1[下载](https://winworldpc.com/product/ms-dos/7x)

## 新建MS-DOS 7.1虚拟机

> 1. 名称：msdos7.1，类型：other，版本：DOS
> 2. 内存大小：64MB
> 3. 现在创建虚拟硬盘
> 4. 选择默认值：VDI
> 5. 选择默认值：动态分配
> 6. 硬盘文件名：modos7.1，硬盘大小：800MB
> 7. 内存与硬盘大小的设定后续Windows 3.1/95/98/ME的安装需求而大于默认值

## 系统镜像文件加载
* MS-DOS 7.1的镜像文件有IMG版本及ISO版本，加载方法不同，IMG是通过软驱加载，ISO是通过光驱加载。

* 选中VBox管理器中虚拟机列表中的“msdos7.1”虚拟机，点击“设置”，打开设置对话框之“存储”标签。

### IMG软盘版镜像加载
> 1. 选择控制器：Floppy中的软盘图标
> 2. 点击右侧栏软盘图标，选择MS-DOS 7.1的Disk1的镜像文件：disk01.img

![1. 加载disk01.img](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/1.onloadimg1.png)

![2. 加载disk01.img](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/2.onloadimg2.png)

### 启动安装
> 点击VBox管理器上的启动

![3. MS-DOS安装欢迎界面](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/3.msdos71setup.png)

### 硬盘格式要求
> MS-DOS 7.1支持大硬盘FAT12/16/32格式，不支持NTFS/HPFS

![4. MS-DOS安装硬盘格式](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/4.msdos71setup2.png)

### MS-DOS7.1安装协议
> 安装协议：[GNU GPL](http://www.gnu.org/licenses/licenses.en.html)

![5. MS-DOS安装协议](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/5.msdosgpl.png)

### 设备分区检查

![6. 设备分区检查](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/6.checkpartitions.png)

### 创建分区

![7. 创建硬盘分区](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/7.createpartitions.png)

### 重新启动
> FAT分区创建完成，为完成安装，需重新启动电脑

![8. 重新启动电脑](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/8.reboot.png)

### 分区检查
> 重启后先进行前3步，再到分区检查，选择默认值skip跳过即可

![9. 二次分区检查](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/12.checkpartitions2.png)

### 重写MBR
> MBR(主引导记录)

![10. 重写MBR(主引导记录)](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/13.rewritembr.png)

### 安装路径
> 设置MS-DOS 7.1的安装路径，可使用默认值

![11. 设置MS-DOS 7.1的安装路径](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/14.installpath.png)

### 创建安装路径
> 刚分好区的设备没有路径，要先创建

![12. 创建安装路径](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/15.createpath.png)

### 安装类型
> 1. 完整安装
> 2. 仅DOS命令安装
> 3. 微DOS系统安装
> 4. Add-Ons插件

![13. 安装类型](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/16.fullinstall.png)

### 安装扩展AccessDos

![14. 安装扩展AccessDos](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/17.checkinstall.png)

### 安装信息确认

![15. 安装信息确认](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/18.toinstall.png)

### 需要第2张软盘

![16. 需要第2张软盘提示信息](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/19.disk2.png)

![17. VBox管理器加载第2张软盘](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/20.insertdisk2.png)

### 安装Add-Ons
> Add-ons插件不建议安装，在1.3.12安装类型时就可取消安装；img版本镜像中也不包含ADD-Ons，ISO版本镜像包含。

![18. 安装Add-Ons插件提示](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/21.addons.png)

### MS-DOS 7.1启动画面
![19. MS-DOS 7.1启动画面设置](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/22.doslogo.png)

### MS-DOS启动日志文件
![20. MS-DOS启动日志文件设置](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/23.startlog.png)

### 后面4项全部默认值即可
![21. Lock command](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/24.lock.png)

![22. UMB memory](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/25.umb.png)

![23. CD/DVD](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/26.loadboth.png)

![24. Configure](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/27.configure.png)

### 重启

![25. 重启](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/28.reboot2.png)

### MS-DOS 7.1启动画面

![26. MS-DOS 7.1启动画面](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/29.msdosstart.png)

### MS-DOS 7.1 命令行界面
![27. MS-DOS 7.1命令行界面](http://wintutorial-1254400168.cossh.myqcloud.com/install/msdos/30.commandline.png)
