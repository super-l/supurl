### linux一键脚本使用说明

从3.2版本后，本采集软件的linux版本就提供了配套的以下脚本:

    一键启动脚本(start.sh)
    一键停止脚本(stop.sh)
    一键导出脚本(export.sh)
  
### 一键启动脚本说明 
在使用start.sh之前，请自行修改好配置文件！根据服务器的硬件配置，与配置文件的说明文档，调整最佳参数的值。

可查看配置文件的参数说明文档：http://www.supurl.net/doc/desc/config.html

系统默认也提供了keyword.txt，里面内置了部分关键词方便测试。可执行修改。一行一个关键词!

注意：不管是配置文件，还是关键词文件，都应该用编辑器打开(建议Nptepad++ 或者 sublime text)，不要使用记事本，主要是为了避免文件编码问题！

运行脚本后：

1. 自动载入keyword.txt关键词信息到redis, 自动启动supurl-plus采集软件(后台模式)；

2. 如果想要supurl-plus改成前台运行模式，可修改start.sh的内容：

```
把 
./supurl-plus start -d -l 

改为 
./supurl-plus start -l
```
`

### 一键导出脚本说明 

```
相当于输入命令：./supurl-plus export
```
