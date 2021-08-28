### 采集软件配置文件参数详解

配置文件在程序的根目录下的config文件夹中，文件名:config.ini

注意，该文件需要使用编辑器打开！推荐下载安装notepad++ 或者 sublime text3编辑器。

如果无需开启某些搜索引擎，则把搜索引擎对应的线程数调整为0即可！

```
[base]

# 浏览器驱动的超时时间,无需修改。建议在300-500
driver_timeout = 300

# 是否显示浏览器窗口(必须是有界面的操作系统，否则会出错。如windows，或者ubuntu,centos的图形桌面)
show_browser = false

# 采集类型，域名=domain 如果是采集网址URL，则改为"save_type = url"
save_type = domain

# 是否开启proxy代理功能(随机)，一般不需要。config/proxy.txt文件中按行存取HTTP代理信息.目前仅对http模式有效
allowed_multiple_proxy = false

# 采集的搜索引擎页数。建议5-10之间
max_page = 8

# 是否按日期存储采集结果,如果开启，则改为true(开启此配置，导出的时候需要修改out节点的keyname参数)
is_save_date = false

[redis]
# redis链接地址和端口,无需修改
uri = 127.0.0.1:6379

# redis密码,可以为空，如果有密码则填写。
password =

# redis数据库编号,无需修改，如redis中有其他数据，则可以区分
db = 0

# redis链接池的最大并发链接数据，为0表示不限制,无需修改
redis_max_connect = 0


[external_links]

# 是否开启网页外链采集引擎。如果不开启，则所有采集结果都是搜索引擎的结果
allowed_extend_links = true

# 外链采集线程数，建议50-500
extend_links_thread = 100


[expand_keyword]

# 是否开启相关词采集
allowed_related_keyword = true

# 是否允许提取网页的关键词文本进行拓展种子关键词
allowed_page_keyword = true

# 关键词拓展引擎线程数，建议1-5
extend_page_keyword_thread = 1

# 是否忽略中文关键词,如果关键词包含中文内容，则不添加。如果采集国外网站，则建议开启
expand_keyword_ignore_chinese = false


[baidu]
# 百度线程数，http模式，建议50-200；selenium模式，建议2-10；如果不使用，则设置为0
baidu_thread = 100

# 百度引擎的模式，包括http(推荐)，browser模式
baidu_method = http


[google]

# 谷歌线程数，所有模式都建议设置为1，如果不使用，则设置为0
google_thread = 1

# 谷歌引擎的模式，包括browser(推荐),facebook,http等
google_method = browser

# 搜索结果语言,如US,JP,HK,具体请查阅软件说明文档的附录
region =

# google主页网址，不带/,如https://www.google.com.hk
homepage =

# 采集间隔，延迟最小值
sleep_min = 10

#  采集间隔，延迟最大值
sleep_max = 40

# facebook的cookie，如果不使用facebook模式，则无需填写
cookie = datr=yRT-YFVCa9RTmMN8pKqh-DMv; _fbp=fb.1.1627264203176.503293882; sb=4hT-YD9s7VEPc3KlJkR-Sisl; dpr=2; locale=zh_HK; c_user=100069669150911; wd=1334x707; spin=r.1004169743_b.trunk_t.1627482069_s.1_v.2_; xs=9%3ASJ7R4NLjoVL6DA%3A2%3A1627281279%3A-1%3A-1%3A%3AAcXH_0ghVVEHf4gmau0WefB4OlwgDdhXjDkR1yPZFQ; fr=1qvvDDImEvA14Ui48.AWXh4ZBnte7n30dk-DrW4axZD_0.BhAWfW.ST.AAA.0.0.BhAWfW.AWUIiLJadJc


[bing]
# 必应线程数，http模式建议50-200；selenium模式暂未支持，如果不使用，则设置为0
bing_thread = 50

# 必应引擎的模式，包括http(推荐)，browser模式
bing_method = http

# 必应结果区域,如zh-cn，en-us具体请查阅软件说明文档的附录。不填写则无限制
region =

# 必应结果语言,如en，jp，fr具体请查阅软件说明文档的附录。不填写则无限制
language =


[sougou]

#  搜狗引擎的结果语言 english  all
sougou_language = english

# 搜狗线程数，http模式建议50-200；如果不使用，则设置为0
sougou_thread = 1

# 搜狗引擎的模式，包括http,browser模式
sougou_method = browser


[yandex]
# yandex线程数，http模式建议50-200；如果不使用，则设置为0
yandex_thread = 1

# yandex引擎的模式，仅包含browser模式
yandex_method = browser


[aol]
# aol线程数，http模式建议50-200；如果不使用，则设置为0
aol_thread = 1

# aol引擎的模式，仅包含browser模式
aol_method = browser


[filter]
# 域名过滤列表，以英文逗号分隔
domain = .gov.cn,.baidu.com,.58.com,.youdao.com,.cdict.net,.amazon.com

# 关键词过滤列表，如果拓展词语包含以下字符，则不添加
keyword = 政府,大学

# 是否只保留顶级域名? 无限制 = false, 只采集顶级域名=true
only_top_domain = false

[out]
# 每批次导出读取的数量，避免大数据超时
read_number = 3000

# 导出的redis键名  按天保存如 supurl:finished:data:2021-08-27
keyname = supurl:finished:data

# 导出的结果文件名
filename = result.txt
```
