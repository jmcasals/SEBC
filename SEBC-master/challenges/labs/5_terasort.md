
$time hadoop jar /opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/neymar/tgen640_file /user/neymar/tsort640m

17/03/15 13:44:08 INFO terasort.TeraSort: starting
17/03/15 13:44:10 INFO hdfs.DFSClient: Created token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@JCASALS.ES, renewer=yarn, realUser=, issueDate=1489513450501, maxDate=1490118250501, sequenceNumber=20, masterKeyId=8 on 192.168.0.125:8020
17/03/15 13:44:10 INFO security.TokenCache: Got dt for hdfs://ip-192-168-0-219.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 192.168.0.125:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@JCASALS.ES, renewer=yarn, realUser=, issueDate=1489513450501, maxDate=1490118250501, sequenceNumber=20, masterKeyId=8)
17/03/15 13:44:10 INFO input.FileInputFormat: Total input paths to process : 2
Spent 432ms computing base-splits.
Spent 6ms computing TeraScheduler splits.
Computing input splits took 439ms
Sampling 10 splits of 392
Making 8 from 100000 sampled records
Computing parititions took 2148ms
Spent 2589ms computing partitions.
17/03/15 17:47:12 INFO client.RMProxy: Connecting to ResourceManager at ip-192-168-0-219.eu-west-1.compute.internal/192.168.0.125:8032
17/03/15 17:47:13 INFO mapreduce.JobSubmitter: number of splits:392
17/03/15 17:47:13 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489509798627_0007
17/03/15 17:47:13 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 192.168.0.125:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@JCASALS.ES, renewer=yarn, realUser=, issueDate=1489513450501, maxDate=1490118250501, sequenceNumber=20, masterKeyId=8)
17/03/15 17:47:13 INFO impl.YarnClientImpl: Submitted application application_1489509798627_0007
17/03/15 17:47:13 INFO mapreduce.Job: The url to track the job: http://ip-192-168-0-219.eu-west-1.compute.internal:8088/proxy/application_1489509798627_0007/
17/03/15 17:47:13 INFO mapreduce.Job: Running job: job_1489509798627_0007
17/03/15 17:47:22 INFO mapreduce.Job: Job job_1489509798627_0007 running in uber mode : false
17/03/15 17:47:22 INFO mapreduce.Job:  map 0% reduce 0%
17/03/15 17:47:32 INFO mapreduce.Job:  map 1% reduce 0%
17/03/15 17:47:40 INFO mapreduce.Job:  map 3% reduce 0%
...............................................
17/03/15 17:54:54 INFO mapreduce.Job:  map 100% reduce 97%
17/03/15 17:54:57 INFO mapreduce.Job:  map 100% reduce 100%
17/03/15 17:54:58 INFO mapreduce.Job: Job job_1489509798627_0007 completed successfully
17/03/15 17:54:58 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2906953865
                FILE: Number of bytes written=5800901182
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553661936
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=1200
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=392
                Launched reduce tasks=8
                Data-local map tasks=392
                Total time spent by all maps in occupied slots (ms)=3632648
                Total time spent by all reduces in occupied slots (ms)=694116
                Total time spent by all map tasks (ms)=3632648
                Total time spent by all reduce tasks (ms)=694116
                Total vcore-seconds taken by all map tasks=3632648
                Total vcore-seconds taken by all reduce tasks=694116
                Total megabyte-seconds taken by all map tasks=3719831552
                Total megabyte-seconds taken by all reduce tasks=710774784
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2843137011
                Input split bytes=61936
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2843137011
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =3136
                Failed Shuffles=0
                Merged Map outputs=3136
                GC time elapsed (ms)=52730
                CPU time spent (ms)=1484830
                Physical memory (bytes) snapshot=199892717568
                Virtual memory (bytes) snapshot=631835029504
                Total committed heap usage (bytes)=224434585600
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=6553600000
        File Output Format Counters
                Bytes Written=6553600000
17/03/15 17:54:58 INFO terasort.TeraSort: done

real    7m50.737
user    0m11.148s
sys     0m0.433s

