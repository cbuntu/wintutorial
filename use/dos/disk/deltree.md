# 磁盘类操作命令

## deltree命令说明及实例

### deltree说明
1. 功能：将整个目录及其下属子目录和文件删除
2. 类型：外部命令
3. 格式：deltree [盘符:]<路径名>
4. 使用说明：
	* 该命令可以一步就将目录及其下的所有文件、子目录、更下层的子目录一并删除，而且不管文件的属性为隐藏、系统或只读，只要该文件位于删除的目录之下，DELTREE都一视同仁，照删不误。使用时务必小心！！！

### deltree实例

```
**[terminal]
# 显示目录树cmd及其下属文件
C:\> tree cmd /F
C:.
|____code
         file1.txt
```

```
**[terminal]
# 删除目录树cmd
C:\> deltree cmd
	[default-build v1.02g] of deltree, The "root-safety-check" is enabled.

delete directory "C:\cmd"
and all its subdirectories?

[Y]  [N]  [Q]，[ENTER] ? Y
==> deleting "C:\cmd" ...
C:\
```
