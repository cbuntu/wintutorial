# 文件类操作命令

## move命令说明及实例

### move说明
1. 功能：移动文件并重命名文件和目录
2. 类型：内部命令
3. 格式：
	* 要移动一个文件：
		+ move [/Y | /-Y] [drive:][path]filename1 destination
	* 要重命名一个目录
		+ move [-Y | /-Y] [drive:][path]dirname1 [path][dirname2]
4. 使用说明：
	* [drive:][path]filename1 指定您想移动的文件位置和名称
	* destination 指定文件的新位置。目标可包含一个驱动器号和冒号、一个目录名或组合。如果只移动一个文件并在移动时将其重命名，您还可以包含文件名
	* [drive:][path]dirname1 指定要重命名的目录
	* dirname2 指定目录的新名称，指定path，不指定dirname2是将目录copy到其他位置
	* /Y 取消确认改写一个现有目标文件的提示
	* /-Y 对确认改写一个现有目标文件发出提示

### move实例

```
**[terminal]
# 移动文件到其他目录
D:\> dir
1.txt        cmd        code
D:\> move 1.txt cmd
D:\> tree /f
D:.
|__cmd
|     1.txt
|__code
D:\>

# 从其他目录移动文件到当前目录
D:\> move cmd\1.txt
# 或
D:\> move cmd\1.txt .\
D:\> tree /f
D:.
|  1.txt
|__cmd
|__code
D:\>
```

```
**[terminal]
D:\> tree /f
D:.
|  1.txt
|__cmd
|__code
D:\> move cmd code\name
D:\> tree /f
D:.
|  1.txt
|__code
    |__name
D:\>
```

```
**[terminal]
# dirname2为已存在的目录，此时会移动到code中，如code不存在，则会更名为code
D:\> tree /f
D:.
|  1.txt
|__cmd
|__code
D:\> move cmd code
D:\> tree /f
D:.
|  1.txt
|__code
    |__cmd
D:\>
```
