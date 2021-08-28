### 实时查看采集进度 | info

#### 一、通过软件自带命令查看
使用以下命令即可实时查看采集统计数据：

    ./supurl-plus info

#### 二、通过redis客户端查看

使用客户端软件，链接redis服务器。

注意，redis如果是安装在Linux服务器，那么图形界面的客户端一般是要按照在windows或者MAC上的。当然如果您会使用cli命令，那就可以直接在服务器上使用。

redis服务端是远程服务器，则在图形界面中填写以下信息并连接：

    IP[服务器ip]: 服务器IP
    PORT[端口]:   6371
    AUTH[密码]:   redis配置文件中设置的密码
    
注意：
    
    由于客户端与服务端不在同一台服务器，为了安全性，建议设置redis的密码，否则所有人都可以访问与操作！

    redis所属服务器还需要开放防火墙端口例外。需要配置redis开启远程访问功能。
    
    具体操作可以查看《Linux下redis的安装教程文档》。
    


链接后，选择配置文件中对应的数据库编号(默认为0)，查看键：

    supurl:finished:data         # 采集结果列表
    supurl:finished:keyword      # 已经采集完成的关键词列表
    
    supurl:running:keyword       # 采集中关键词
    
    supurl:seed:host             # 剩余的种子域名列表
    supurl:seed:keyword          # 剩余的种子关键词列表


