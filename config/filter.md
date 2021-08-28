### 如何过滤指定后缀域名或忽略敏感关键词？

比如，以下例子就是会忽略域名中包含".gov.cn""的结果。

并且，自动扩展关键词时，如果关键词包含"政府",则也不进行拓展!

```
[filter]
# 域名过滤列表，以英文逗号分隔
domain = .google.com,.google.cn,.gov.cn,.baidu.com,.58.com,.youdao.com,.cdict.net,.amazon.com

# 关键词过滤列表，如果拓展词语包含以下字符，则不添加
keyword = 政府,学院,大学

```