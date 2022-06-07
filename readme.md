### 软件信息
```
软件名称：supurl
软件最新版本：4.0
最后更新时间：2021-8-27
支持系统：windows、 centos、 ubuntu、 mac等
```
github文档可能更新延迟，建议查看最新在线文档：[[http://www.msray.net/doc](http://www.msray.net/doc)]

<video id="video" controls="" width="390" height="300">
  <source id="mp4" src="http://url.2te.cc/supurl-plus/video/0-0.mp4" type="video/mp4">
</video>

### 软件简介
```
新一代的关键词域名采集系统(supurl-plus)，采用Go语言开发，每日采集不重复域名/网址超千万级！

可自定义开启与关闭国内采集、国外采集引擎。

可突破反爬虫机制，支持国内与国外多个主流的搜索引擎，支持自动拓展关键词，支持外链采集，支持批量采集等。

可根据用户提供的种子关键词txt文件，自动的从多个自定义的搜索引擎采集全网不重复域名/网址数据。

本软件提供持续的更新与维护服务。
```

### 文档目录

* [采集软件介绍](readme.md)
    * [软件说明](desc.md)
    * [功能一览](desc/function.md)
    * [更新记录](desc/update.md)
    * [配置文件详解](desc/config.md)
    * [支持的搜索引擎列表](desc/engine.md)
    * [视频演示效果](desc/video.md)
* [安装说明]()
    * [windows安装教程](install/windows.md)
    * [ubuntu安装教程](install/ubuntu.md)
    * [centos安装教程](install/centos.md)
   
* [使用技巧]()    
    * [采集国外域名或网址的配置说明](config/english.md)
    * [如何保存采集结果是网页地址,而不是域名?](config/domain-url.md)
    * [如何进行精准采集,只保存搜索引擎的结果？](config/accurate.md)
    * [如何采集结果只保留顶级域名？](config/topdomain.md)
    * [如何过滤指定后缀域名或忽略敏感关键词？](config/filter.md)
    * [什么是采集模式？如何选用http,browser模式？](config/model.md)
    * [如何设置最佳的搜索引擎采集线程数？](config/thread.md)
    * [如何设置与开启采集HTTP代理池？](config/proxy.md)
    
* [使用教程]()
   * [windows手工使用说明](use/windows.md)
   * [linux一键脚本使用说明](use/auto-linux.md)
   * [linux手工使用说明](use/linux.md)


* [命令文档]()
    * [windows使用说明](command/windows/start.md)
        * [启动采集任务](command/windows/start.md)
        * [实时查看采集进度](command/windows/info.md)
        * [停止采集任务](command/windows/stop.md)
        * [导出采集结果](command/windows/export.md)
        * [自定义清除redis中的数据](command/windows/clear.md)
        * [动态添加新的种子关键词](command/windows/loadkey.md)
        * [查看当前程序版本](command/windows/version.md)
        
    * [linux使用说明](command/linux/start.md)
        * [启动采集任务](command/linux/start.md)
        * [实时查看采集进度](command/linux/info.md)
        * [停止采集任务的方法](command/linux/stop.md)
        * [导出采集结果的方法](command/linux/export.md)
        * [自定义清除redis中的数据](command/linux/clear.md)
        * [动态添加新的种子关键词](command/linux/loadkey.md)
        * [查看当前程序版本](command/linux/version.md)
    
* [手工升级说明]()
    * [windows升级教程](update/windows.md)
    * [linux升级教程](update/ubuntu.md)
  
* [常见问题]()
    * [如何订购采集系统？](question/buy.md)
    * [免费试用与体验说明](question/trial.md)
    * [功能拓展与需求定制说明](question/diy.md)
    * [采集系统前台运行与后台运行的区别](question/difference.md)
