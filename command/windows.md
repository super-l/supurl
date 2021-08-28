### windows系统-采集程序使用说明

查看命令帮助：

    supurl-plus.exe -h 
    

#### 启动采集任务

    进入程序根目录，双击运行cmd.bat文件，即可在当前目录的位置打开命令提示符窗口；
    
    启动采集任务的命令为：
        supurl-plus.exe start 参数列表
        
        -l 参数，可自动载入keyword.txt中的种子关键词到redis中；
        -d 参数，可在后台运行采集进程，不影响其他操作，也可一定程度上减少资源占用；
        -c 参数，可自动删除所有redis中的历史数据
        
        例子：
        如果想要后台运行，自动载入种子关键词，则命令行中输入以下命令(建议)
        supurl-plus.exe start -d -l 
        
        如果想要后台运行，并自动载入种子关键词，并且删除所有历史数据，则在命令行中输入以下命令：
        supurl-plus.exe start -d -l -c
        
        如果是想要前台运行，自动载入种子关键词，则命令行中输入：
        supurl-plus.exe start -l 
        
        如果是想要前台运行，自动载入种子关键词，并且删除所有历史数据，则命令行中输入：
        supurl-plus.exe start -l -c

   
    查看启动采集任务的命令的帮助说明：
    supurl-plus.exe start -h
        
    