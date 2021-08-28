### ubuntu安装redis服务端

#### 1. 修改apt-get源
    
    （1）先使用如下命令，备份系统原本的源文件：
    sudo mv /etc/apt/sources.list /etc/apt/sources.list.bak20181105
    
    （2）编辑文件，更换为阿里云的源
    sudo vim /etc/apt/sources.list
       
    复制以下内容到sources.list:
    
    deb-src http://archive.ubuntu.com/ubuntu xenial main restricted #Added by software-properties
    deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted
    deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted multiverse universe #Added by software-properties
    deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted
    deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted multiverse universe #Added by software-properties
    deb http://mirrors.aliyun.com/ubuntu/ xenial universe
    deb http://mirrors.aliyun.com/ubuntu/ xenial-updates universe
    deb http://mirrors.aliyun.com/ubuntu/ xenial multiverse
    deb http://mirrors.aliyun.com/ubuntu/ xenial-updates multiverse
    deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
    deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse #Added by software-properties
    deb http://archive.canonical.com/ubuntu xenial partner
    deb-src http://archive.canonical.com/ubuntu xenial partner
    deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted
    deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted multiverse universe #Added by software-properties
    deb http://mirrors.aliyun.com/ubuntu/ xenial-security universe
    deb http://mirrors.aliyun.com/ubuntu/ xenial-security multiverse

    （3）：执行更新
    sudo apt-get update

#### 1. 安装redis与运行
    
    执行以下命令，即可快速安装redis服务器：
    sudo apt-get install redis-server -y
    
    
    以下是一些redis常用操作：
    ps -aux|grep redis
    
    检查端口：
    netstat -nlt|grep 6379
    
    查看状态命令:
    
    sudo /etc/init.d/redis-server status 查看状态
    
    service redis status  查看状态
    service redis start   启动
    service redis stop    停止
    service redis restart 重启
