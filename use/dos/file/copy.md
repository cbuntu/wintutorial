# 文件类操作命令

## copy命令说明及实例

### copy说明
1. 功能：将一份或多份文件复制到另一个位置
2. 类型：内部命令
3. 格式：copy [drive:][path]source[+source] [drive:][path][target]
4. 新建文件：copy > filename
5. 使用说明：
	* copy是文件对文件的方式复制数据，复制前目标盘必需已格式化
	* 复制过程中，目标盘上同名旧文件会被源文件取代
	* 文件名中允许使用通配符"\*"和"?"可同时复制多个文件
	* copy命令的源文件名必需指出，不可缺省
	* 复制时，目标文件名可以与源文件名相同，称作“同名拷贝”此时目标文件名可以省略
	* 复制时，目标文件名也可以与源文件名不相同，称作“异名拷贝”，此时，目标文件名不能省略
	* 复制时，还可以将几个文件合并为一个文件，称为“合并拷贝”
	* COPY命令的使用格式，源文件名与目标文件名之间必须有空格

### copy实例

```
**[terminal]
# 当前目录下复制文件
D:\> cd code
D:\code> dir
main.c
D:\code> copy main.c header.c
D:\code> dir
main.c        header.c
```

```
**[terminal]
# 跨路径复制文件
D:\> dir
code        cmd
D:\> dir code
main.c        header.c
D:\> dir cmd
D:\>copy code\main.c cmd
D:\> dir cmd
main.c
```

```
**[terminal]
# 跨盘复制文件
D:\> copy C:\code\history.c D:\cmd
D:\> dir cmd
main.c        history.c
```

```
**[terminal]
# 异名复制
D:\> copy cmd\history.c cmd\his.c
D:\> dir cmd
main.c        history.c        his.c
```

```
**[terminal]
# 多文件复制
D:\> cd cmd
D:\cmd> copy main.c + history.c + his.c file.c
D:\cmd> type file.c
#include <stdio.h>  # ----------------------------------------- < main.c >
int main() {
	printf("Hello World!\n");
	return 0;
}
#include <stdio.h>  # ----------------------------------------- < history.c >
int main() {
	printf("Hello World!\n");
	return 0;
}
#include <stdio.h>  # ----------------------------------------- < his.c >
int main() {
	printf("Hello World!\n");
	return 0;
}
```

```
**[terminal]
D:\> cd cmd
D:\cmd> dir
main.c        history.c        his.c        file.c
D:\cmd> copy *.c test.c
D:\cmd> type test.c
#include <stdio.h>  # ----------------------------------------- < main.c >
int main() {
	printf("Hello World!\n");
	return 0;
}
#include <stdio.h>  # ----------------------------------------- < history.c >
int main() {
	printf("Hello World!\n");
	return 0;
}
#include <stdio.h>  # ----------------------------------------- < his.c >
int main() {
	printf("Hello World!\n");
	return 0;
}
#include <stdio.h>  # ----------------------------------------- < file.c >
int main() {
	printf("Hello World!\n");
	return 0;
}
D:\cmd> dir
main.c        history.c        his.c        file.c      test.c
```
