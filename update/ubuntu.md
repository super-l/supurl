## linux下supurl-plus手工升级教程

1: ssh客户端登录服务器；

2: 使用cd命令进入软件目录；

3：使用wget命令下载程序压缩包(联系客服获取最新版)，如：

wget http://url.2te.cc/supurl-plus/release/linux/xx.zip

4: 解压压缩包并删除压缩包

unzip xx.zip && rm -rf xx.zip

5：修改默认的配置文件*(config/config.ini)*中的参数,根据自己服务器的配置做响应的调整即可

6：根据需求，可开启http代理(一般不需要)，如果开启，则需要编辑config/proxy.txt录入代理数据(一行一个)；

6：升级完成
