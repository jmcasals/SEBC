
Teragen command:
time hadoop jar /opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D dfs.block.size=16777216 65536000 /user/neymar/tgen640_file

17/03/15 16:18:10 INFO client.RMProxy: Connecting to ResourceManager at ip-192-168-0-219.eu-west-1.compute.internal/192.168.0.125:8032
17/03/15 16:18:11 INFO hdfs.DFSClient: Created token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@JMCASALS.ES, renewer=yarn, realUser=, issueDate=1489512551148, maxDate=1490117351148, sequenceNumber=18, masterKeyId=8 on 192.168.0.125:8020
17/03/15 16:18:11 INFO security.TokenCache: Got dt for hdfs://ip-192-168-0-219.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 192.168.0.125:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@JMCASALS.ES, renewer=yarn, realUser=, issueDate=1489512551148, maxDate=1490117351148, sequenceNumber=18, masterKeyId=8)
17/03/15 16:18:11 INFO terasort.TeraGen: Generating 65536000 using 2
17/03/15 16:18:11 INFO mapreduce.JobSubmitter: number of splits:2
17/03/15 16:18:11 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/03/15 16:18:11 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489509798627_0005
17/03/15 16:18:11 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 192.168.0.125:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@JMCASALS.ES, renewer=yarn, realUser=, issueDate=1489512551148, maxDate=1490117351148, sequenceNumber=18, masterKeyId=8)
17/03/15 16:18:12 INFO impl.YarnClientImpl: Submitted application application_1489509798627_0005
17/03/15 16:18:12 INFO mapreduce.Job: The url to track the job: http://ip-192-168-0-219.eu-west-1.compute.internal:8088/proxy/application_1489509798627_0005/
17/03/15 16:18:12 INFO mapreduce.Job: Running job: job_1489509798627_0005
17/03/15 16:18:20 INFO mapreduce.Job: Job job_1489509798627_0005 running in uber mode : false
17/03/15 16:18:20 INFO mapreduce.Job:  map 0% reduce 0%
17/03/15 16:18:42 INFO mapreduce.Job:  map 21% reduce 0%
----------------------------
17/03/15 16:20:08 INFO mapreduce.Job:  map 100% reduce 0%
17/03/15 16:20:08 INFO mapreduce.Job: Job job_1489509798627_0005 completed successfully
17/03/15 16:20:09 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=251026
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=170
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=211646
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=211646
                Total vcore-seconds taken by all map tasks=211646
                Total megabyte-seconds taken by all map tasks=216725504
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=170
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=835
                CPU time spent (ms)=93020
                Physical memory (bytes) snapshot=360542208
                Virtual memory (bytes) snapshot=3127373824
                Total committed heap usage (bytes)=417857536
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

real    2m0.973s
user    0m6.741s
sys     0m0.266s

hdfs dfs -ls /user/neymar/tgen640_file
Found 3 items
-rw-r--r--   3 neymar supergroup          0 2017-03-15 16:29 /user/neymar/tgen640_file/_SUCCESS
-rw-r--r--   3 neymar supergroup 3276800000 2017-03-15 16:29 /user/neymar/tgen640_file/part-m-00000
-rw-r--r--   3 neymar supergroup 3276800000 2017-03-15 16:29 /user/neymar/tgen640_file/part-m-00001

