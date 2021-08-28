### 如何设置与开启采集HTTP代理池

如果开启了HTTP代理池，则每次请求搜索引擎，都会从proxy.txt中随机收取HTTP代理并运用。


注意：在软件运行过程中，也可以修改proxy.txt中的代理列表，新增，修改、删除都可以！实时生效！

```

1: 在config/config.ini中开启代理池

[core]
# 是否开启proxy代理功能(随机)，config/proxy.txt文件中按行存取HTTP代理信息.目前仅对http模式有效
allowed_multiple_proxy = true


2: 在config/proxy.txt中，按行录入http代理信息,如：

http://100.149.174.100:58080
http://100.149.156.100:58080
```

