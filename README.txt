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

2018-02-03，星期六，深圳，局部多云
1. 将清洗、过滤后的访问日志进行相应RDDs转换得到当天到现在为止具体条目的访问次数统计结果
2. 将统计结果入库到HBase
   在Scala中调用Java函数、Java经过一层Thrift到Go服务，Go服务与HBase Thrift服务相连
   为了避免Java HBase接口Deprecated以及Java HBase Client版本更换的麻烦，中间加一层Thrift，用Go最新的HBase Thrift Client连接HBase

2018-02-04，星期日，深圳，晴间多云
1. 将清洗、过滤后的访问日志进行相应RDDs转换得到当天到现在为止由搜索引擎引流过来具体条目的访问次数统计结果
2. Go服务将统计结果入库到HBase时遇到问题，具体问题如下：
   共享变量var HBaseClient *hbase.THBaseServiceClient会报EOF等错误，将其改成每更新一条数据重新申请一个HBaseClient对象（局部），则问题解决
   但类似简单对象访问方法、数据库连接对象、RPC Client对象等多线程共享访问的具体细节以及网络数据返回格式细节，有待研究
3. 构建可视化的必要性：从模糊、抽象到具体、形象的过程，提高行业决策效率
   ECharts的简单使用：柱状图、饼图

2018-02-05，星期一，深圳，晴间多云
1. ECharts前端ajax从后端拉取json数据做可视化呈现
2. DataV可视化框架的见识：通过配置MySQL数据源、SQL语句、间隔时间等，将数据从后端拉取做可视化呈现
3. Scala、Java、Python都可以写Spark计算作业，但Scala更简洁更优雅
   Scala可以与Java相互调用，Scala写计算作业时，一些常用Java类库函数可以直接调用

2018-02-06，星期二，深圳，晴间多云，14°
1. Scala程序设计基础学习
   函数式编程思想、Scala语言基础
   尾递归优化普通递归函数可能引起的栈溢出问题
   用递归思想+函数式编程的方式4行代码实现快速排序
2. Redis学习：Redis初识&复习、基本数据结构
   单线程、原子性：Redis在一个瞬间只会执行一条命令，可用于分布式ID生成器
   epoll IO多路复用模型：当客户端网络文件描述符ready时，即有命令写入
   string：set、set nx|xx|ex、incr、incrby等

2018-02-07，星期三，深圳，晴间多云，15°
1. Redis学习：基本数据结构
   hash：key field value，可类比关系型数据库，但具体field的ttl难以控制，可通过程序逻辑控制
   list：链表实现，可作为简单消息队列，brpop key timeout设置阻塞等待
   set：sadd、smembers、spop（随机弹出一个元素），sinter（共同关注）、sdiff、sunion [store destkey]
   有序集合zset：默认从小到大，zadd、zincrby、zrange、zrangebyscore，常用排行榜实现
   慢查询slowlog：在命令生命周期的第三个阶段，可设置慢查询队列长度、慢查询时间阈值
   流水线pipeline：1次网络+n条命令，到达服务器时命令会被拆分开，因此不是原子操作，而mget、mset等都是原子操作
   发布订阅：channel与模式两种方式，channel用字典，模式用链表。每publish一条消息，从channel字典中取出客户端发送消息，然后遍历模式链表，如果模式与channel匹配，则发送
   发布订阅与消息队列不同的是，发布订阅不会堆积历史消息
   bitmap：类型其实为string，最大到512MB。一般用来按位操作，使用恰当可节省内存
   hyperloglog：本质还是string，三个命令pfadd、pfcount、pfmerge，一般用来统计独立用户总数等，极度节省内存，百万的数据才消费15KB左右的内存。但有0.81%的错误率，且无法取出单条数据
   geo：geoadd、geopos、geodist等命令，可计算两个城市（经纬度）的距离，方圆多少公里内的远近城市等，底层为zset

2018-02-08，星期四，深圳，晴间多云，17°
1. Redis学习：持久化
   RDB快照：save会阻塞排队的所有命令；bgsave会阻塞于fork产生子进程用于持久化，但fork是很快的，排队的命令基本不会阻塞；save 60 10000等配置都是基于bgsave实现
   RDB存在的问题：耗时耗性能（O(n)时间复杂度、fork()消耗内存）、容易丢失数据（save配置）
   AOF：appendonly yes、appendfsync everysec；always每条写命令都从缓冲区刷新到硬盘、everysec每秒将缓冲区里的写命令刷新到硬盘、no不可控，由OS决定刷新到硬盘的时机
   AOF重写：bgrewriteaof命令或基于AOF重写配置，从内存中优化写命令到AOF文件中，注意并不是读入原生AOF文件做优化。例原生AOF incr count、incr count、incr count，重写后AOF set count 3
   bgrewriteaof子进程在重写AOF的过程中，新来的写命令会通过父进程进入aof-rewrite-buf，此buf的命令再同步到新的AOF文件中
   一般情况下不会使用RDB，会将其关掉；一般会使用AOF everysec的配置，当然要考虑具体应用场景