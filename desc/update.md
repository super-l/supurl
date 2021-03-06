
### 升级记录

#### 4.0版本 （预计2021-8-28）
- 新增搜狗引擎(中文 + 英文双引擎)
- 支持俄罗斯搜索引擎yandex
- 支持国外知名的AOL搜索引擎
- 优化谷歌搜索引擎
- 优化配置文件
- 去除分词功能，新增网页关键词"keywords"模式的拓展关键词模块
- 新增browser浏览器真实模拟采集模式
- 无需安装与运行chrome驱动

#### 3.7版本 （2021-8-17）
- 必应官方规则更新，程序同步升级
- 性能优化

#### 3.6版本 （2021-8-14）
- 适配必应相关参数，优化必应引擎针对国外网站采集的功能

#### 3.5版本 （2021-8-07）
- 在线文档更新
- 所有引擎的所有模式新增重试模式
- 百度引擎新增HTTP模式，也可使用selenium
- 新增只保留顶级域名模式！过滤二级域名、三级域名等！
- info命令增强，可查看更多状态信息
- 修复部分BUG


#### 3.4版本 （2021-8-03）
- 新增HTTP代理池功能(基础版)
- 搜索引擎逻辑优化
- selenium模式优化
- 无需手工运行浏览器驱动
- 强制关闭也可以自动清理遗留的chrome进程

#### 3.3版本 （2021-7-31）
- 优化redis池,防止阻塞；
- 新增域名过滤器,比如支持过滤gov.cn；
- 新增关键词过滤器,比如支持过滤"美女"；

#### 3.2版本 （2021-7-27）
- 新增linux启动与停止脚本
- 优化结果导出功能；
- 新增google采集模式(基于Facebook代理)；
- 配置信息优化,支持自定义redis池最大连接数；
- 支持自定义各个搜索引擎采集模式；
- 修复linux下stop命令无法停止的问题

#### 3.1版本 （2021-7-25）
- 优化redis连接池，防止redis高并发下的超时与系统资源占用；
- selenium采集模式优化；
- 配置信息优化；
- 支持自定义拓展关键词(自动分词)的线程数；
- 支持自定义外链采集线程数；
- 支持自定义采集结果保存类型，可以选择保存为域名，也可以是网址格式；

#### 3.0版本 （2021-7-20）
- 采集效率与性能优化，成倍提升！
- 采集逻辑优化，采集速度更快！
- 新增谷歌采集引擎
- 新增必应采集引擎
- 新增selenium采集模式
- 新增谷歌自定义语言，自定义国家参数配置
- 新增必应自定义语言，自定义国家参数配置
- 新增外链采集线程自定义参数配置
- 新增自动分词模式，同时支持中文分词与英文分词
- 修复一些遗留问题

#### 2.2版本
- 性能优化


#### 2.1版本

- 解决redis导出数据量大，导致的超时失败问题(采用分批导出)，可自定义每次读取数量；
- 支持自定义拓展关键词的生成线程(频率),防止高配服务器采集过快，导致关键词被消耗完的问题；
- 新增支持按天导出采集数据的功能；


#### 2.0版本

- 优化了程序运行的资源开销；
- 优化了日志，支持自定义日志输出级别；
- 优化了采集核心逻辑，提升采集效率；
- 新增后台运行模式；
- 新增停止采集功能；
- 新增导出功能，可自动导出,也支持自定义导出的文件名；
- 新增查看采集统计信息功能，可实时查看已采集到的域名数量等信息；
- 便携式安装与运行。去除了谷歌浏览器驱动和谷歌浏览器；
- 可一键清除redis中的历史数据，可自定义清除的类型；

#### 1.0版本