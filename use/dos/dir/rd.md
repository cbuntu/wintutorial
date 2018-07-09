# 目录类操作命令

## rd命令说明及实例

### rd说明
1. 功能：从指定磁盘删除目录
2. 类型：内部命令
3. 格式：rd [盘符:][路径][子目录名] [/S] [/Q]
4. 别名：rmdir
5. 使用说明：
	* 子目录：删除前必须是空的，如有内容，应先进入该子目录，用rd及del（删除文件的命令）删除目录和文件，然后回到上级目录，用rd命令再删除该子目录
	* 不能删除根目录和当前目录
	* /S 除目录本身外，还将删除指定目录下的所有子目录和文件，用于删除目录树
	* /Q 安静模式，配合/S使用，删除目录树时不要求确认

### rd实例

```
**[terminal]
# 1. 先删除目录中文件，“*”星号为通配符
C:\> del C:\cmd\code\*.*

# 2. 再删除子目录“code”
C:\> rd C:\cmd\code

# 3. 查看确认
C:\> dir C:\cmd
[.]     [..]
```

```
**[terminal]
# /S参数可直接删除目录及目录下文件，即能删除目录树
D:\> rd code /s
code，是否确认(Y/N)? y
D:\>
```

```
**[terminal]
# 无需确认，直接删除目录树
D:\> rd code /s /q
D:\>
```