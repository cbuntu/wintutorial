# 文件类操作命令

## del命令说明及实例

### del说明
1. 功能：删除一个或数个文件
2. 类型：内部命令
3. 格式：del names [/P] [/F] [/S] [/Q] [/A:attributes]
4. 别名：erase
5. 使用说明：
	* names 指定一个或数个文件或目录列表。通配符可用来删除多个文件。如果指定一个目录，目录中的所有文件都会被删除
	* /P 删除每一个文件之前提示确认
	* /F 强制删除只读文件
	* /S 从所有子目录删除指定文件
	* /Q 安静模式，删除全局通配符时，不要求确认
	* /A 根据属性选择要删除的文件：
		R 只读文件      S 系统文件      H 隐藏文件      A 存档文件      \- 表示“否”的前缀

### del实例
```
**[terminal]
# 同时删除多个文件
D:\> tree /f
D:.
|   1.txt
|   2.txt
|__cmd
|     1.txt
|     2.txt
|__code
      1.txt
	  2.txt
D:\> del 1.txt 2.txt # or: del *.txt
D:\> tree /f
D:.
|__cmd
|     1.txt
|     2.txt
|__code
      1.txt
	  2.txt

# 同时删除多个目录下文件
D:\> del cmd code
D:\cmd\*，是否确认(Y/N)? y
D:\code\*，是否确认(Y/N)? y
D:\> tree /f
D:.
|__cmd
|__code
D:\>
```

```
**[terminal]
# 删除时提示确认
D:\> dir
1.txt        2.txt
D:\> del 1.txt /P
D:\1.txt，要删除(Y/N)吗？y
D:\> dir
2.txt
D:\>
```

```
**[terminal]
# 强制删除只读文件
D:\> dir
1.txt        2.txt
D:\> attrib
A        D:\1.txt
A        D:\2.txt
D:\> attrib 2.txt +r
D:\> attrib
A        D:\1.txt
A   R    D:\2.txt
D:\>del *
D:\*，是否确认(Y/N)? y
D:\2.txt
拒绝访问
D:\> dir
2.txt
D:\> del 2.txt /f
D:\>dir
D:\>
```

```
**[terminal]
# 从其所有子目录下删除指定的文件
D:\> tree /f
D:.
|   1.txt
|   2.txt
|__cmd
|     1.txt
|     2.txt
|__code
      1.txt
	  2.txt
D:\> del 1.txt /s
删除文件 - D:\1.txt
删除文件 - D:\cmd\1.txt
删除文件 - D:\code\1.txt
D:\> tree /f
D:.
|   2.txt
|__cmd
|     2.txt
|__code
	  2.txt
D:\>
```

```
**[terminal]
# 安静模式，删除时不要求确认
D:\> tree /f
D:.
|   2.txt
|__cmd
|     2.txt
|__code
	  2.txt
D:\> del 2.txt /q
D:\>del cmd\* /q
D:\> tree /f
D:.
|__cmd
|__code
       2.txt
D:\>
```

```
**[terminal]
# 删除指定属性的文件
D:\> attrib
A        D:\1.txt
A   R    D:\2.txt
D:\> del * /a:r
D:\*，是否确认(Y/N)? y
D:\> dir
1.txt
D:\>
```
