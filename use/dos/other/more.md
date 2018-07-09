# 其他类操作命令

## more命令说明及实例

### more说明
1. 功能：逐屏显示输出
2. 格式：
	* more [drive:][path]filename [/E] [/C] [/P] [/S] [/Tn] [+n]
	* command -name | more [/E] [/C] [/P] [/S] [/Tn] [+n]
	* more [files] [/E] [/C] [/P] [/S] [/Tn] [+n]
3. 使用说明：
	* [drive:][path]filename 指定要逐屏显示的文件
	* command-name 指定要显示其输出的命令
	* /E 启用扩展功能
	* /C 显示页面前先清除屏幕
	* /P 扩展 FormFeed 字符
	* /S 将多个空白行缩成一行
	* /Tn 将跳格键扩展成 n 个空格(默认值为 8)

		命令行开关可以出现在 MORE 环境变量中。

	* +n 从第 n 行开始显示第一个文件
	* files 要显示的文件列表，用空格分开列表中的文件

	如果扩展功能已启用，在 -- More -- 提示处会接受下列命令：
		* P n     显示下 n 行
		* S n     略过下 n 行
		* F       显示下个文件
		* Q       退出
		* =       显示行号
		* ?       显示帮助行
		* <space> 显示下一页
		* <ret>   显示下一行

### more实例
```
**[terminal]
D:\> more demo.txt
this is the demo document.
1
 
 
4
 
6
 
8
9
-- More (95%) --
```

```
**[terminal]
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
D:\> more 1.txt 2.txt
1
-- More (100%) --

# 按ENTER出现如下内容
D:\> more 1.txt 2.txt
2
3

D:\>
```

```
**[terminal]
D:\> dir
1.txt        2.txt        code
D:\> more 1.txt /c

# 按ENTER屏幕变为如下内容
1
D:\>
```

```
**[terminal]
D:\> more demo.txt
this is the demo document.
1
 
4
 
6
 
8
9
10
-- More (95%) --
```

```
**[terminal]
D:\> more demo.txt +4
 
4
 
6
 
8
9
10
11
12
-- More (95%) --
```
