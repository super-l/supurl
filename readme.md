### 最新公告
```
2021-06-21 ：supurl-depth v1.0 上线！用于高并发大规模的域名深度采集，每天可轻松采千万级域名；

2021-06-10 ：supurl v1.0 已上线！用于关键词精准采集；
```

### 系统简介

新一代的关键词URL采集系统(Supurl)。采用Go语言 + java语言实现。前端采用vue。可突破搜索引擎的反爬虫机制！

supurl为系列产品。有多个版本，面向的用户不同。

可根据用户录入的关键词，自动化的使用全网主流的多个搜索引擎(包括但不限于百度、谷歌、必应、搜狗、搜搜等)，获取搜索引擎的返回结果进行统一采集与处理的一款程序。采集与处理的信息包括但不限于真实URL地址、排名、标题等。


笔者很多年前使用python开源的superl-url，被多人随便改了拿去卖，已停止维护。有技术能力的可以自己下载去改了用。

现在最新重构的Supurl系列产品为商业版本，完全重写，使用的采集核心技术方案也不同，不开源。


如需使用，可联系QQ：86717375 
忘忧草安全交流2群：50246933


### 关于不同版本的说明

根据用户需求的不通，本系统分为多个版本。

| 产品名称 | 产品编码 | 收费方式 | 说明 |
| :------| :------: | :------: |:------: |
| supurl | supurl | 按月| 用于指定关键词的精准采集，支持所有主流搜索引擎，带网站管理后台；可获得标题，对应搜索引擎的排名，网页URL，域名等多种信息，支持自定义API推送接口，支持自定义多种过滤方案 |
| supurl-depth | depth01| 按月 | 用于批量指定关键词的大规模深度采集，自动拓展相关词。每天可轻松采集千万条域名。支持百度 + 必应搜索引擎；只采集域名，自动重复过滤。|

#### 关于supurl的更多介绍

https://github.com/super-l/supurl/tree/main/supurl

#### 关于supurl-depth的更多介绍

https://github.com/super-l/supurl/tree/main/supurl-depth


### 系统优势

- 全新的构架设计，可突破所有搜索引擎的反爬虫机制！
- 完美兼容支持所有搜索引擎，可多个搜索引擎并发采集；
- 稳定性与效率高；
- 采用GO语言实现采集核心，并且交叉编译跨平台，可完美运行在ubuntu、centos、windows、mac等系统；
- 拥有网站后台，在后台即可实现采集任务的管理与方案自定义。无需技术经验，小白也能快速上手！
- 灵活的过滤方案自定义、重复判断模式自定义；
- 灵活的导出功能，同时支持导出excel表格csv、json、txt等文件；
- 强大的HTTP API推送接口功能，可实现采集结果的推送。可进行二次开发拓展，对接到自己的接口，灵活存储与自定义结果。

### 网站后台截图(supurl)

![登录页面](images/login.png)
![会员首页](images/home.png)
![任务列表页面](images/urltask_list.png)
![任务添加页面](images/urltask_add.png)
![推送方案管理页面](images/push.png)
![域名过滤方案管理页面](images/filter-domain.png)
![标题过滤方案管理页面](images/filter-title.png)

### 采集客户端运行截图(supurl)

![运行1](images/run1.png)
![运行2](images/run2.png)
![运行3](images/run3.png)

### 演示视频(supurl)

暂无

### 关于HTTP推送接口说明(supurl)

```
推送请求地址：任务中选择的推送方案的HTTP地址
推送请求方式：POST
推送请求类型：application/json
推送请求参数：

{
    "id": 1,             
    "task_id": 1,        
    "engine": "baidu",
    "keyword": "关键词",
    "url": "http://www.xxx.com/article/1.html",
    "domain": "www.xxx.com",
    "title": "网页标题",
    "weight": 1,
    "is_repeat": false,
    "code_language": "",
    "webcms": "",
    "web_server_name": "",
    "registed_at": "",
    "contact_email": "",
    "contact_name": "",
    "contact_mobile": "",
    "created_at": ""
}

注意: 会员的HTTP接口每次正常接收完数据后，需要输出字符串"success"，否则会视为推送不成功。

```
| 字段名称 | 示例值 | 说明 |
| :------| :------: |:------: |
| id | 1 | URL结果的ID编号 |
| task_id | 1 | 所属任务的ID编号 |
| engine |  baidu | 对应的搜索引擎别名 |
| keyword | 最新漏洞 | 搜索的关键词 |
| url | https://www.cnvd.org.cn/webinfo/show/3096 | 网页完整地址 |
| domain | www.cnvd.org.cn | 网页所属的域名 |
| title | 常见漏洞类型汇总 - 国家信息安全漏洞共享平台 | 网页的标题 |
| weight | 1 | 搜索引擎的排名 |
| is_repeat | false| 是否属于重复过滤 true表示被过滤的,false表示没被过滤 |
| code_language | php | 网站后端开发语言 暂不支持 |
| webcms | dedecms | 网站使用的开源网站系统名称 暂不支持 |
| web_server_name | apache | 网站使用的web服务器名称 暂不支持 |
| registed_at | 2020-10-01 | 网站域名的注册时间 暂不支持 |
| contact_email | 123456@qq.com | 网站的联系邮箱 暂不支持 |
| contact_name | 张三 | 网站的联系人 暂不支持 |
| contact_mobile | 13000000000 | 网站的联系方式 暂不支持 |
| created_at | 2021-06-12 | 采集入库时间 |


### 技术实现

- 采用Go语言作为采集客户端的开发语言，交叉编译跨平台；
- 采用selenium实现采集基础核心；
- 采用redis作为内存数据库；
- 采用rabbitmq消息队列；
- 采用内存操作算法实现结果的去重复；
- 采用sqlite作为本地微型数据库，实现数据的入库、结果统计等；
- 采用java作为会员端API接口的转发服务；
- 采用vue + elementui用于会员网站系统的前端开发；

### 联系方式

- 联系QQ： 86717375

- 忘忧草安全交流2群：50246933



