# 其他类操作命令

## cmd命令说明及实例

### cmd说明
1. 功能：启动 Windows 命令解释程序一个新的实例
2. 格式：cmd [/C | /K] string
3. 使用说明：
	* /C        执行字符串指定的命令然后中断
	* /K        执行字符串指定的命令但保留
	* string    指定的字符串

### cmd实例
```
**[terminal]
# 标题栏：C:\WINDOWS\system32\cmd.exe
D:\>cmd

# 按ENTER后cmd窗口变为如下样式：
# 标题栏：C:\WINDOWS\system32\cmd.exe - cmd
D:\> cmd
Microsoft Windows XP [版本 5.1.2600]
<C> 版权所有 1985-2001 Microsoft Corp.

D:\>
```

```
**[terminal]
#标题栏不变 标题栏：C:\WINDOWS\system32\cmd.exe
D:\> cmd /c dir
1.txt        2.txt        code

D:\>
```

```
**[terminal]
#标题栏由 标题栏：C:\WINDOWS\system32\cmd.exe
#变为：标题栏：C:\WINDOWS\system32\cmd.exe - cmd /k dir
D:\> cmd /c dir
1.txt        2.txt        code

D:\>
```
