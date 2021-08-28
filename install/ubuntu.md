## ubuntu下supurl-plus环境安装教程

### 1：redis服务端安装
```
sudo apt-get install redis-server
```

安装完成后，Redis服务器会自动启动。

使用ps -aux|grep redis命令可以看到服务器系统进程默认端口6379

使用netstat -nlt|grep 6379命令可以看到redis服务器状态；

相关命令
```
sudo /etc/init.d/redis-server status   # 查看Redis服务器状态
sudo /etc/init.d/redis-server start    # 启动
sudo /etc/init.d/redis-server restart  # 重启
```


### 2：chrome浏览器下载安装

<font color="Hotpink">
注意：如果开启的搜索引擎中，使用的模式包含browser模式采集，则必须先安装chrome浏览器，如果只是HTTP模式，则无需安装!
</font>


```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb 
sudo dpkg -i google-chrome-stable_current_amd64.deb
sudo apt-get -f install -y
google-chrome --version # 查看版本

ubuntu chrome 中文字体乱码解决
sudo apt-get install ttf-wqy-microhei ttf-wqy-zenhei xfonts-wqy
```

### 3：采集软件下载与运行

采集软件其实无需安装，也属于绿色软件，只需要下载后解压即可使用；

前台运行模式，方便观察程序采集进度与输出，可以随时强制停止(建议配合screen命令使用，否则终端退出，软件就结束运行了)；

后台运行模式，就算终端退出，也可以持续运行。运行日志需要查看logs下的日志文件；

以下是采集程序的下载与启动说明:

```
# 下载最新程序
wget http://url.2te.cc/supurl-plus/release/linux/xxx.zip

# 解压并删除源文件
unzip xxx.zip && rm -rf xxx.zip

# 进入文件夹
cd xxx

# 按需要修改配置文件
vim config/config.ini

# 设置运行权限(可省略)
chmod +x supurl-plus

# 开始采集（后台运行)
./supurl-plus start -d -l

```
如果想要前台运行，则可使用下面的子终端模式：
```
# 创建一个子终端
screen -D -R supurl

# 进入程序所在目录
cd xxx

# 前台运行
./supurl-plus start -l
```