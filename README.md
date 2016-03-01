# EsKeeper

## 目录
- [概述](#概述)
- [需求](#需求)
	- [eskeeper-admin 需求](#eskeeper-admin 需求)
	- [eskeeper-drive 需求](#eskeeper-drive 需求)
- [部署](#部署)
- [用户使用手册](#用户使用手册)
- [项目计划](#项目计划)




## 概述
自己练手的一个项目

项目目前主要有:

* eskeeper-admin
	
	主要产生基于ES集群的监控需求, 简单的管理需求, 常用诊断积累.
	
* eskeeper-drive

	主要针对java开发人员, 可以提供基于 Java api, Restful api, Sql的操作, 封装原有的EsClient.

软件环境为: JDK1.8

## 需求

### eskeeper-admin 需求

* 集群列表
	* 集群名称
	* 集群状态
	* 节点数
	* 索引数
	* 分片数
	* doc数
	* 占用总存储空间

* 节点列表
	* 节点基本信息: 节点名称; ip:port; 节点类型; JVM版本; es版本
	* load average(1分钟, 5分钟,15分钟)
	* cpu%
	* heap usage%
	* disk usage%
	* memory%
	* 性能图表; templates; cat api

* 具体节点详细图片
	* jvm图表
	* fs状态
	* os状态
	* thread pool
	* hot_threads
	


* http://192.168.10.235:9200/_nodes/_all/os,jvm?pretty
* 节点所有jvm监控信息, http://192.168.10.235:9209/_nodes/stats/jvm?pretty
* 所有节点使用磁盘的状态, http://192.168.10.235:9209/_nodes/stats/fs?pretty
	各字段说明.
* 各节点所在操作系统负载状况, http://192.168.10.235:9209/_nodes/stats/os?pretty
* thread_pool信息监控, http://192.168.10.235:9209/_nodes/stats/thread_pool?pretty
* 索引状态监控, http://192.168.10.235:9209/_nodes/stats/indices?pretty
* 整个集群正在执行的任务列表, http://172.16.10.18:9201/_cluster/pending_tasks?pretty
* 整个集群的健康状况: http://192.168.10.235:9209/_cluster/health?pretty
* 当前节点下所有状态信息(比较全): http://localhost:9200/_cluster/stats?pretty&human
* 当前节点下哪个资源在最近10秒钟之内耗费资源,具体在做什么: http://192.168.10.235:9209/_nodes/hot_threads?ignore_idle_threads=true&interval=500ms&threads=3&type=cpu
* 分词接口: http://192.168.10.235:9209/eagleye_bigindex_2016.02.21_short/_analyze?field=log.body

### eskeeper-drive 需求



## 部署


## 用户使用手册


## 项目计划



	



