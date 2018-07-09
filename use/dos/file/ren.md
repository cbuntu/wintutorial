# 文件类操作命令

## ren命令说明及实例

### ren说明
1. 功能：重命名文件
2. 类型：内部命令
3. 格式：ren [drive:][path]oldfilename newfilename
4. 别名：rename
5. 使用说明：
	* newfilename前不可加盘符和路径，只能修改同一盘上的文件名
	* 允许使用通配符修改一组文件名或扩展名，通配符代表的字符与相同位置的字符相同

### ren实例
```
**[terminal]
D:\> dir cmd
file1.c        file2.c
D:\> ren file1.c demo.txt
D:\> dir cmd
demo.txt        file2.c
D:\>
```

```
**[terminal]
D:\> dir cmd
file1.c        file2.c
D:\> ren *.c d*.c
D:\> dir cmd
dile1.c        dile2.c
D:\>ren *.c ?emo?.c
D:\> dir cmd
demo1.c        demo2.c
D:\>
```

```
**[terminal]
D:\> dir cmd
file1.c        file2.c
D:\> ren *.c *.txt
D:\> dir cmd
file1.txt        file2.txt
D:\>
```
