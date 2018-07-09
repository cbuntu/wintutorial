# 其他类操作命令

## set命令说明及实例

### set说明
1. 功能：显示、设置或删除 CMD.EXE 环境变量
2. 格式：set [variable=[string]]
3. 使用说明：
	* variable 指定环境变量名
	* string 指定要指派给变量的一系列字符串
	* 无参数set，显示当前所有环境变量
	* set p 将显示首字母为p的环境变量

### set实例
```
**[terminal]
D:\> set
ALLUSERSPROFILE=C:\DOcuments and Settings\All Users
APPDATA=C:\Documents and Settings\win\Application Data
CLIENTNAME=Console
CommonProgramFiles=C:\Program Files\Common Files
COMPUTERNAME=Win-host
ComSpec=C:\WINDOWS\system32\cmd.exe
DIRCMD=/l /w /b
FP_NO_HOST_CHECK=NO
HOMEDRIVE=C:
HOMEPATH=\DOcuments and Settings\win
LOGONSERVER=\\Win-host
NUMBER_OF_PROCESSONRS=1
OS=Windows_NT
Path=C:\WINDOWS\system32;C:\WINDOWS;C:\WINDOWS\System32\Wbem
PATHEXT=.COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH
PROCESSOR_ARCHITECTURE=x86
PROCESSOR_IDENTIFIER=x86 Family 6 Model 42 Stepping 7, GenuineIntel
PROCESSOR_LEVEL=6
PROCESSOR_REVISION=2a07
ProgramFiles=C:\Program Files
PROMPT=$P$G
SESSIONNAME=Console
SystemDrive=C:
SystemRoot=C:\WINDOWS
TEMP=C:\DOCUME~1\win\LOCALS~1\Temp
TMP=C:\DOCUME~1\win\LOCALS~1\Temp
USERDOMAIN=Win-host
USERNAME=win
USERPROFILE=C:\Documents and Settings\win
windir=C:\WINDOWS

D:\>
```

```
**[terminal]
D:\> set d
DIRCMD=/l /w /b
```

```
**[terminal]
D:\> set prompt=$P$Q
D:\= prompt $P$G
D:\>
```
