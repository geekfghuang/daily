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

2018-01-28，星期日，深圳，多云
1. 学习Spark Streaming核心概念与编程（IDEA工程、scala）
   StreamingContext、DStream、InputDStreams、Receivers
   Transformations、OutPutOperations
   Spark Streaming处理socket数据
   Spark Streaming处理文件系统（hdfs/local）数据

2018-01-29，星期一，深圳，大部多云
1. Spark Streaming进阶与编程
   foreach将统计结果入库MySQL：connection序列化问题、性能问题
   窗口函数的理解与使用：窗口长度、滑动距离
   黑名单过滤：transform、leftOuterJoin、filter、map
2. Spark Streaming整合Flume编程：Flume采取Push方式
   Spark Streaming先启动，充当avro source agent的角色A（打开端口接收数据）
   Flume后启动，其avro sink指向A
   mvn打包scala源码为jar包，spark-submit --packages 外部依赖jar 方式提交计算作业

2018-01-30，星期二，深圳，多云
1. Spark Streaming整合Flume编程：Streaming采取Pull方式
   Flume相关jar包版本准确配置
   Pull使用一个可靠的receiver且基于事务的方式从Flume sink缓冲里拉取数据
   当数据被Streaming接收且复制完后，事务才算执行成功

2018-01-31，星期三，深圳，阵雨
1. Spark Streaming整合Kafka编程：基于Receiver方式
   Streaming开启Receiver Job接收Kafka的数据，存储到Executor（内存）中
   可以增加WALs的方式提高故障容错能力
2. Spark Streaming整合Kafka编程：基于Direct方式
   关注Direct与Receiver两种方式从Kafka读取数据的内部细节、区别与优缺点

2018-02-01，星期四，深圳，大部多云
1. 整合Flume、Kafka、Spark Streaming，实现通用流处理平台
   log4j将日志输出到Flume avro source
   日志经过Flume Kafka sink配置输出到Kafka
   Spark Streaming读取Kafka的日志数据做计算处理

2018-02-02，星期五，深圳，大部多云
1. 用Python开发用户访问行为日志产生器，并用crontab定时调度产生日志
2. Flume收集产生的日志到Kafka，Spark Streaming从Kafka接收日志数据
   Spark Streaming Scala编程将接收到的日志数据进行清洗：转换格式，过滤等
   RDDs Scala编程再度熟悉，对数据清洗有了具体的概念