## 采集系统前台运行与后台运行的区别


前台运行，会在当前终端实时显示采集日志；如果ssh链接断开，或者其他方式导致终端关闭，则采集系统也会被关闭；



后台运行，不会在ssh链接断开或者终端关闭的情况下推出；而日志信息在logs目录下以文件的方式存储；
