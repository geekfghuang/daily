2018-01-24，星期三，深圳，晴朗
1. Spark学习：总体概念、各个组件、运行wordcount例子
   RDDs基本操作：Transformations、Actions 
   RDDs的特性：血统关系图、延迟计算 
   KeyValue对RDDs：重点combineByKey

2018-01-25，星期四，深圳，大部多云
1. 初步认识实时流处理：应用场景、技术选型（Spark Streaming、Storm）等
2. 学习分布式日志收集框架Flume：总体概念、架构
   监控一个文件实时采集新增的数据输出到控制台
   将A服务器上的日志实时采集到B服务器

2018-01-26，星期五，深圳，局部多云
1. 分布式发布订阅消息系统Kafka学习：架构及核心概念
   单节点单broker部署、单节点多broker部署
   容错性测试与理解
   整合Flume(1.8.0)和Kafka完成实时数据采集：exec-memory-avro -> avro-memory-kafka

2018-01-27，星期六，深圳，当前有霾
1. Spark Streaming入门：概述、词频统计例子
   spark-submit提交jar包方式运行词频统计
   spark-shell编程方式（scala）运行词频统计
   nc方式提交源数据
2. 分别从粗、细粒度理解Spark Streaming工作原理