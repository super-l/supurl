### 检查redis服务是否启动的方法

程序依赖redis数据库，如果redis没有运行，则无法开始采集，会提示redis连接失败！

如果是linux系统，redis服务可开机自动启动，每次使用都可以省略这一步；

windows检查方法：

    打开任务管理器，查看进程列表中是否存在redis；

linux检查方法：

    ps -ef | grep redis  # 通过进程查询
    netstat -ntlp        # 通过网络端口
