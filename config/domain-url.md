### 如何保存采集结果是网页地址,而不是域名?

修改配置文件即可。默认为domain(保存为域名),如果需要保存网页地址，则改为 url

```
[base]
# 采集类型，域名=domain 网址:url
save_type = domain
```