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