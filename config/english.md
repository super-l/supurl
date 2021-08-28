### 采集国外域名或网址的配置说明

如果仅仅需要采集国外站：

1：建议关闭百度引擎
```
由于百度只适合中文采集，所以建议关闭，修改配置文件，把百度线程数设置Wie0即可。
[baidu]
baidu_thread = 0
```

2：可选择开启必应引擎
```
必应引擎也适合采集国外网站！下面是采集英文网站的示例配置
[bing]
# 线程数建议30-100
bing_thread = 30

# 必应引擎的模式，包括http(推荐)，browser模式
bing_method = http

# 必应结果区域,如zh-cn，en-us具体请查阅软件说明文档的附录。不填写则无限制
region = en-us

# 必应结果语言,如en，jp，fr具体请查阅软件说明文档的附录。不填写则无限制
language = en
```

3: 可选择开启引擎谷歌
```
[google]

# 谷歌线程数，建议固定设置为1，否则可能被封IP。如果不使用，则设置为0
google_thread = 1

# 谷歌引擎的模式，包括browser(推荐),facebook,http等
google_method = browser

# 搜索结果语言,如US,JP,HK,具体请查阅软件说明文档的附录
region =

# google主页网址，不带/,如https://www.google.com
homepage =

# 采集间隔，延迟最小值。如果比较小，可能会触发反爬虫机制。建议10以上
sleep_min = 10

#  采集间隔，延迟最大值。如果比较小，可能会触发反爬虫机制。建议30以上
sleep_max = 40

# facebook的cookie，如果不使用facebook模式，则无需填写
cookie = datr=yRT-YFVCa9RTmMN8pKqh-DMv; _fbp=fb.1.1627264203176.503293882; sb=4hT-YD9s7VEPc3KlJkR-Sisl; dpr=2; locale=zh_HK; c_user=100069669150911; wd=1334x707; spin=r.1004169743_b.trunk_t.1627482069_s.1_v.2_; xs=9%3ASJ7R4NLjoVL6DA%3A2%3A1627281279%3A-1%3A-1%3A%3AAcXH_0ghVVEHf4gmau0WefB4OlwgDdhXjDkR1yPZFQ; fr=1qvvDDImEvA14Ui48.AWXh4ZBnte7n30dk-DrW4axZD_0.BhAWfW.ST.AAA.0.0.BhAWfW.AWUIiLJadJc

```

4: 可选择开启yandex引擎
```
# yandex线程数，建议为1-5
yandex_thread = 1

# yandex引擎的模式，仅包含browser模式
yandex_method = browser
```



5: 可选择开启aol引擎
```
# aol线程数，建议为1-5
aol_thread = 1

# aol引擎的模式，仅包含browser模式
aol_method = browser
```

6: 可选择开启搜狗引擎

```
#  搜狗引擎的结果语言 english  all
sougou_language = english

# 搜狗线程数，建议为1
sougou_thread = 1

# 搜狗引擎的模式，包括http,browser模式
sougou_method = http

```