# 其他类操作命令

## edit命令说明及实例

### edit说明
1. 功能：DOS模式下的编辑器
2. 格式：edit [filename]
3. 使用说明：
	* filename 指定编辑的文件名

### edit实例
```
**[terminal]
**[path D:\]**[delimiter > ]**[command edit]
```
![无参数edit命令](http://wintutorial-1254400168.cossh.myqcloud.com/use/msdos/11.png)

```
**[terminal]
**[path D:\]**[delimiter > ]**[command edit demo.txt]
```
![带文件名参数edit命令](http://wintutorial-1254400168.cossh.myqcloud.com/use/msdos/12.png)

### edit编辑器使用方法
* 光标移动命令

命令            |命令含义                          
:--------------:|:--------------------------------:
Home            |移动光标到当前行行首
End             |移动光标到当前行行尾
Ctrl + Up       |向上滚动一行
Ctrl + DOwn     |向下滚动一行
PageUp          |向上滚动一屏
PageDown        |向下滚动一屏
Ctrl + PgUp     |向左滚动一屏
Ctrl + PgDn     |向右滚动一屏
Ctrl + Home     |滚动到文档开头处
Ctrl + End      |滚动到文档结尾处
Ctrl + Left     |向左移动一个词
Ctrl + Right    |向右移动一个词

* 编辑命令

命令            |命令含义
:--------------:|:--------------------------------:
Enter           |开始新的一行
Delete          |删除光标所在处的字符
Backspace       |删除光标所在处左边的字符
Tab             |移动光标到下一个Tab制表符处
Insert          |插入模式与覆盖模式转换开关
Ctrl + Y        |删除当前行
Ctrl + V        |将剪切板内容粘贴进文件中
Ctrl + P        |允许特殊字符插入

* 选择命令

命令            |命令含义
:--------------:|:--------------------------------:
Shift           |按住Shift键，可将光标移动过的区域设置为选择区域
Ctrl + C        |复制当前选择区域至缓冲区域
Ctrl + X        |剪切当前所选区域至缓冲区域
Delete          |删除当前所选区域内容
Tab             |缩进所选择的行
Shift + Tab     |反缩进所选择的行

* 查找替换文本命令

命令            |命令含义
:--------------:|:--------------------------------:
Ctrl + Q + F    |查找文本
Ctrl + Q + A    |查找并替换文本
F3              |重复上次的查找

* 窗口管理命令

命令            |命令含义
:--------------:|:--------------------------------:
F6              |切换至下一个编辑窗口
F8              |切换到您工作中的下个文件
Ctrl + F6       |打开第2个编辑窗口
Ctrl + F4       |关闭第2个编辑窗口
Ctrl + F8       |重置窗口大小

* 其他命令

命令            |命令含义
:--------------:|:--------------------------------:
F1              |显示上下文帮助
