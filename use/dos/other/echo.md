# 其他类操作命令

## echo命令说明及实例

### echo说明
1. 功能：显示信息，或将命令回显打开或关上。
2. 格式：echo [ON | OFF]
         echo [message]
3. 使用说明：
	* ON 打开命令回显
	* OFF 关上命令回显
	* message 要输出显示的信息
	* 不带参数的 echo ,显示当前回显设置

### echo实例
```
**[terminal]
D:\> echo
ECHO 处于打开状态

D:\>
```

```
**[terminal]
# bat中不显示命令行执行过程，只显示执行结果
D:\> echo off
echo
ECHO 处于关闭状态
echo on

D:\> echo
ECHO 处于打开状态

D:\>
```

```
**[terminal]
D:\> echo Windows Tutorial
Windows Tutorial

D:\>
```
