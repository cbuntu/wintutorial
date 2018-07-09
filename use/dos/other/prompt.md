# 其他类操作命令

## prompt命令说明及实例

### prompt说明
1. 功能：更改 CMD.EXE 命令提示符
2. 格式：prompt [text]
3. 环境变量：PROMPT
4. 使用说明：
	* text 指定新的命令指示符
	* 提示符可以由普通字符及下列特定代码组成：

代码 |字符                       |代码 |字符         
:---:|:-------------------------:|:---:|:---------------------------:
$A   |& (短 and 符号)            |$N   |当前驱动器
$B   |&#124; (管道)              |$P   |当前驱动器及路径 
$C   |( (左括弧)                 |$Q   |= (等号)
$D   |当前日期                   |$S   |  (空格)
$E   |Escape code (ASCLL 码 27)  |$T   |当前时间
$F   |) (右括弧)                 |$V   |Windows 版本号
$G   |> (大于符号)               |$\_  |换行
$H   |Backspace (擦除前一个字符) |$$   |$ (货币符号)
$L   |< (小于符号)               

### prompt实例
```
**[terminal]
**[path D:\]**[delimiter > ]**[command prompt $P $$ ]
**[path D:\]**[delimiter  $ ]**[command prompt $P$G ]
**[path D:\]**[delimiter > ]
```
