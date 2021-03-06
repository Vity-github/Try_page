## 大数据的感知与获取
### 数据渠道
|数据来| 数据类别|描述|   
|-|-|-|
|本单位自营|自营系统|理论上数据可以最大限度共享|
||历史遗留数据|纸质文档或存放在历史数据中|
|外单位他营|其他利益主题运营平台|和自营系统类似，仅归属不一样|
||物联网数据|由具体利益主体运营，与自营系统类似，仅归属不一样|
||政府数据|政府执行政府职能而存放的数据|
||移动互联网数据|以网页的行书存放在互联网当中|

### 内部数据以及获取方法
ELT（Extract-Transform-Load）    
数据库、文件、其他---->抽取、转换、加载---->目的数据
| | | |
|-|-|-|
|数据抽取|全量抽取||
||增量抽取|日志对比、时间戳、全表对比、触发器|
|数据加工和转换|ETL引擎|数据转换组件|
||数据库|SQL指令|
|数据加载||SQL语句进行插入更新删除操作|
|||e.g.bulk,bcp,关系数据库的批量装在工具SQL*Loader(SQLLDR)等|

#### 主流ETL工具对比
![](ware1.png)
![](ware2.png)
---
### 外部数据以及获取方法
*网络爬虫*
网络爬虫的基本框架
![](pachong.png)
网络爬虫流程    
1. 指定入口URL，将其加入URL队列
2. 将种子URL加入待抓取URL队列
3. 从待抓取URL中一次获取URL，在互联网上下载网页
4. 将网页的URL保存到已经抓取的URL中，将网页信息保存到下载网页库中，从网页中抽取新的所需要抓取的UR并加入带抓取的URL队列中
5. 重复1~4直到URL队列为空
爬虫类型
![](pachong2.png)
不同爬取策略比较
![](pachong3.png)
PageRank简介
![](pagerank.png)
爬虫工具比较
![](pachongtool.png)
---
## 深网数据以及获取方法
> 深网：在互联网上可得到的，但传统搜索引擎由于技术限制不能或者经过慎重考虑不愿意做索引的网页、文件、或者其他高质量、权威的信息
### 简介
搜索引擎搜索结果是网页，而DeepWeb中的搜索结果主要是结构化的数据。   
Deep Web数据库通常有复杂的接口，而搜索引擎的接口较为简单，一般是关键字搜索。    
搜索引擎对结果的排序是根据搜索结果与所提交查询的相似性，Deep Web数据库则是根据结果中对DeepWeb中信息的获取主要的途径是通过某个属性的值。        
深网数据采集是通过对网站中所提供的查询接口提交查询来获得，每个查询接口支持在若干个属性上进行查询，这和对搜索引擎的访问在某种程度上来说是相似的，但DeepWeb数据和搜索引擎二者之间是有着很大区别的。    
深网数据采集分为两大子问题：查询接口识别；自动填写表单    
1. 查询接口识别
![](jiekoushibie.png)
2. 自动填写表单
![](tianxiebiaodan.png)

