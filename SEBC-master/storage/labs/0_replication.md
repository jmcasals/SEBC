
time hadoop jar /opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D dfs.block.size=33554432 100000 /tmp/test_file


time hadoop jar /opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /tmp/test_file /tmp/test_file_sort

(su hdfs)
hadoop fs -ls hdfs://192.168.161:8020/tmp/test_file_sort
hadoop distcp //192.168.161:8020/tmp/test_file_sort hdfs://192.168.0.142/tmp
