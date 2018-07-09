# 其他类操作命令

## help命令说明及实例

### help说明
1. 功能：提供命令的帮助信息
2. 格式：help [command]
3. 使用说明：
	* 无 command参数，提供命令列表
	* command-显示该命令的帮助信息

### help实例
```
**[terminal]
# help命令后加more命令可逐屏显示
D:\> help | more
有关某个命令的详细信息，请键入 HELP 命令名
ASSOC     显示或修改文件扩展名关联。
AT        计划在计算机上运行的命令和程序。
ATTRIB    显示或更改文件属性。
BREAK     设置或清除扩展式 CTRL + C 检查。
CACLS     显示或修改文件的访问控制列表(ACLs)。
CALL      从另一个批处理程序调用这一个。
CD        显示当前目录的名称或将其更改。
CHCP      显示或设置活动代码页数。
CHDIR     显示当前目录的名称或将其更改。
CHKDSK    检查磁盘并显示状态报告。
CHKNTFS   显示或修改启动时间磁盘检查。
CLS       清除屏幕。
CMD       打开另一个 Windows 命令解释程序窗口。
COLOR     设置默认控制台前景和背景颜色。
COMP      比较两个或两套文件的内容。
COMPACT   显示或更改 NTFS 分区上文件的压缩。
CONVERT   将 FAT 卷转换成 NTFS。您不能转换当前驱动器。
COPY      将至少一个文件复制到另一个位置。
DATE      显示或设置日期。
-- More  --
```

```
**[terminal]
D:\> help date
显示或设置日期

DATE [/T | date]

显示当前日期设置和输入新日期的提示，请键入
不带参数的 DATE。要保留现有日期，请按ENTER。

如果命令扩展名被启用，DATE 命令会支持 /T 开关；
该开关指示命令只输出当前日期，但不提示输出新日期。

D:\>
```
