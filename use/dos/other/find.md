# 其他类操作命令

## find命令说明及实例

### find说明
1. 功能：在文件中搜索字符串
2. 格式：find [drive:][path]filename "string" [/V] [/C] [/N] [/I]
3. 使用说明：
	* [drive:][path]filename 指定要搜索的文件
	* "string" 指定要搜索的文字串
	* /V 显示所有未包含指定字符串的行
	* /C 仅显示包含字符串的行数
	* /N 显示行号
	* /I 搜索字符串时忽略大小写

### find实例
```
**[terminal]
D:\> type 1.txt
> 1. the first line of 1.txt.

> 2. the second Line of 1.txt.
> 3. the third line of 1.txt.

> 4. the four Line of 1.txt.
D:\> find 1.txt "second"
---------- 1.txt
> 2. the second Line of 1.txt.
D:\>
```

```
**[terminal]
D:\> find 1.txt "second" /n
---------- 1.txt
[3]> 2. the second Line of 1.txt.
D:\>
```

```
**[terminal]
D:\> find 1.txt "second" /v /n
---------- 1.txt
[1]> 1. the first line of 1.txt.
[2]
[4]> 3. the third line of 1.txt.
[5]
[6]> 4. the four Line of 1.txt.
D:\>
```

```
**[terminal]
D:\> find 1.txt "line" /c
---------- 1.txt: 2
D:\>
```

```
**[terminal]
D:\> find 1.txt "line" /i
> 1. the first line of 1.txt.
> 2. the second Line of 1.txt.
> 3. the third line of 1.txt.
> 4. the four Line of 1.txt.
D:\>
```
