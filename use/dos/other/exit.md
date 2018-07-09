# 其他类操作命令

## exit命令说明及实例

### exit说明
1. 功能：退出 CMD.EXE 程序(命令解释程序)或当前批处理脚本
2. 格式：exit [/B] [exitCOde]
3. 使用说明：
	* /B 指定要退出当前批处理脚本而不是 CMD.EXE ，如果从一个批处理脚本外执行，则会退出 CMD.EXE
	* exitCode 指定一个数字号码，如果指定了 /B，将 ERRORLEVEL设成那个数字。如果退出 CMD.EXE ，则用那个数字设置过程退出代码

### exit实例
```
**[terminal]
**[path D:\]**[delimiter > ]**[command exit]
# 按 ENTER 后 CMD.EXE 程序退出，程序关闭
```
