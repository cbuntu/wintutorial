# 目录类操作命令

## dir命令说明及实例

### dir说明
1. 功能：显示磁盘目录的内容
2. 类型：内部命令
3. 格式：dir [盘符:][路径][文件名][/A[[:]属性]][/C][/D][/L][/N][/O[[:]分类属性]][/P][/Q][/S][/T[[:]时间]][/W][/X][/4]
4. 使用说明：
	* /A显示具有指定属性的文件:D 目录 R 只读文件 H 隐藏文件 A 准备存档的文件 S 系统文件
	* /B 使用空格式（没有标题信息或摘要）
	* /C 在文件大小中显示千位数分隔符。这是默认值。用/-C来停用分隔符显示
	* /D 跟宽式相同，但文件是按栏分类列出的
	* /L 用小写
	* /N 新的长列表格式，其中文件名在最右边
	* /O 用分类顺序列出文件
	分类排序：
		N 按名称（字母顺序） S 按大小（从小到大） E 按扩展名（字母顺序） D 按日期/时间（从先到后）G 组目录优先-颠倒顺序的前缀
	* /P 在每个信息屏幕后暂停
	* /Q 显示文件所有者
	* /T 控制显示或用来分类的时间字符域:C 创建时间 A 上次访问时间 W 上次写入时间
	* /W 用宽列表格式
	* /X 显示为短文件名
	* /4 用四位数字显示年

### dir实例

```
**[terminal]
C:\> dir
Directory of C:\
.                       <DIR>           06-19-2018	9:21p
..                      <DIR>           06-19-2018	9:21p
TEST                    <DIR>           06-19-2018	10:29p
TEXT            TXT     13              06-19-2018	10:59p
			1 file(s)			13 bytes
			3 dir(s)		493,477,888 bytes free
```

```
**[terminal]
C:\> dir /L
Directory of C:\
.                       <DIR>           06-19-2018	9:21p
..                      <DIR>           06-19-2018	9:21p
test                    <DIR>           06-19-2018	10:29p
text            txt     13              06-19-2018	10:59p
			1 file(s)			13 bytes
			3 dir(s)		493,477,888 bytes free
```

```
**[terminal]
C:\> dir /A:D
Directory of C:\
.                       <DIR>           06-19-2018	9:21p
..                      <DIR>           06-19-2018	9:21p
TEST                    <DIR>           06-19-2018	10:29p
			1 file(s)			13 bytes
			3 dir(s)		493,477,888 bytes free
```

```
**[terminal]
C:\> dir text.txt
Directory of C:\
TEXT            TXT     13              06-19-2018	10:59p
			1 file(s)			13 bytes
			3 dir(s)		493,477,888 bytes free
```

```
**[terminal]
C:\> dir /B
TEST
TEXT.TXT

C:\> dir /L /B
test
text.txt
```

```
**[terminal]
C:\> dir /L /B /W
[test]		text.txt
```

```
**[terminal]
C:\> set DIRCMD=/l/w/b
C:\> dir
[test]		text.txt

C:\> set DIRCMD
/l/w/b

C:\> set DIRCMD=
```
