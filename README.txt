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
   bgrewriteaof�ӽ�������дAOF�Ĺ����У�������д�����ͨ�������̽���aof-rewrite-buf����buf��������ͬ�����µ�AOF�ļ���
   һ������²���ʹ��RDB���Ὣ��ص���һ���ʹ��AOF everysec�����ã���ȻҪ���Ǿ���Ӧ�ó���