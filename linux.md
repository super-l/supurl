### linux简单运行步骤

    1. 使用ssh客户单软件，链接服务器的终端；
    2. 使用cd命令，进入supurl-plus程序的根目录，比如:cd /root/3.0
    3. 第一次运行的时候，建议修改配置文件(config/config.ini);
    
    4. 使用以下命令即可后台启动采集：
    ./supurl-plus start -d -l 
    
    5：使用以下命令，可以实时查看采集数量：
    ./supurl-plus info
    
    6: 使用以下命令，可以导出采集结果：
    ./supurl-plus export
          
    7: 使用以下命令，可结束采集：
    ./supurl-plus stop
    
    8: 使用以下命令，可以不关闭程序换关键词,并删除所有历史数据：
    ./supurl-plus clear -m all
    ./supurl-plus loadkey 新关键词文件名.txt
    
    
    更多使用命令，查阅：http://url.2te.cc/supurl-plus/doc/use.html

