# 其他类操作命令

## start命令说明及实例

### start说明
1. 功能：启动另一窗口运行指定和程序或命令
2. 格式：start ["title"] [/path] [/MIN] [/MAX] [command/program]
3. 使用说明：
	* "title" 在窗口标题栏中显示的标题
	* /MIN 开始时窗口最小化
	* /MAX 开始时窗口最大化
	* command/program cmd命令或批处理文件，程序名称

### start实例
```
**[terminal]
# 默认大小打开notepad(记事本)
D:\> start notepad
```

```
**[terminal]
# 最小化打开notepad(记事本)
D:\> start /min notepad
```

```
**[terminal]
# 最大化打开notepad(记事本)
D:\> start /max notepad
```
