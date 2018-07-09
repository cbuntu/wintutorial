# 其他类操作命令

## subst命令说明及实例

### subst说明
1. 功能：将路径与驱动器号关联
2. 格式：subst [drive1: [drive2:]path]
         subst drive1: /D
3. 使用说明：
	* drive1: 指定要指派路径的虚拟驱动器
	* [drive2:]path 指定物理驱动器和要指派给虚拟驱动器的路径
	* /D 删除被替换的(虚拟)驱动器
	* 无参数 subst 显示当前虚拟驱动器的清单

### subst实例
```
**[terminal]
# 说明：物理驱动器仅有C:、D:两个
D:\> dir
code
D:\> subst E: D:\code
D:\> E:
E:\> subst
E:\> E:\: => D:\code

E:\>
```

```
**[terminal]
D:\> subst E: /d
D:\> E:
系统找不到指定的驱动器

D:\>
```
