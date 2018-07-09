# 文件类操作命令

## attrib命令说明及实例

### attrib说明
1. 功能：显示或更改文件属性
2. 类型：外部命令
3. 格式：attrib [drive:][path][filename][+R][-R][+A][-A][+S][-S][+H][-H][/S[/D]]
4. 使用说明：
	* \+ 设置属性
	* \- 清除属性
	* R 只读文件属性
	* A 存档文件属性
	* S 系统文件属性
	* H 隐藏文件属性
	* /S 处理当前文件夹及其子文件夹中与filename相匹配的文件
	* /D /D要与/S配合使用，处理与filename相匹配的文件夹

### attrib实例

```
**[terminal]
# 查看文件属性
D:\code> tree /f
D:.
|  file1.txt
|__test1
|      file2.txt
|__test2

# 查看当前目录下所有文件属性，无filename时，默认指当前目录下的文件或子目录
D:\code> attrib
A        D:\code\file1.txt
D:\code>

# 查看目录属性
D:\code> attrib test1
A        D:\code\test1
D:\code>
```

```
**[terminal]
# 设置文件只读属性
D:\code> attrib +R
D:\code> attrib
A   R   D:\code\file1.txt
D:\code>

# 设置特定文件或目录的只读属性
D:\code> attrib file1.txt -R
D:\code> attrib file1.txt
A       D:\code\file1.txt
D:\code>
D:\code> attrib test2 +R
D:\code> attrib test2
R       D:\code\test2
D:\code>
```

```
**[terminal]
D:\code> attrib -A
D:\code> attrib
R        D:\code\file1.txt
D:\code> attrib file1.txt +A
D:\code> attrib file1.txt
A   R    D:\code\file1.txt
D:\code>
```

```
**[terminal]
D:\code> attrib +S
D:\code> attrib
R   S    D:\code\file1.txt
D:\code> attrib file1.txt -S
D:\code> attrib file1.txt
R        D:\code\file1.txt
D:\code>
```

```
**[terminal]
D:\code> attrib +H
D:\code> attrib
R   H    D:\code\file1.txt
D:\code> attrib file1.txt -H
D:\code> attrib file1.txt
R        D:\code\file1.txt
D:\code>
```

```
**[terminal]
D:\> tree /f
D:.
|__cmd
|  |   file1.txt
|  |   file2.txt
|  |___cmd
|         file1.txt
|__code
   |   file1.txt
   |__test1
   |   file2.txt
   |__test2

# D:\下所有文件隐藏，-h可取消隐藏
D:\>attrib +h /S
D:\> tree /f
D:.
|__cmd
|  |__cmd
|__code
   |__test1
   |__test2
D:\>
```

```
**[terminal]
# 与/S配合使用
D:\> attrib +h /S /D
D:/>tree /f
D:.
没有子目录及文件显示
D:\>
```
