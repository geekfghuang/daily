2018-01-24�������������ڣ�����
1. Sparkѧϰ���������������������wordcount����
   RDDs����������Transformations��Actions 
   RDDs�����ԣ�Ѫͳ��ϵͼ���ӳټ��� 
   KeyValue��RDDs���ص�combineByKey

2018-01-25�������ģ����ڣ��󲿶���
1. ������ʶʵʱ������Ӧ�ó���������ѡ�ͣ�Spark Streaming��Storm����
2. ѧϰ�ֲ�ʽ��־�ռ����Flume���������ܹ�
   ���һ���ļ�ʵʱ�ɼ��������������������̨
   ��A�������ϵ���־ʵʱ�ɼ���B������

2018-01-26�������壬���ڣ��ֲ�����
1. �ֲ�ʽ����������ϢϵͳKafkaѧϰ���ܹ������ĸ���
   ���ڵ㵥broker���𡢵��ڵ��broker����
   �ݴ��Բ��������
   ����Flume(1.8.0)��Kafka���ʵʱ���ݲɼ���exec-memory-avro -> avro-memory-kafka

2018-01-27�������������ڣ���ǰ����
1. Spark Streaming���ţ���������Ƶͳ������
   spark-submit�ύjar����ʽ���д�Ƶͳ��
   spark-shell��̷�ʽ��scala�����д�Ƶͳ��
   nc��ʽ�ύԴ����
2. �ֱ�Ӵ֡�ϸ�������Spark Streaming����ԭ��

2018-01-28�������գ����ڣ�����
1. ѧϰSpark Streaming���ĸ������̣�IDEA���̡�scala��
   StreamingContext��DStream��InputDStreams��Receivers
   Transformations��OutPutOperations
   Spark Streaming����socket����
   Spark Streaming�����ļ�ϵͳ��hdfs/local������

2018-01-29������һ�����ڣ��󲿶���
1. Spark Streaming��������
   foreach��ͳ�ƽ�����MySQL��connection���л����⡢��������
   ���ں����������ʹ�ã����ڳ��ȡ���������
   ���������ˣ�transform��leftOuterJoin��filter��map
2. Spark Streaming����Flume��̣�Flume��ȡPush��ʽ
   Spark Streaming���������䵱avro source agent�Ľ�ɫA���򿪶˿ڽ������ݣ�
   Flume����������avro sinkָ��A
   mvn���scalaԴ��Ϊjar����spark-submit --packages �ⲿ����jar ��ʽ�ύ������ҵ

2018-01-30�����ڶ������ڣ�����
1. Spark Streaming����Flume��̣�Streaming��ȡPull��ʽ
   Flume���jar���汾׼ȷ����
   Pullʹ��һ���ɿ���receiver�һ�������ķ�ʽ��Flume sink��������ȡ����
   �����ݱ�Streaming�����Ҹ�������������ִ�гɹ�

2018-01-31�������������ڣ�����
1. Spark Streaming����Kafka��̣�����Receiver��ʽ
   Streaming����Receiver Job����Kafka�����ݣ��洢��Executor���ڴ棩��
   ��������WALs�ķ�ʽ��߹����ݴ�����
2. Spark Streaming����Kafka��̣�����Direct��ʽ
   ��עDirect��Receiver���ַ�ʽ��Kafka��ȡ���ݵ��ڲ�ϸ�ڡ���������ȱ��

2018-02-01�������ģ����ڣ��󲿶���
1. ����Flume��Kafka��Spark Streaming��ʵ��ͨ��������ƽ̨
   log4j����־�����Flume avro source
   ��־����Flume Kafka sink���������Kafka
   Spark Streaming��ȡKafka����־���������㴦��

2018-02-02�������壬���ڣ��󲿶���
1. ��Python�����û�������Ϊ��־������������crontab��ʱ���Ȳ�����־
2. Flume�ռ���������־��Kafka��Spark Streaming��Kafka������־����
   Spark Streaming Scala��̽����յ�����־���ݽ�����ϴ��ת����ʽ�����˵�
   RDDs Scala����ٶ���Ϥ����������ϴ���˾���ĸ���

2018-02-03�������������ڣ��ֲ�����
1. ����ϴ�����˺�ķ�����־������ӦRDDsת���õ����쵽����Ϊֹ������Ŀ�ķ��ʴ���ͳ�ƽ��
2. ��ͳ�ƽ����⵽HBase
   ��Scala�е���Java������Java����һ��Thrift��Go����Go������HBase Thrift��������
   Ϊ�˱���Java HBase�ӿ�Deprecated�Լ�Java HBase Client�汾�������鷳���м��һ��Thrift����Go���µ�HBase Thrift Client����HBase

2018-02-04�������գ����ڣ�������
1. ����ϴ�����˺�ķ�����־������ӦRDDsת���õ����쵽����Ϊֹ������������������������Ŀ�ķ��ʴ���ͳ�ƽ��
2. Go����ͳ�ƽ����⵽HBaseʱ�������⣬�����������£�
   �������var HBaseClient *hbase.THBaseServiceClient�ᱨEOF�ȴ��󣬽���ĳ�ÿ����һ��������������һ��HBaseClient���󣨾ֲ�������������
   �����Ƽ򵥶�����ʷ��������ݿ����Ӷ���RPC Client����ȶ��̹߳�����ʵľ���ϸ���Լ��������ݷ��ظ�ʽϸ�ڣ��д��о�
3. �������ӻ��ı�Ҫ�ԣ���ģ�������󵽾��塢����Ĺ��̣������ҵ����Ч��
   ECharts�ļ�ʹ�ã���״ͼ����ͼ

2018-02-05������һ�����ڣ�������
1. EChartsǰ��ajax�Ӻ����ȡjson���������ӻ�����
2. DataV���ӻ���ܵļ�ʶ��ͨ������MySQL����Դ��SQL��䡢���ʱ��ȣ������ݴӺ����ȡ�����ӻ�����
3. Scala��Java��Python������дSpark������ҵ����Scala����������
   Scala������Java�໥���ã�Scalaд������ҵʱ��һЩ����Java��⺯������ֱ�ӵ���

2018-02-06�����ڶ������ڣ������ƣ�14��
1. Scala������ƻ���ѧϰ
   ����ʽ���˼�롢Scala���Ի���
   β�ݹ��Ż���ͨ�ݹ麯�����������ջ�������
   �õݹ�˼��+����ʽ��̵ķ�ʽ4�д���ʵ�ֿ�������
2. Redisѧϰ��Redis��ʶ&��ϰ���������ݽṹ
   ���̡߳�ԭ���ԣ�Redis��һ��˲��ֻ��ִ��һ����������ڷֲ�ʽID������
   epoll IO��·����ģ�ͣ����ͻ��������ļ�������readyʱ����������д��
   string��set��set nx|xx|ex��incr��incrby��

2018-02-07�������������ڣ������ƣ�15��
1. Redisѧϰ���������ݽṹ
   hash��key field value������ȹ�ϵ�����ݿ⣬������field��ttl���Կ��ƣ���ͨ�������߼�����
   list������ʵ�֣�����Ϊ����Ϣ���У�brpop key timeout���������ȴ�
   set��sadd��smembers��spop���������һ��Ԫ�أ���sinter����ͬ��ע����sdiff��sunion [store destkey]
   ���򼯺�zset��Ĭ�ϴ�С����zadd��zincrby��zrange��zrangebyscore���������а�ʵ��
   ����ѯslowlog���������������ڵĵ������׶Σ�����������ѯ���г��ȡ�����ѯʱ����ֵ
   ��ˮ��pipeline��1������+n��������������ʱ����ᱻ��ֿ�����˲���ԭ�Ӳ�������mget��mset�ȶ���ԭ�Ӳ���
   �������ģ�channel��ģʽ���ַ�ʽ��channel���ֵ䣬ģʽ������ÿpublishһ����Ϣ����channel�ֵ���ȡ���ͻ��˷�����Ϣ��Ȼ�����ģʽ�������ģʽ��channelƥ�䣬����
   ������������Ϣ���в�ͬ���ǣ��������Ĳ���ѻ���ʷ��Ϣ
   bitmap��������ʵΪstring�����512MB��һ��������λ������ʹ��ǡ���ɽ�ʡ�ڴ�
   hyperloglog�����ʻ���string����������pfadd��pfcount��pfmerge��һ������ͳ�ƶ����û������ȣ����Ƚ�ʡ�ڴ棬��������ݲ�����15KB���ҵ��ڴ档����0.81%�Ĵ����ʣ����޷�ȡ����������
   geo��geoadd��geopos��geodist������ɼ����������У���γ�ȣ��ľ��룬��Բ���ٹ����ڵ�Զ�����еȣ��ײ�Ϊzset

2018-02-08�������ģ����ڣ������ƣ�17��
1. Redisѧϰ���־û�
   RDB���գ�save�������Ŷӵ��������bgsave��������fork�����ӽ������ڳ־û�����fork�Ǻܿ�ģ��Ŷӵ������������������save 60 10000�����ö��ǻ���bgsaveʵ��
   RDB���ڵ����⣺��ʱ�����ܣ�O(n)ʱ�临�Ӷȡ�fork()�����ڴ棩�����׶�ʧ���ݣ�save���ã�
   AOF��appendonly yes��appendfsync everysec��alwaysÿ��д����ӻ�����ˢ�µ�Ӳ�̡�everysecÿ�뽫���������д����ˢ�µ�Ӳ�̡�no���ɿأ���OS����ˢ�µ�Ӳ�̵�ʱ��
   AOF��д��bgrewriteaof��������AOF��д���ã����ڴ����Ż�д���AOF�ļ��У�ע�Ⲣ���Ƕ���ԭ��AOF�ļ����Ż�����ԭ��AOF incr count��incr count��incr count����д��AOF set count 3
   bgrewriteaof�ӽ�������дAOF�Ĺ����У�������д�����ͨ�������̽���aof-rewrite-buf��buf��������ͬ������AOF�ļ���
   һ������²���ʹ��RDB���Ὣ��ص���һ���ʹ��AOF everysec�����ã���ȻҪ���Ǿ���Ӧ�ó���
2. Redisѧϰ�����Ӹ���
   ���Ӹ���һ��������д���룬Ҳ��Redisʵ�ָ߿��á��ֲ�ʽ�Ļ���
   �ӽڵ�һ��Ҫ����slave-read-only yes�����ò�����д���ֻ�����
   ȫ�����ƣ�slave����runid offsetΪ? -1��master��master�����bgsave����RDB�ļ������slave����bgsave�Լ�����Ĺ����µ�д�������븴�ƻ��壬��RDB������󽫸��ƻ��������͸�slave��slave flushall������������պ���������ݣ�master�����µ�д�����ʵʱͬ����slave����֤���ӽڵ�����һ��
   ���ָ��ƣ�������Ϊ����һʱ�Ͽ���ԭ��master�޷�ͬ��д�����slave��master�Ὣд������븴�ƻ��壬slave�ڵ㽫runid��offset���͸�master��master�Ὣ���ƻ����д�offset��ʼ����β��д����͸�slave����֤���ӽڵ�����һ�£�offsetһ�£�
   ���Ӹ����з�������ʱ�޷�ʵ���Զ�����ת�ƣ�Ҫ�˹���ű����롣���slave�ڵ���ϣ���Ӧ�ĳ���ͻ��˾�Ҫ�޸�redis�����ַ������������������slave�ڵ㣬ʵ��ֻ��Ǩ�ƣ����master�ڵ���ϣ���Ҫ������һ��slave����slaveof no one���ٶ�����slave�ڵ�����slaveof new master��ͬ����master��Ӧ�ĳ���ͻ���Ҫ�޸�redis�����ַ������ʵ�ֶ�дǨ��

2018-02-09�������壬���ڣ����ƣ�19��
1. Redisѧϰ��Sentinel
   Redis Sentinel��Redis�߿��ö�д�����ʵ�ַ��������Ϸ��֡������Զ�ת�ơ��������ģ����Ǵ���master�����ͻ���֪ͨ
   Redis Sentinelͨ��������ʱ����ʵ����Sentinel�ڵ�����ڵ㡢�ӽڵ㡢����Sentinel�ڵ�ļ��
   Redis Sentinel�ڶԽڵ���ʧ���ж�ʱ�ֱ�Ϊ�������߸��͹�����
2. Sentinel������ʱ����
   ÿ10��ÿ��Sentinel��master��slaveִ��info������slave�ڵ㡢ȷ�����ӹ�ϵ
   ÿ2��ÿ��Sentinelͨ��master�ڵ��channel������Ϣ���������ģ���Sentinel��Ⱥ�ɵ������ݡ�����������Ϣ�Ͷ�Redis�ڵ�Ŀ���
   ÿ1��ÿ��Sentinel������Sentinel��Redisִ��ping���������
3. �������ߺͿ͹�����
   �������ߣ�ÿ��Sentinel�ڵ��Redis�ڵ�ʧ�ܵġ�ƫ����
   �͹����ߣ�����Sentinel�ڵ��Redis�ڵ�ʧ�ܡ���ɹ�ʶ������quorum��
   һ��Sentinel�ڵ�������������n��quorum = 1 + n/2
4. ����ת�ƣ���Sentinel leader�ڵ���ɣ�leader��ѡ����Sentinel��Ⱥ���Լ���ɣ�
   ��slave�ڵ���ѡ��һ�������ʡ��Ľڵ���Ϊ�µ�master�ڵ�
   �������slave�ڵ�ִ��slaveof no one���������Ϊmaster�ڵ�
   ��ʣ���slave�ڵ㷢����������ǳ�Ϊ��master�ڵ��slave�ڵ㣬���ƹ����parallel-syncs�й�
   ����ԭ��master�ڵ�����Ϊslave�������ֶ����ע������ָ���������ȥ�����µ�master�ڵ�
5. JedisSentinelPool�ͻ��ˣ���Ϸ����ʵ�ָ߿���
   �ͻ����ڲ���������̶߳�������Sentinel�ڵ��+switch-master channel
   ������˹���ת����ɺ�Sentinel�ᷢ������master����Ϣ�����channel
   ��ת���ڼ�ͻ��˲������Ա����Ӵ��󣬴��յ�����master����Ϣ������³�ʼ�����ӳأ�����ͻ�����
6. ����slave�ڵ�߿���
   ע��ĿǰJedisSentinelPoolֻ��װ��master�ڵ�Ĺ���ת�ƣ���������������û��Sentinel�߿��õĿͻ��ˣ���Ҫʵ��slave�ڵ��Զ�����ת�ƣ���Ҫ�Լ���װ��Ӧ�Ŀͻ��ˣ���������Sentinel��+sdown��+odown��Ӧ��Ϣ

2018-02-11�������գ����ڣ������ʣ�14��
1. Redisѧϰ��Cluster
   �ֲ�ʽϵͳ���ݷֲ�����hash���������һ����hash�����������ࣩ�������hash���������࣬redis�ķ�����ʽ��
   Redis Cluster����׼���ڵ㡢�ڵ��໥meet��ָ�ɲۡ����Ӹ���
   ��Ⱥ���ݣ�׼���ڵ㡢meet���뼯Ⱥ��Ǩ�Ʋۺ����ݡ�����Ǩ�Ʋۺ����ݰ���׼��Ǩ�Ʋ��֡�ѭ��Ǩ�����ݹ��̡���Ⱥ�������ڵ㷢��setslot����֪ͨ���ѷ����Ŀ��ڵ�ȣ���ʹ��redis-trib.rb���߼��ֹ�����
   ��Ⱥ������ԭ�����������ƣ���������Ǩ�Ʋۡ����ǽڵ㡢�رսڵ�Ȳ�����ʹ��redis-trib.rb���߼��ֹ�����
2. smart�ͻ���JedisCluster����������
   �Ӽ�Ⱥ��ѡһ�������нڵ㣬ʹ��cluster slots��ʼ���ۺͽڵ�ӳ��
   ��cluster slots�Ľ��ӳ�䵽���أ�Ϊÿ���ڵ㴴��JedisPool
   ִ�����JedisCluster����key��Ӧ��slot����ͨ��ӳ��õ���Ӧ�Ľڵ����ӣ������������ɹ��������������ӳ�����ѡȡ�����Ծ�ڵ㷢�ͣ��յ�moved�쳣���ض���Ŀ��ڵ㣬ִ�гɹ���ˢ�±���ӳ�䡣�������������Դ���Ϊ5�Σ��������Դ������״���Ȼ�м���ܻ���ask�쳣�����Լ��ɣ�
3. Redis Cluster����ת�ƣ����Ϸ��֡����ϻָ���
   ͨ��ping/pong��Ϣʵ�ֹ��Ϸ��֣�����ҪSentinel
   �������ߣ��ڵ�1��ڵ�2����ping��Ϣ�����ڵ�2�ظ�pong��Ϣ���ڵ�1�������ڵ�2���ͨ��ʱ�䣻���ڵ�2û�лظ����ڵ�1���᲻�϶�ʱ����ping��Ϣ������ڵ�2���ͨ��ʱ�䳬��node-timeout����Ϊ��������pfail
   �͹����ߣ��������ϳ��в۵����ڵ㶼���ĳ�ڵ��������ߡ�ping��Ϣ���з��ͷ���Ϊ��pfail��Ϣ��ÿ�����ڵ��ά��һ�����ϱ�����������Ⱥ�������ڵ���Ϊ��pfail��Ϣ��������ĳ�ڵ��pfail������������������Ϊ�͹����ߣ�����Ⱥ�㲥���߽ڵ��fail��Ϣ
   ���ϻָ�����Ա��������ڵ�����дӽڵ㣬�����ʸ��飨ÿ���ӽڵ�����������ڵ�Ķ���ʱ�䣬������ȡ���ʸ񣩡�׼��ѡ��ʱ�䣨offsetԽ��׼��ʱ��Խ�̡�Խ�췢��ѡ�٣���ѡ��ͶƱ����ð�������ͶƱ�����滻���ڵ㣨slaveof no one��clusterDelSlot��clusterAddSlot����Ⱥ�㲥�Լ���pong��Ϣ�����Ѿ��滻�˹������ڵ㣩��smart�ͻ��˻��յ��㲥����Ϣ�����ˢ��ӳ�������ӳ����³�ʼ����ע�⣺������һ���ڵ㷢����Ϣ��Pub/Sub����������Ⱥ�����յ���������Ϣ����ζ���ڼ�ȺPub/Sub��ʵ�ǹ㲥��Ϣ

2018-02-12������һ�����ڣ������ƣ�17��
1. Redisѧϰ�����棨Ŀ���Ǳ����洢�㡢�ӿ���Ӧ�ٶȣ�
   ���洩͸���⣺������������cache��ȫ���䵽storage��cache�㲻�������á����ܵ�ԭ����ҵ��������⡢���⹥���ȡ��������һ���ǻ��桰�ն��󡱣��ն����й���ʱ�䣬����Ҫ�����key����cache���storage�����ݡ����ڡ���һ�£�
   �޵׶����⣺���ӻ��������ܷ����½��������ӻ�����������ߵ����ܡ��������뵽Redis Cluster�����ڵ�Ҫ���ϵ�ping/pong����ǳ���������������mget/mset�Ȳ���ֻ����һ���ڵ���ִ�У���˿ͻ���Ҫ�ȼ���CRC16�����ұ���ӳ��Ⱥ�ۺ�ͬһ���ڵ��key���ٴ��л��з��ͶԵ����ڵ��mget/mset�����ӻ������Ի�Ӵ�ͻ��˵Ĺ�������mget/mset����������ͨ������get/set��hash_tag�Ȳ�����ɣ����Ż��ֶ�ͨ��Ϊhash_tag hgetall�����ڵ��ڵ�ִ�м�������ͨ�ŵ�����
   �����ȵ�key�ؽ����⣺�߲��������µ��ȵ�key�����ܻ���ͬʱ�Ⱥ������߳�ȥ��ȡstorageˢ��cache������һ����redis������ͬ��ˢ��cache�Ĺ��̣�����ѯ����Դ��ˢ�»���Ĺ�����ס��
   ���洩͸�Ż����ȵ�key�ؽ��Ż���https://github.com/geekfghuang/javaproj/blob/master/redis-cluster/src/main/java/RedisCacheAbout.java
   CacheCloud��Redis�ƹ���ƽ̨���ṩRedis���ӻ�������ά����صȹ��ܵ�ƽ̨��https://github.com/sohutv/cachecloud

2018-02-13�����ڶ������ڣ������ʣ�15��
1. Nginxѧϰ����Ч�ɿ���web���񡢴����м��
   IO��·����epoll��������������ģ���٣�ע�غ���ģ�顢����ģ�黯��
   CPU�׺ͣ�һ��worker���̰�һ��CPU������ģ�����CPU�л��Լ��л�CPU������cache miss
   sendfile����̬�ļ��㿽��
2. Nginxѧϰ���ٷ�ģ��ʹ��
   ��������ļ��﷨��nginx -t -c /etc/nginx/nginx.conf
   ���¼��������ļ���nginx -s reload -c /etc/nginx/nginx.conf
   http_sub_module���滻http����
   http_limit_conn_module����������������
   http_limit_req_module������Ƶ�����ƣ�������ָ����ip��Ƶ�ʣ����������壩
   http_access_module�����ʿ��ƣ��������������������ͻ����ߴ�������޷�����
   http_auth_basic_module�����ʿ��ƣ���֤��¼���� htpasswd -c Ŀ���ļ� �û��� �����û�������

2018-02-14�������������ڣ��󲿶��ƣ�21��
1. Nginxѧϰ���ٷ�ģ��ʹ��
   ngx_http_gzip_module��ѹ��ģ�飬�ɼ����������������ģ������ӦЧ��
2. Nginx����httpͷ��Ϣ��Cache-Control/Expires��Last-Modified/If-Modified-Since��
   Cache-Control��max-age=[��]�����þ�̬��Դ����������صĻ���ʱ��
   Expires��������ʱ��㣬Ҳ�����þ�̬��Դ����������صĻ���ʱ��
   Last-Modified/If-Modified-Since��Last-Modified���ɷ��������ͻ��˷��͵�HTTPͷ��If-Modified-Since���ɿͻ��������������͵�ͷ����������ٴ����󱾵ش��ڵ�cacheҳ��ʱ���ͻ��˻�ͨ��If-Modified-Sinceͷ����ǰ�������˷�������Last-Modified����޸�ʱ������ͻ�ȥ���÷������˽�����֤��ͨ�����ʱ����жϿͻ��˵�ҳ���Ƿ������µģ�����������µģ��򷵻��µ����ݣ���������µģ��򷵻�304���߿ͻ����䱾��cache��ҳ�������µģ�bodyΪ�գ������ǿͻ���ֱ�Ӵӱ��ؼ���ҳ�棬�����������ϴ�������ݾͻ�����٣�ͬʱҲ�����˷������ĸ���

2018-02-15�������ģ����ڣ��󲿶��ƣ�23��
1. Nginxѧϰ��������
   ͨ���ж�http_refererͷ��Ϣ����ֹ��̬��Դ���ӱ�������վֱ��ʹ��
   valid_referers none blocked 101.200.45.225;
   if ($invalid_referer) {
   	return 403;
   }
2. Nginxѧϰ���������
   proxy_pass http://127.0.0.1;
3. Nginxѧϰ���������
   ���������A�Ѿ�ͨ�����ʿ��ƹ���deny��allow��http_x_forward_for������ֻ����һ���̶�IP������B�ķ��ʣ���ô�ڷ�����B��Ӧ�����ô����﷨���£�
   resolver 8.8.8.8
   location / {
	proxy_pass http://$http_host$request_uri;
   }
   Ȼ���ڿͻ�����������ô��������ΪB����
4. Nginxѧϰ����������뷴�����
   ��Nginx����������������Ƿ�������﷨����proxy_pass��һ�㻹Ҫ����proxy_set_header X-Real-IP $remote_addr;��Ϊ���յĴ��������������Ҫ��ʵ�ͻ��˵�IP��һЩ��λ����ط���ȵ�

2018-02-16�������壬���ڣ������ƣ�27��
1. Nginxѧϰ�����ؾ���
   upstream goload {
        server 127.0.0.1:9991;
        server 127.0.0.1:9992;
        server 127.0.0.1:9993;
   }
   proxy_pass http://goload;
   ���ز���Ĭ���ǵ�Ȩ����ѯ
2. Nginxѧϰ��������˷������ڸ��ؾ����е�״̬
   down�������븺�ؾ���
   backup�����ݷ����������нڵ����ʱ�������븺�ؾ���
   max_fails����������ʧ�ܵĴ���
   fail_timeout������max_failsʧ�ܺ󣬷�����ͣ��ʱ�䣬��ʱ�����nginx��������ýڵ��Ƿ����
   max_conns�����������յ���������Ԥ����˽ڵ����ܲ�ͬ����ΪĬ�ϲ����ǵ�Ȩ��ѯ
3. Nginxѧϰ�����ؾ������
   ��ѯ����Ȩ��ѯ��weight��������������������cookie��session�Ȳ�ƥ�䣬����ɵ��ߵ����
   ip_hash������˵��ߵ����⣬�����û����������ʱ�����е����󶼻�ֻ�䵽һ̨��������
   url_hash��hash $request_uri;����/test��/{id}/info������url��hashֵ�����ж�
4. Nginxѧϰ������
   �����Ϊ����˻��桢�ͻ��˻��桢�����棬Nginx���ڴ�����
   ����proxy_cache_path��proxy_cache��proxy_cache_key�ȣ�������Ч�����Ĭ�ϲ����ǵ�Ȩ��ѯ����ô�Ժ�ÿ�η��صĽ�����ǵ�һ�η��صĽ������Ϊ����Ѿ������浽������

2018-02-17�������������ڣ��ֲ����ƣ�22��
1. Nginxѧϰ������������ߺ�˺��ķ�������
2. Nginxѧϰ��Luaģ�鰲װ��򵥲���
   Nginx��װLua��https://www.imooc.com/article/19597��https://www.cnblogs.com/aoeiuv/p/6856056.html
   Nginx�򵥲���Lua��
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

2018-02-18�������գ����ڣ��󲿶��ƣ�20��
1. Nginxѧϰ�����Luaʵ�ֻҶȷ���
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
   --�Ҷȷ���������IP��@server_test������IP��ԭ����
   if clientIP == "119.123.185.177" then
       ngx.exec("@server_test")
   else
       ngx.exec("@server")
   end

   ע��鿴Nginx logs�ļ����µ�access.log��error.log����־�����ڼ�ط����������Ч��λ�����

2018-02-19������һ�����ڣ������ƣ�26��
1. Nginxѧϰ��locationƥ��
   =    ��ȷƥ��
   ^~   ǰ׺ƥ��
   ~\~* ����ƥ�䣨���ȼ��ͣ���ʹƥ��ɹ���Ҳ�����ƥ��������
2. Nginxѧϰ�������û���ʵIP
   ���û��ĵ�һ�������set httpͷx_real_ip=$remote_addr��Ȼ��͸�������պ�˷���
3. Http��Ӧ״̬��
   500Internal Server Error�������ڲ�����һ����Դ�����д���
   502Bad Gateway��˷�������Ӧ������down��
   503Service Unavailable���ܷ�������ʱ�Ĺ��ص����޷���������һ��ʱ�����Զ��ָ�
   504Gateway Timeout��˷���ִ�г�ʱ
4. ѹ������
   yum install httpd-tools
   ab -n 2000 -c 2 url
5. Nginxѧϰ��ϵͳ��Nginx�����Ż�
   �����ļ��������ϵͳȫ�����޸ġ��û��ֲ����޸ġ����ֲ̾����޸�
   Nginx���̵����ļ������worker_rlimit_nofile 65535;
   NginxCPU�׺����ã�worker_processes 16;worker_cpu_affinity auto;
6. Nginxѧϰ��LNMP�ܹ�
   yum install php php-fpm php-mysql
   �޸�php-fpm�����ļ���user��group����Ϊroot
   php-fpm -R -D����php-fpm
   Nginx����php·�ɣ�
   location ~ \.php$ {
       root /root/geekfghuang/phpproj;
       fastcgi_pass 127.0.0.1:12900;
       index index.php index.html;
       fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
       include fastcgi_params;
   }

2018-02-21�������������ڣ����꣬19��
1. CI��ܴ�򵥲��ͣ�https://github.com/geekfghuang/phpproj/tree/master/CI-blog
2. ��PHPʵ��һ��MVCģ��
   index.phpΪ����ļ�
   ������ļ��л�ȡ�û������controller��action
   include��Ӧ�ļ���ʵ����һ��controller���󣬵���action����
   ��action��include��Ӧģ���ļ���ʵ����ģ�Ͷ��󣬻�ȡ���ģ������Ϊ�ֲ�����
   ��action��include��Ӧ��ͼ�ļ�������ͼ�ļ�����ֱ��ʹ��action�ڵľֲ�����

2018-02-22�������ģ����ڣ����ƣ�14��
1. CI���ѧϰ����ʹ��
   ����������ͼ��ʹ��
   ��������load��uri��input�����Ե�ʹ��
2. CI���ѧϰ�����ݿ������query��
   ���ݿ���Ĭ�ϲ����أ�������Ҫ�������ݿ��࣬$this->db�ͻᱻʵ������ֵ
   $res = $this->db->query($sql);���ض���$res->result()�������飬��������һ��������$res->result_array()���ض�ά���ݣ������ǹ�������$res->row()���ص�һ�����ݣ�ֱ����һ������
   ��insert��update��delete�����󣬿���ͨ��$this->db->affected_rows();��$this->db->insert_id();������Ӱ������ݣ���Ϊǰ����ͨ��conn_id��ϵ�ģ���ͬһ�������ڲ��ܻ�ȡ���رջ������ӳع黹���Ӻ󶼻ᱻ���
3. CI���ѧϰ�����ݿ������AR��
   //select id, name from user where id >= 3 order by id desc limit 2, 3;
   $res = $this->db->select('id, name')
        ->from('user')
        ->where('id >=', 3)
        ->limit(3, 2)//����2����ȡ��3������
        ->order_by('id desc')
        ->get();
   //��ʾ���һ��SQL
   echo $this->db->last_query();
4. һ����չ��ܵķ������̳�
5. CI���ѧϰ��ģ��
   ��application/models���½�*_model.php extends CI_Model�ļ�����ģ�Ͳ����$this->db->get('*');return $res->result();�ȷ���
   ��ΪCI_Model��������ħ��������
   public function __get($key) {
	return get_instance()->$key;
   }
   ��get_instance()���£�
   function &get_instance() {
	return CI_Controller::get_instance();
   }
   ���ԣ���model����ֱ����controller������$this->db->get()�Ȳ���
   ��controller�����model��������£�
   $this->load->model('User_model', 'user');
   $list = $this->user->getAll();

2018-02-24�������������ڣ�����18��
1. dataV�ļ�ʵ�ã���̬���ݳ��֡�api��ʽ��ȡ����
2. ����Uduck��־��������https://github.com/geekfghuang/Uduck/tree/master/log-generator

2018-02-25�������գ����ڣ�����21��
1. Uduck��־���������붨ʱ����

2018-02-26������һ�����ڣ��󲿶��ƣ�21��
1. Flume��Uduck��־���������ɵ���־�����ռ���Kafka
2. Spark Streaming��Kafka�м�������־����

2018-02-27�����ڶ������ڣ������ʣ�19��
1. Uduckͳ�Ƴ��л�Ծ������е���λ�ã����ݽ���redis
   ���л�Ծ��dataV-api������������ʾ