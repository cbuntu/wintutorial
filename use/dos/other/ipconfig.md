# 其他类操作命令

## ipconfig命令说明及实例

### ipconfig说明
1. 功能：查看或设置网络
2. 格式：ipconfig [/? | /all | /renew]
3. 使用说明：
	* /? 显示这条帮助信息
	* /all 显示所有配置信息
	* /renew 重新配置IP地址

### ipconfig实例
```
**[terminal]
D:\> ipconfig

Windows IP Configuration

Ethernet adapter 本地连接：

		Connection-specific DNS Suffix  . :
		IP Address. . . . . . . . . . . . : 192.168.2.111
		Subnet Mask . . . . . . . . . . . : 255.255.255.0
		Default Gateway . . . . . . . . . : 192.168.2.1

D:\>
```

```
**[terminal]
D:\> ipconfig /?
USAGE:
	ipconfig [/? | /all | /renew [adapter] | /release [adapter] | /flushdns |
	/displaydns | /registerdns | /showclassid adapter | /setclassid adapter [classid] ]

	where
		adapter         Connection name
						(wildcard characters * and ? allowed, see examples)

		Options:
		   /?           Display this help message
		   /all         Display full configuration information.
		   /release     Release the IP address for the specified adapter.
		   /renew       Renew the IP address for the specified adapter.
		   /flushdns    Purges the DNS Resolver cache.
		   /registerdns Refreshes all DHCP leases and re-registers DNS names
		   /displaydns  Display the contents of the DNS Resolver Cache.
		   /showclassid Displays all the dhcp class IDs allowed for adapter.
		   /setclassid  Modifies the dhcp class id.

	The default is to display only the IP address, subnet mask and
	default gateway for each adapter bound to TCP/IP.

	For Release and Renew, if no adapter name is specified, then the IP address
	leases for all adapters bound to TCP/IP will be released or renewed.

	For Setclassid, if no ClassId is specified, then the ClassId is removed.

	Examples:
		> ipconfig                   ... Show information.
		> ipconfig /all              ... Show detailed information
		> ipconfig /renew            ... renew all adapters
		> ipconfig /renew EL*        ... renew any connection that has its
										 name starting with EL
		> ipconfig /release *Con*    ... release all matching connections,
		                                 eg. "Local Area Connection 1" or
		                                     "Local Area Connection 2"

D:\>
```

```
**[terminal]
D:\> ipconfig /all

Windows IP Configuration

	Host Name . . . . . . . . . . . . : win-d8321f65fe6
	Primary Dns Suffix  . . . . . . . :
	Node Type . . . . . . . . . . . . : Unknown
	IP Routing Enabled. . . . . . . . : No
	WINS Proxy Enabled. . . . . . . . : No

Ethernet adapter 本地连接：
	
	Connection-specific DNS Suffix. . :
	Description . . . . . . . . . . . : Intel(R) PRO/1000 T Server Adapter
	Physical Address. . . . . . . . . : 08-21-E5-AD-22-32
	Dhcp Enabled. . . . . . . . . . . : Yes
	Autoconfiguration Enabled . . . . : Yes
	IP Address. . . . . . . . . . . . : 192.168.2.111
	Subnet Mask . . . . . . . . . . . : 255.255.255.0
	Default Gateway . . . . . . . . . : 192.168.2.1
	DHCP Server . . . . . . . . . . . : 192.168.2.1
	DNS Servers . . . . . . . . . . . : 211.128.12.168
	                                    211.128.168.168
	Lease Obtained. . . . . . . . . . : 2018年6月39日 12:20:35
	Lease Expires . . . . . . . . . . : 2018年6月30日 14:20:35

D:\>
```

```
**[terminal]
D:\> ipconfig /renew

Windows IP Configuration

Ethernet adapter 本地连接

	Connection-specific DNS Suffix. . :
	IP Address. . . . . . . . . . . . : 192.168.2.111
	Subnet Mask . . . . . . . . . . . : 255.255.255.0
	Default Gateway . . . . . . . . . : 192.168.2.1

D:\>
```
