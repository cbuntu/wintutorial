# 其他类操作命令

## replace命令说明及实例

### replace说明
1. 功能：替换文件
2. 格式：replace [drive1:][path1]filename [drive2:][path2] [/A] [/P] [/R]
		 replace [drive1:][path1]filename [drive2:][path2] [/P] [/R] [/S] [/U]
3. 使用说明：
	* [drive1:][path1]filename 指定源文件
	* [drive2:][path2] 指定要替换文件的目录
	* /A 把新文件加入目标目录。不能和 /S 和 /U 命令行开关搭配使用
	* /P 替换文件或加入源文件之前会先提示您进行确认
	* /R 替换只读文件以及未受保护的文件
	* /S 替换目标目录中所有子目录的文件，不能与/A 命令选项搭配使用
	* /U 只会替换或更新比源文件创建日期早的文件，不能与/A 命令选项搭配使用

### replace实例

```
**[terminal]
# 替换指定目录中已存在的同名文件
D:\> tree /f
D:.
|  1.txt
|__code
      1.txt

# 将code\1.txt替换成D:\1.txt
D:\> replace 1.txt code
正在替换 D:\code\1.txt
替换了 1 文件
D:\>
```

```
**[terminal]
D:\> tree /f
D:.
|  1.txt
|__code

D:\> replace 1.txt code
未替换文件

D:\> replace 1.txt code /a
正在添加 D:\code\1.txt
添加了 1 文件

D:\>
```

```
**[terminal]
D:\> tree /f
D:.
|  1.txt
|__code
      1.txt
D:\> replace 1.txt code /p
是否替换 D:\code\1.txt? (Y/N) y
正在替换 D:\code\1.txt
替换了 1 文件

D:\> del code\1.txt
D:\> replace 1.txt code /a /p
是否添加 D:\code\1.txt? (Y/N) y
正在添加 D:\code\1.txt
添加了 1 文件

D:\>
```

```
**[terminal]
D:\> tree /f
D:.
|  1.txt
|__code
      1.txt
	
D:\> attrib code\1.txt
A            D:\code\1.txt

D:\> attrib code\1.txt +R
D:\> attrib code\1.txt
A     R      D:\code\1.txt

D:\> replace 1.txt code
拒绝访问 - D:\code\1.txt
未替换文件

D:\> replace 1.txt code /r
正在替换 D:\code\1.txt
替换了 1 文件

D:\> attrib code\1.txt
A            D:\code\1.txt

D:\>
```

```
**[terminal]
D:\> tree /f
D:.
|__code
    |__cmd

D:\> echo 0 > 1.txt
D:\> echo 1 > code\1.txt
D:\> echo 2 > code\cmd\1.txt
D:\> tree /f
D:.
|  1.txt
|__code
   |  1.txt
   |__cmd
        1.txt
	
D:\> type 1.txt code\1.txt code\cmd\1.txt

1.txt
0

code\1.txt
1

code\cmd\1.txt
2

D:\> replace 1.txt code /s
正在替换 D:\code\1.txt
正在替换 D:\code\cmd\1.txt
替换了2 文件

D:\> type 1.txt code\1.txt code\cmd\1.txt

1.txt
0

code\1.txt
0

code\cmd\1.txt
0

D:\>
```

```
**[terminal]
D:\> tree /f
D:.
|__code
   |__cmd

D:\> echo code > code\1.txt
D:\> echo d: > 1.txt
D:\> echo cmd > code\cmd\1.txt
D:\> tree /f
D:.
|  1.txt
|__code
   |  1.txt
   |__cmd
        1.txt

D:\> replace 1.txt code /s /u
正在替换 D:\code\1.txt
替换了 1 文件

D:\> type 1.txt code\1.txt code\cmd\1.txt

1.txt 
d:

code\1.txt
d:

code\cmd\1.txt
cmd

D:\>
```
