# 文件类操作命令

## type命令说明及实例

### type说明
1. 功能：显示文本文件内容
2. 类型：内部命令
3. 格式：type [drive:][path]filename
4. 使用说明：
	* 文件扩展名必须加上
	* 可使用通配符，可一次显示多个文件
	* 文件内容多时，一屏显示不下，可加 more 通道命令让其一屏一屏显示

### type实例

```
**[terminal]
D:\> tree /f
D:.
  file1.txt
  file2.txt
D:\> type file1.txt
file1 content
```

```
**[terminal]
# 显示所列出的文本文件
D:\> tree /f
D:.
  file1.txt
  file2.txt
D:\> type file1.txt file2.txt
file1.txt

file1 content

file2.txt

file2 content
```

```
**[terminal]
# 使用通配符显示一个或多个文本文件
D:\> tree /f
D:.
  file1.txt
  file2.txt
D:\> type *.txt    #或：type *
file1.txt

file1 content

file2.txt

file2 content
```
