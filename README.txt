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
   bgrewriteaof子进程在重写AOF的过程中，新来的写命令会通过父进程进入aof-rewrite-buf，buf的命令再同步到新AOF文件中
   一般情况下不会使用RDB，会将其关掉；一般会使用AOF everysec的配置，当然要考虑具体应用场景
2. Redis学习：主从复制
   主从复制一般用作读写分离，也是Redis实现高可用、分布式的基础
   从节点一般要设置slave-read-only yes，设置不接受写命令，只允许读
   全量复制：slave发送runid offset为? -1给master，master会基于bgsave，将RDB文件传输给slave，在bgsave以及传输的过程新的写命令会进入复制缓冲，待RDB传输完后将复制缓冲的命令发送给slave，slave flushall将所有数据清空后加载新数据，master再有新的写命令会实时同步给slave，保证主从节点数据一致
   部分复制：可能因为网络一时断开的原因master无法同步写命令给slave，master会将写命令加入复制缓冲，slave节点将runid与offset发送个master，master会将复制缓冲中从offset开始到队尾的写命令发送给slave，保证主从节点数据一致（offset一致）
   主从复制中发生故障时无法实现自动故障转移，要人工或脚本介入。如果slave节点故障，对应的程序客户端就要修改redis服务地址后重启将流量打到其他slave节点，实现只读迁移；如果master节点故障，就要对其中一个slave进行slaveof no one，再对其他slave节点重新slaveof new master，同样旧master对应的程序客户端要修改redis服务地址重启，实现读写迁移

2018-02-09，星期五，深圳，多云，19°
1. Redis学习：Sentinel
   Redis Sentinel是Redis高可用读写分离的实现方案：故障发现、故障自动转移、配置中心（并非代理master）、客户端通知
   Redis Sentinel通过三个定时任务实现了Sentinel节点对主节点、从节点、其余Sentinel节点的监控
   Redis Sentinel在对节点做失败判定时分别为主观下线跟客观下线
2. Sentinel三个定时任务
   每10秒每个Sentinel对master和slave执行info：发现slave节点、确认主从关系
   每2秒每个Sentinel通过master节点的channel交换信息（发布订阅）：Sentinel集群可弹性扩容、交换自身信息和对Redis节点的看法
   每1秒每个Sentinel对其他Sentinel和Redis执行ping：心跳检测
3. 主观下线和客观下线
   主观下线：每个Sentinel节点对Redis节点失败的“偏见”
   客观下线：所有Sentinel节点对Redis节点失败“达成共识”（≥quorum）
   一般Sentinel节点数设置奇数个n，quorum = 1 + n/2
4. 故障转移（由Sentinel leader节点完成，leader的选举由Sentinel集群内自己完成）
   从slave节点中选择一个“合适”的节点作为新的master节点
   对上面的slave节点执行slaveof no one命令让其成为master节点
   向剩余的slave节点发送命令，让他们成为新master节点的slave节点，复制规则和parallel-syncs有关
   更新原来master节点配置为slave，并保持对其关注，当其恢复后命令它去复制新的master节点
5. JedisSentinelPool客户端：配合服务端实现高可用
   客户端内部启动多个线程订阅所有Sentinel节点的+switch-master channel
   当服务端故障转移完成后，Sentinel会发布更换master的消息对这个channel
   在转移期间客户端不断重试报连接错误，待收到更换master的消息后会重新初始化连接池，服务就会正常
6. 关于slave节点高可用
   注意目前JedisSentinelPool只封装了master节点的故障转移，其他语言甚至还没有Sentinel高可用的客户端，若要实现slave节点自动故障转移，需要自己封装相应的客户端，订阅来自Sentinel的+sdown与+odown相应消息

2018-02-11，星期日，深圳，大部晴朗，14°
1. Redis学习：Cluster
   分布式系统数据分布：简单hash求余分区、一致性hash分区（不求余）、虚拟槽hash分区（求余，redis的分区方式）
   Redis Cluster部署：准备节点、节点相互meet、指派槽、主从复制
   集群扩容：准备节点、meet加入集群、迁移槽和数据。其中迁移槽和数据包括准备迁移部分、循环迁移数据过程、向集群所有主节点发送setslot命令通知槽已分配个目标节点等，可使用redis-trib.rb工具简化手工操作
   集群收缩：原理与扩容相似，包括下线迁移槽、忘记节点、关闭节点等操作。使用redis-trib.rb工具简化手工操作
2. smart客户端JedisCluster：工作流程
   从集群中选一个可运行节点，使用cluster slots初始化槽和节点映射
   将cluster slots的结果映射到本地，为每个节点创建JedisPool
   执行命令：JedisCluster计算key相应的slot，再通过映射得到相应的节点连接，发送命令，如果成功则结束；如果连接出错则选取任意活跃节点发送，收到moved异常后重定向到目标节点，执行成功后刷新本地映射。这个过程最大重试次数为5次，超过重试次数就抛错（当然中间可能会有ask异常，重试即可）
3. Redis Cluster故障转移（故障发现、故障恢复）
   通过ping/pong消息实现故障发现：不需要Sentinel
   主观下线：节点1向节点2发送ping消息，若节点2回复pong消息，节点1会更新与节点2最后通信时间；若节点2没有回复，节点1还会不断定时发送ping消息，当与节点2最后通信时间超过node-timeout则标记为主观下线pfail
   客观下线：半数以上持有槽的主节点都标记某节点主观下线。ping消息带有发送方认为的pfail信息，每个主节点会维护一个故障表，这个表包含集群所有主节点认为的pfail信息。当发现某节点的pfail数超过半数，则将其标记为客观下线，并向集群广播下线节点的fail消息
   故障恢复：针对被下线主节点的所有从节点，包括资格检查（每个从节点检查与故障主节点的断线时间，过长则取消资格）、准备选举时间（offset越大准备时间越短、越快发起选举）、选举投票（获得半数以上投票）、替换主节点（slaveof no one、clusterDelSlot与clusterAddSlot、向集群广播自己的pong消息表明已经替换了故障主节点）。smart客户端会收到广播的消息，完成刷新映射与连接池重新初始化。注意：在其中一个节点发布消息（Pub/Sub），整个集群都会收到发布的消息，意味着在集群Pub/Sub其实是广播消息

2018-02-12，星期一，深圳，晴间多云，17°
1. Redis学习：缓存（目的是保护存储层、加快响应速度）
   缓存穿透问题：大量请求不命中cache，全部落到storage，cache层不再起作用。可能的原因有业务代码问题、恶意攻击等。解决方法一般是缓存“空对象”（空对象有过期时间，但需要更多的key，且cache层和storage层数据“短期”不一致）
   无底洞问题：增加机器后性能反而下降，即增加机器不代表更高的性能。可以联想到Redis Cluster各个节点要不断地ping/pong，会非常消耗网络带宽；其次mget/mset等操作只能在一个节点中执行，因此客户端要先计算CRC16、查找本地映射等后聚合同一个节点的key，再串行或并行发送对单个节点的mget/mset，增加机器而言会加大客户端的工作量（mget/mset操作还可以通过串行get/set，hash_tag等操作完成），优化手段通常为hash_tag hgetall等能在单节点执行减少网络通信的做法
   缓存热点key重建问题：高并发场景下的热点key，可能会有同时先后两个线程去读取storage刷新cache的现象。一般用redis互斥锁同步刷新cache的过程（将查询数据源与刷新缓存的过程锁住）
   缓存穿透优化与热点key重建优化：https://github.com/geekfghuang/javaproj/blob/master/redis-cluster/src/main/java/RedisCacheAbout.java
   CacheCloud：Redis云管理平台，提供Redis可视化部署、运维、监控等功能的平台，https://github.com/sohutv/cachecloud

2018-02-13，星期二，深圳，大部晴朗，15°
1. Nginx学习：高效可靠的web服务、代理中间件
   IO多路复用epoll、轻量级（功能模块少，注重核心模块、代码模块化）
   CPU亲和：一个worker进程绑定一个CPU计算核心，减少CPU切换以及切换CPU带来的cache miss
   sendfile：静态文件零拷贝
2. Nginx学习：官方模块使用
   检查配置文件语法：nginx -t -c /etc/nginx/nginx.conf
   重新加载配置文件：nginx -s reload -c /etc/nginx/nginx.conf
   http_sub_module：替换http内容
   http_limit_conn_module：并发连接数限制
   http_limit_req_module：请求频率限制（这里特指限制ip的频率，而不是总体）
   http_access_module：访问控制，黑名单、白名单，但客户端走代理后则无法控制
   http_auth_basic_module：访问控制，认证登录，用 htpasswd -c 目标文件 用户名 加入用户名密码

2018-02-14，星期三，深圳，大部多云，21°
1. Nginx学习：官方模块使用
   ngx_http_gzip_module：压缩模块，可减少网络流量的消耗，提高响应效率
2. Nginx设置http头信息：Cache-Control/Expires、Last-Modified/If-Modified-Since等
   Cache-Control：max-age=[秒]，设置静态资源在浏览器本地的缓存时间
   Expires：将来的时间点，也是设置静态资源在浏览器本地的缓存时间
   Last-Modified/If-Modified-Since：Last-Modified是由服务器往客户端发送的HTTP头，If-Modified-Since是由客户端往服务器发送的头，当浏览器再次请求本地存在的cache页面时，客户端会通过If-Modified-Since头将先前服务器端发过来的Last-Modified最后修改时间戳发送回去，让服务器端进行验证，通过这个时间戳判断客户端的页面是否是最新的，如果不是最新的，则返回新的内容，如果是最新的，则返回304告诉客户端其本地cache的页面是最新的（body为空），于是客户端直接从本地加载页面，这样在网络上传输的数据就会大大减少，同时也减轻了服务器的负担

2018-02-15，星期四，深圳，大部多云，23°
1. Nginx学习：防盗链
   通过判定http_referer头信息，防止静态资源链接被其他网站直接使用
   valid_referers none blocked 101.200.45.225;
   if ($invalid_referer) {
   	return 403;
   }
2. Nginx学习：反向代理
   proxy_pass http://127.0.0.1;
3. Nginx学习：正向代理
   如果服务器A已经通过访问控制规则（deny、allow、http_x_forward_for）限制只允许一个固定IP服务器B的访问，那么在服务器B上应该配置代理语法如下：
   resolver 8.8.8.8
   location / {
	proxy_pass http://$http_host$request_uri;
   }
   然后在客户端浏览器配置代理服务器为B即可
4. Nginx学习：正向代理与反向代理
   在Nginx中无论是正向代理还是反向代理，语法都是proxy_pass，一般还要设置proxy_set_header X-Real-IP $remote_addr;因为最终的处理服务器可能需要真实客户端的IP做一些定位、监控服务等等

2018-02-16，星期五，深圳，晴间多云，27°
1. Nginx学习：负载均衡
   upstream goload {
        server 127.0.0.1:9991;
        server 127.0.0.1:9992;
        server 127.0.0.1:9993;
   }
   proxy_pass http://goload;
   负载策略默认是等权重轮询
2. Nginx学习：调整后端服务器在负载均衡中的状态
   down：不参与负载均衡
   backup：备份服务器，当有节点可用时，不参与负载均衡
   max_fails：允许请求失败的次数
   fail_timeout：经过max_fails失败后，服务暂停的时间，该时间过后nginx会继续检查该节点是否可用
   max_conns：限制最大接收的连接数，预防后端节点性能不同，因为默认策略是等权轮询
3. Nginx学习：负载均衡策略
   轮询、加权轮询（weight），可能遇到的问题是cookie与session等不匹配，会造成掉线的情况
   ip_hash：解决了掉线的问题，但当用户走正向代理时，所有的请求都会只落到一台服务器上
   url_hash：hash $request_uri;根据/test、/{id}/info等请求url的hash值进行判定
4. Nginx学习：缓存
   缓存分为服务端缓存、客户端缓存、代理缓存，Nginx属于代理缓存
   配置proxy_cache_path、proxy_cache、proxy_cache_key等，缓存生效后如果默认策略是等权轮询，那么以后每次返回的结果会是第一次返回的结果，因为结果已经被缓存到磁盘中

2018-02-17，星期六，深圳，局部多云，22°
1. Nginx学习：动静分离提高后端核心服务性能
2. Nginx学习：Lua模块安装与简单测试
   Nginx安装Lua：https://www.imooc.com/article/19597、https://www.cnblogs.com/aoeiuv/p/6856056.html
   Nginx简单测试Lua：
   location /lua {
       default_type 'text/plain';
       content_by_lua 'ngx.say("hello, lua")';
   }
   location /myip {
       default_type 'text/plain';
       content_by_lua '
           clientIP = ngx.var.remote_addr 
           clientPort = ngx.var.remote_port
           ngx.say("IP:", clientIP, ":", clientPort)';
   }

2018-02-18，星期日，深圳，大部多云，20°
1. Nginx学习：结合Lua实现灰度发布
   location /grayscale {
       default_type "text/html";
       content_by_lua_file /root/geekfghuang/luaproj/grayscale.lua;
   }
   location @server {
       proxy_pass http://127.0.0.1:9991;
   }
   location @server_test {
       proxy_pass http://127.0.0.1:9993;
   }

   clientIP = ngx.req.get_headers()["X-Real-IP"]
   if clientIP == nil then
       clientIP = ngx.req.get_headers()["x_forwarded_for"]
   end
   if clientIP == nil then
       clientIP = ngx.var.remote_addr
   end
   --灰度发布白名单IP走@server_test，其他IP走原服务
   if clientIP == "119.123.185.177" then
       ngx.exec("@server_test")
   else
       ngx.exec("@server")
   end

   注意查看Nginx logs文件夹下的access.log、error.log等日志，用于监控访问情况、有效定位错误等

2018-02-19，星期一，深圳，晴间多云，26°
1. Nginx学习：location匹配
   =    精确匹配
   ^~   前缀匹配
   ~\~* 正则匹配（优先级低，即使匹配成功了也会继续匹配其他）
2. Nginx学习：传递用户真实IP
   在用户的第一层代理中set http头x_real_ip=$remote_addr，然后透传到最终后端服务
3. Http响应状态码
   500Internal Server Error服务器内部错误，一般是源代码有错误
   502Bad Gateway后端服务无响应，服务down掉
   503Service Unavailable可能服务器临时的过载导致无法处理请求，一段时间后会自动恢复
   504Gateway Timeout后端服务执行超时
4. 压力测试
   yum install httpd-tools
   ab -n 2000 -c 2 url
5. Nginx学习：系统与Nginx性能优化
   调整文件句柄数：系统全局性修改、用户局部性修改、进程局部性修改
   Nginx进程调整文件句柄：worker_rlimit_nofile 65535;
   NginxCPU亲和配置：worker_processes 16;worker_cpu_affinity auto;
6. Nginx学习：LNMP架构
   yum install php php-fpm php-mysql
   修改php-fpm配置文件，user、group均设为root
   php-fpm -R -D启动php-fpm
   Nginx配置php路由：
   location ~ \.php$ {
       root /root/geekfghuang/phpproj;
       fastcgi_pass 127.0.0.1:12900;
       index index.php index.html;
       fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
       include fastcgi_params;
   }

2018-02-21，星期三，深圳，阵雨，19°
1. CI框架搭建简单博客：https://github.com/geekfghuang/phpproj/tree/master/CI-blog
2. 用PHP实现一个MVC模型
   index.php为入口文件
   在入口文件中获取用户请求的controller和action
   include相应文件后，实例化一个controller对象，调用action方法
   在action中include相应模型文件并实例化模型对象，获取相关模型数据为局部变量
   在action中include相应视图文件，该视图文件可以直接使用action内的局部变量

2018-02-22，星期四，深圳，多云，14°
1. CI框架学习：简单使用
   控制器、视图的使用
   超级对象load、uri、input等属性的使用
2. CI框架学习：数据库操作（query）
   数据库类默认不加载，首先需要加载数据库类，$this->db就会被实例化赋值
   $res = $this->db->query($sql);返回对象、$res->result()返回数组，数组中是一个个对象、$res->result_array()返回二维数据，里面是关联对象，$res->row()返回第一条数据，直接是一个对象
   在insert或update或delete操作后，可以通过$this->db->affected_rows();或$this->db->insert_id();返回受影响的数据，因为前后是通过conn_id联系的，在同一个连接内才能获取，关闭或向连接池归还连接后都会被清空
3. CI框架学习：数据库操作（AR）
   //select id, name from user where id >= 3 order by id desc limit 2, 3;
   $res = $this->db->select('id, name')
        ->from('user')
        ->where('id >=', 3)
        ->limit(3, 2)//跳过2条，取出3条数据
        ->order_by('id desc')
        ->get();
   //显示最近一条SQL
   echo $this->db->last_query();
4. 一般扩展框架的方法：继承
5. CI框架学习：模型
   在application/models下新建*_model.php extends CI_Model文件，在模型层调用$this->db->get('*');return $res->result();等方法
   因为CI_Model下有如下魔术方法：
   public function __get($key) {
	return get_instance()->$key;
   }
   而get_instance()如下：
   function &get_instance() {
	return CI_Controller::get_instance();
   }
   所以，在model层能直接像controller层那样$this->db->get()等操作
   在controller层调用model层代码如下：
   $this->load->model('User_model', 'user');
   $list = $this->user->getAll();

2018-02-24，星期六，深圳，有雾，18°
1. dataV的简单实用：静态数据呈现、api方式获取数据
2. 开发Uduck日志生成器：https://github.com/geekfghuang/Uduck/tree/master/log-generator

2018-02-25，星期日，深圳，有雾，21°
1. Uduck日志生成器加入定时调度

2018-02-26，星期一，深圳，大部多云，21°
1. Flume将Uduck日志生成器生成的日志数据收集至Kafka
2. Spark Streaming从Kafka中简单消费日志数据

2018-02-27，星期二，深圳，大部晴朗，19°
1. Uduck统计城市活跃度与城市地理位置，数据接入redis
   城市活跃度dataV-api开发，大屏显示