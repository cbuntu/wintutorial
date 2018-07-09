# 文件类操作命令

## fc命令说明与实例

### fc说明
1. 功能：比较两个文件或两个文件集并显示它们之间的不同
2. 类型：外部命令
3. 格式：fc [drive1:][path1]filename1 [drive2:][path2]filename2 [/B][/C][/L][/N]
4. 使用说明：
	* /B 执行二进制比较
	* /C 比较时不区分大小写
	* /L 将文件作为ASCLL文字比较
	* /N 在ASCLL比较上显示行数

### fc实例
```
**[terminal]
D:\cmd> dir
file1.txt        file2.txt
D:\cmd> type file1.txt file2.txt
file1.txt
file1
file2.txt
file2
D:\cmd>fc file1.txt file2.txt
正在比较文件 file1.txt 和 file2.txt
****** file1.txt
file1
****** file2.txt
file2
******
D:\cmd> echo file1 > file2.txt
D:\cmd> fc file1.txt file2.txt
正在比较文件 file1.txt 和 file2.txt
FC: 找不到相异处
D:\cmd>
```

```
**[terminal]
D:\cmd> echo FIle1 > file1.txt
D:\cmd> fc file1.txt file2.txt
正在比较文件 file1.txt 和 file2.txt
****** file1.txt
FIle1
****** file2.txt
file1
******
D:\cmd> fc file1.txt file2.txt /C
正在比较文件 file1.txt 和 file2.txt
FC: 找不到相异处
D:\cmd>
```
