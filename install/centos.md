## centos下supurl-plus环境安装教程

### 1：redis服务端安装
```
# download fedora epel
yum install epel-release -y

# install redis
yum install redis -y

# 启动redis
service redis start

# 停止redis
# service redis stop

# 重启redis
service redis restart

# 查看状态
service redis status

# 自动启动
chkconfig redis on  
```

### 2：chrome浏览器下载与安装

<font color="Hotpink">
注意：如果开启的搜索引擎中，使用的模式包含browser模式采集，则必须先安装chrome浏览器，如果只是HTTP模式，则无需安装!
</font>

```
# 创建yum源文件
[root@localhost /]# cd /etc/yum.repos.d/
[root@localhost /]# touch google-chrome.repo

# 输入yum源信息
[google-chrome]
name=google-chrome
baseurl=http://dl.google.com/linux/chrome/rpm/stable/$basearch
enabled=1
gpgcheck=1
gpgkey=https://dl-ssl.google.com/linux/linux_signing_key.pub


# 安装chrome
[root@localhost /]# yum -y install google-chrome-stable --nogpgcheck

# 检查是否安装完成与版本,如果正常显示出chrome的版本信息，那么就是按照成功了
[root@localhost /]# google-chrome --version

```


### 3：采集软件下载与运行

采集软件其实无需安装，也属于绿色软件，只需要下载后解压即可使用；

前台运行模式，方便观察程序采集进度与输出，可以随时强制停止(建议配合screen命令使用，否则终端退出，软件就结束运行了)；

后台运行模式，就算终端退出，也可以持续运行。运行日志需要查看logs下的日志文件；

以下是采集程序的下载与启动说明:

```
# 下载最新程序
wget http://url.2te.cc/supurl-plus/release/linux/3.6.zip

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