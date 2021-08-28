### 导出采集结果的方法

#### 一、软件自带导出功能

使用以下命令即可一键导出所有不重复的域名采集结果

    ./supurl-plus.exe export   # 默认导出全部结果，保存为result.txt文件，每批次读取3000条(默认)结果写入.
    
    上面的命令，等同于命令：
    ./supurl-plus.exe export -f result.txt -n 3000 -k supurl:finished:host
    
支持自定义导出文件名：

    ./supurl-plus.exe  export -f res.txt # 保存为res.txt文件 每批次读取5000条记录写入结果


支持自定义每批次读取与写入的数量(影响导出时间)：

    ./supurl-plus.exe  export -n 5000   # 保存为默认的result.txt文件 每批次读取5000条记录写入结果

支持按天导出，自定义导出的redis的键名(keyname):
    
    # 导出键名为"supurl:finished:host:2021-06-15"的所有数据，保存为res.txt文件 每批次读取5000条记录写入结果
    ./supurl-plus.exe  export -k supurl:finished:host:2021-06-15 -f res.txt -n 5000


运行结果如：
```
supurl-plus.exe export -f res.txt -n 5000

当前要导出的key名称为:supurl:finished:host
等待导出的结果数量:167464
正在分批次读取与写入结果文件(每批5000条)...
导出成功！数据条数:167464
导出完成,欢迎下次继续使用!本次操作用时:0.564438234 秒
superldeMacBook-Pro:supurl-plus superl$ 
```


#### 二、其他导出方法

由于采集结果是存储在redis中的，所以二次开发拓展性很强，可以自己写导出脚本，链接redis服务器，读取数据，导出到任何地方。

比如：
    自写脚本，导出结果到Mysql，导出到es,导出到excel等。
    
    
    