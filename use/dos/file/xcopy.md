# 文件类操作命令

## xcopy命令说明及实例

### xcopy说明
1. 功能：复制目录树及各目录下的文件
2. 类型：外部命令
3. 格式：xcopy source [target] [/P] [/S] [/E] [/W] [/Q] [/F]
4. 使用说明：
	* source [源盘符:][源路径][源文件]
		* 三者必需至少有一
		* 止于源文件，只复制文件
		* 止于路径，复制路径目录下的文件及子目录
	* target [目标盘符:][目标路径][目标文件]
		* 三者全部可选，
		* 止于目标文件，会将源文件改写为目标文件，即使多个源文件也只会改写成一个目标文件
		* 止于目标路径，会将源的目录及文件复制到目标路径中
	* /P 创建每个目标文件前提示
	* /S 复制目录和子目录，除了空的
	* /E 复制目录和子目录，包括空的
	* /W 提示您在复制前按键
	* /Q 复制时不显示文件名
	* /F 复制时显示完成的源和目标文件名

### xcopy实例

```
**[terminal]
# 不带参数，无目标路径
D:\> tree /f
D:.
|__code
   |   file1.txt
   |___test1
   |       file2.txt
   |___test2

# 情形1：目标路径或文件不指定，以当前目录为目标路径
D:\> xcopy code
D:\> tree /f
D:.
|   file1.txt
|___code
     |  file1.txt
	 |___test1
	 |       file2.txt
	 |___test2
D:\>

# 情形2.1：目标路径或文件指定，但目标路径或文件不存在
D:\> xcopy code cmd
目标 cmd 是文件名 还是 目录名
(F = 文件名，D = 目录)?F
code\file1.txt
复制了 1 个文件
D:\> tree /f
D:.
|  cmd # ----------------------- 和file1.txt的复制文件，重命名为cmd
|__code
   |   file1.txt
   |___test1
   |       file2.txt
   |___test2
D:\>

# 情形2.2：目标路径或文件指定，但目标路径或文件不存在
D:\> xcopy code cmd
目标 cmd 是文件名 还是 目录名
(F = 文件名，D = 目录)?D
code\file1.txt
复制了 1 个文件
D:\> tree /f
D:.
|__cmd
|     file1.txt
|__code
    | file1.txt
	|__test1
	|      file2.txt
	|__test2
D:\>
```

```
**[terminal]
# 不带参数，有目标路径
D:\> tree /f
D:.
|__cmd
|__code
   |  file1.txt
   |__test1
   |      file2.txt
   |__test2
D:\> xcopy code cmd
code\file1.txt
复制了 1 个文件
D:\> tree /f
D:.
|__cmd
|    file1.txt
|__code
    | file1.txt
	|__test1
	|      file2.txt
	|__test2
D:\>
```

```
**[terminal]
# 有目标路径，/P创建每个文件前提示确认
D:\> tree /f
D:.
|__cmd
|__code
   |  file1.txt
   |__test1
   |      file2.txt
   |__test2
D:\> xcopy code cmd /P
code\file1.txt (Y/N)? Y
复制了 1 个文件
D:\> tree /f
D:.
|__cmd
|    file1.txt
|__code
    | file1.txt
	|__test1
	|      file2.txt
	|__test2
D:\>
```

```
**[terminal]
# 有目标路径，/S复制目录和子目录，除了空的
D:\> tree /f
D:.
|__cmd
|__code
   |  file1.txt
   |__test1
   |      file2.txt
   |__test2
D:\> xcopy code cmd /S
code\file1.txt
code\test1\file2.txt
复制了 2 个文件
D:\> tree /f
D:.
|__cmd
|   |  file1.txt
|   |__test1
|          file2.txt
|__code
    | file1.txt
	|__test1
	|      file2.txt
	|__test2
D:\>
```

```
**[terminal]
# 有目标路径，/E复制目录和子目录，包括空的
D:\> tree /f
D:.
|__cmd
|__code
   |  file1.txt
   |__test1
   |      file2.txt
   |__test2
D:\> xcopy code cmd /E
code\file1.txt
code\test1\file2.txt
复制了 2 个文件
D:\> tree /f
D:.
|__cmd
|   |  file1.txt
|   |__test1
|   |      file2.txt
|   |__test2
|__code
    | file1.txt
	|__test1
	|      file2.txt
	|__test2
D:\>
```

```
**[terminal]
# 有目标路径，/W提示您在复制前按键
D:\> tree /f
D:.
|__cmd
|__code
   |  file1.txt
   |__test1
   |      file2.txt
   |__test2
D:\> xcopy code cmd /W
准备复制文件时，请按做任意键
code\file1.txt
复制了 1 个文件
D:\> tree /f
D:.
|__cmd
|     file1.txt
|__code
    | file1.txt
	|__test1
	|      file2.txt
	|__test2
D:\>
```

```
**[terminal]
# 有目标路径，/Q复制时不显示文件名
D:\> tree /f
D:.
|__cmd
|__code
   |  file1.txt
   |__test1
   |      file2.txt
   |__test2
D:\> xcopy code cmd /Q
复制了 1 个文件
D:\> tree /f
D:.
|__cmd
|      file1.txt
|__code
    |  file1.txt
	|__test1
	|      file2.txt
	|__test2
D:\>
```

```
**[terminal]
# 有目标路径，/F复制时显示完成的源和目标文件名
D:\> tree /f
D:.
|__cmd
|__code
   |  file1.txt
   |__test1
   |      file2.txt
   |__test2
D:\> xcopy code cmd /F
D:\code\file1.txt -> D:\cmd\file1.txt
复制了 1 个文件
D:\> tree /f
D:.
|__cmd
|      file1.txt
|__code
    |  file1.txt
	|__test1
	|      file2.txt
	|__test2
D:\>
```
