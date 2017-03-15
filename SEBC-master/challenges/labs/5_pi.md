kinit ronaldo@JCASALS.ES
Password for ronaldo@JCASALS.ES:
time hadoop jar /opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 4 10
Number of Maps  = 4
Samples per Map = 10
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Starting Job
17/03/15 18:59:21 INFO client.RMProxy: Connecting to ResourceManager at ip-192-168-0-125.eu-west-1.compute.internal/192.168.0.125:8032
17/03/15 18:59:21 INFO hdfs.DFSClient: Created token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@JCASALS.ES, renewer=yarn, realUser=, issueDate=1489514181565, maxDate=1490118981565, sequenceNumber=22, masterKeyId=8 on 192.168.0.125:8020
17/03/15 18:59:21 INFO security.TokenCache: Got dt for hdfs://ip-192-168-0-125.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 192.168.0.125:8020, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@JCASALS.ES, renewer=yarn, realUser=, issueDate=1489514181565, maxDate=1490118981565, sequenceNumber=22, masterKeyId=8)
17/03/15 18:59:21 INFO input.FileInputFormat: Total input paths to process : 4
17/03/15 18:59:21 INFO mapreduce.JobSubmitter: number of splits:4
17/03/15 18:59:21 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489509798627_0009
17/03/15 18:59:21 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 192.168.0.125:8020, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@JCASALS.ES, renewer=yarn, realUser=, issueDate=1489514181565, maxDate=1490118981565, sequenceNumber=22, masterKeyId=8)
17/03/15 18:59:22 INFO impl.YarnClientImpl: Submitted application application_1489509798627_0009
17/03/15 18:59:22 INFO mapreduce.Job: The url to track the job: http://ip-192-168-0-125.eu-west-1.compute.internal:8088/proxy/application_1489509798627_0009/
17/03/15 18:59:22 INFO mapreduce.Job: Running job: job_1489509798627_0009
17/03/15 18:59:30 INFO mapreduce.Job: Job job_1489509798627_0009 running in uber mode : false
17/03/15 18:59:30 INFO mapreduce.Job:  map 0% reduce 0%
17/03/15 18:59:35 INFO mapreduce.Job:  map 25% reduce 0%
17/03/15 18:59:43 INFO mapreduce.Job:  map 100% reduce 0%
17/03/15 18:59:49 INFO mapreduce.Job:  map 100% reduce 100%
17/03/15 18:59:49 INFO mapreduce.Job: Job job_1489509798627_0009 completed successfully
17/03/15 18:59:49 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=65
                FILE: Number of bytes written=631195
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1200
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=19
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=4
                Launched reduce tasks=1
                Data-local map tasks=4
                Total time spent by all maps in occupied slots (ms)=36972
                Total time spent by all reduces in occupied slots (ms)=3357
                Total time spent by all map tasks (ms)=36972
                Total time spent by all reduce tasks (ms)=3357
                Total vcore-seconds taken by all map tasks=36972
                Total vcore-seconds taken by all reduce tasks=3357
                Total megabyte-seconds taken by all map tasks=37859328
                Total megabyte-seconds taken by all reduce tasks=3437568
        Map-Reduce Framework
                Map input records=4
                Map output records=8
                Map output bytes=72
                Map output materialized bytes=135
                Input split bytes=728
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=135
                Reduce input records=8
                Reduce output records=0
                Spilled Records=16
                Shuffled Maps =4
                Failed Shuffles=0
                Merged Map outputs=4
                GC time elapsed (ms)=263
                CPU time spent (ms)=3460
                Physical memory (bytes) snapshot=2243837952
                Virtual memory (bytes) snapshot=7939981312
                Total committed heap usage (bytes)=2465202176
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=472
        File Output Format Counters
                Bytes Written=97
Job Finished in 29.123 seconds
Estimated value of Pi is 3.40000000000000000000

real    0m31.477s
user    0m5.999s
sys 0m0.295s
