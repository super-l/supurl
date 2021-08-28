### 实时查看采集进度 | info

#### 一、通过软件自带命令查看
使用以下命令即可实时查看采集统计数据：

    supurl-plus.exe info

#### 二、通过redis客户端查看

使用客户端软件，链接redis服务器，如果redis是本地安装的，则：

    IP[服务器ip]: 127.0.0.1
    PORT[端口]:   6371
    AUTH[密码]:   留空

链接后，选择配置文件中对应的数据库编号(默认为0)，查看键：

    supurl:finished:data         # 采集结果列表
    supurl:finished:keyword      # 已经采集完成的关键词列表
    
    supurl:running:keyword       # 采集中关键词
    
    supurl:seed:host             # 剩余的种子域名列表
    supurl:seed:keyword          # 剩余的种子关键词列表
    
