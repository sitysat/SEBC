Run the terasort program as raffles using /user/raffles/tgen512m
```
[raffles@ip-172-31-3-217 root]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort /user/raffles/tgen512m tsort512m
16/12/08 22:26:22 INFO terasort.TeraSort: starting
16/12/08 22:26:23 INFO hdfs.DFSClient: Created token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@SITYSAT.SG, renewer=yarn, realUser=, issueDate=1481253983744, maxDate=1481858783744, sequenceNumber=1, masterKeyId=2 on 172.31.3.217:8020
16/12/08 22:26:23 INFO security.TokenCache: Got dt for hdfs://ip-172-31-3-217.ap-southeast-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.3.217:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@SITYSAT.SG, renewer=yarn, realUser=, issueDate=1481253983744, maxDate=1481858783744, sequenceNumber=1, masterKeyId=2)
16/12/08 22:26:23 INFO input.FileInputFormat: Total input paths to process : 1
Spent 287ms computing base-splits.
Spent 3ms computing TeraScheduler splits.
Computing input splits took 290ms
Sampling 10 splits of 77
Making 6 from 100000 sampled records
Computing parititions took 771ms
Spent 1064ms computing partitions.
16/12/08 22:26:24 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-3-218.ap-southeast-1.compute.internal/172.31.3.218:8032
16/12/08 22:26:25 INFO mapreduce.JobSubmitter: number of splits:77
16/12/08 22:26:25 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1481253470973_0001
16/12/08 22:26:25 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.3.217:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@SITYSAT.SG, renewer=yarn, realUser=, issueDate=1481253983744, maxDate=1481858783744, sequenceNumber=1, masterKeyId=2)
16/12/08 22:26:26 INFO impl.YarnClientImpl: Submitted application application_1481253470973_0001
16/12/08 22:26:26 INFO mapreduce.Job: The url to track the job: http://ip-172-31-3-218.ap-southeast-1.compute.internal:8088/proxy/application_1481253470973_0001/
16/12/08 22:26:26 INFO mapreduce.Job: Running job: job_1481253470973_0001
16/12/08 22:26:36 INFO mapreduce.Job: Job job_1481253470973_0001 running in uber mode : false
16/12/08 22:26:36 INFO mapreduce.Job:  map 0% reduce 0%
16/12/08 22:26:49 INFO mapreduce.Job:  map 4% reduce 0%
16/12/08 22:26:55 INFO mapreduce.Job:  map 8% reduce 0%
16/12/08 22:26:59 INFO mapreduce.Job:  map 12% reduce 0%
16/12/08 22:27:00 INFO mapreduce.Job:  map 14% reduce 0%
16/12/08 22:27:01 INFO mapreduce.Job:  map 17% reduce 0%
16/12/08 22:27:07 INFO mapreduce.Job:  map 21% reduce 0%
16/12/08 22:27:11 INFO mapreduce.Job:  map 22% reduce 0%
16/12/08 22:27:12 INFO mapreduce.Job:  map 25% reduce 0%
16/12/08 22:27:15 INFO mapreduce.Job:  map 30% reduce 0%
16/12/08 22:27:18 INFO mapreduce.Job:  map 31% reduce 0%
16/12/08 22:27:19 INFO mapreduce.Job:  map 34% reduce 0%
16/12/08 22:27:23 INFO mapreduce.Job:  map 36% reduce 0%
16/12/08 22:27:24 INFO mapreduce.Job:  map 38% reduce 0%
16/12/08 22:27:27 INFO mapreduce.Job:  map 39% reduce 0%
16/12/08 22:27:30 INFO mapreduce.Job:  map 43% reduce 0%
16/12/08 22:27:31 INFO mapreduce.Job:  map 47% reduce 0%
16/12/08 22:27:34 INFO mapreduce.Job:  map 48% reduce 0%
16/12/08 22:27:36 INFO mapreduce.Job:  map 49% reduce 0%
16/12/08 22:27:37 INFO mapreduce.Job:  map 51% reduce 0%
16/12/08 22:27:42 INFO mapreduce.Job:  map 52% reduce 0%
16/12/08 22:27:43 INFO mapreduce.Job:  map 53% reduce 0%
16/12/08 22:27:44 INFO mapreduce.Job:  map 56% reduce 0%
16/12/08 22:27:46 INFO mapreduce.Job:  map 61% reduce 0%
16/12/08 22:27:47 INFO mapreduce.Job:  map 62% reduce 0%
16/12/08 22:27:49 INFO mapreduce.Job:  map 64% reduce 0%
16/12/08 22:27:54 INFO mapreduce.Job:  map 65% reduce 0%
16/12/08 22:27:55 INFO mapreduce.Job:  map 66% reduce 0%
16/12/08 22:27:56 INFO mapreduce.Job:  map 68% reduce 0%
16/12/08 22:27:58 INFO mapreduce.Job:  map 69% reduce 0%
16/12/08 22:27:59 INFO mapreduce.Job:  map 71% reduce 0%
16/12/08 22:28:00 INFO mapreduce.Job:  map 74% reduce 0%
16/12/08 22:28:01 INFO mapreduce.Job:  map 77% reduce 0%
16/12/08 22:28:07 INFO mapreduce.Job:  map 79% reduce 0%
16/12/08 22:28:09 INFO mapreduce.Job:  map 81% reduce 0%
16/12/08 22:28:11 INFO mapreduce.Job:  map 83% reduce 0%
16/12/08 22:28:12 INFO mapreduce.Job:  map 85% reduce 0%
16/12/08 22:28:13 INFO mapreduce.Job:  map 86% reduce 0%
16/12/08 22:28:14 INFO mapreduce.Job:  map 87% reduce 0%
16/12/08 22:28:15 INFO mapreduce.Job:  map 90% reduce 0%
16/12/08 22:28:19 INFO mapreduce.Job:  map 92% reduce 0%
16/12/08 22:28:21 INFO mapreduce.Job:  map 94% reduce 0%
16/12/08 22:28:24 INFO mapreduce.Job:  map 95% reduce 0%
16/12/08 22:28:25 INFO mapreduce.Job:  map 95% reduce 7%
16/12/08 22:28:28 INFO mapreduce.Job:  map 96% reduce 10%
16/12/08 22:28:30 INFO mapreduce.Job:  map 97% reduce 10%
16/12/08 22:28:31 INFO mapreduce.Job:  map 100% reduce 14%
16/12/08 22:28:32 INFO mapreduce.Job:  map 100% reduce 21%
16/12/08 22:28:34 INFO mapreduce.Job:  map 100% reduce 34%
16/12/08 22:28:35 INFO mapreduce.Job:  map 100% reduce 41%
16/12/08 22:28:37 INFO mapreduce.Job:  map 100% reduce 43%
16/12/08 22:28:38 INFO mapreduce.Job:  map 100% reduce 49%
16/12/08 22:28:39 INFO mapreduce.Job:  map 100% reduce 51%
16/12/08 22:28:42 INFO mapreduce.Job:  map 100% reduce 58%
16/12/08 22:28:45 INFO mapreduce.Job:  map 100% reduce 74%
16/12/08 22:28:48 INFO mapreduce.Job:  map 100% reduce 79%
16/12/08 22:28:51 INFO mapreduce.Job:  map 100% reduce 82%
16/12/08 22:28:54 INFO mapreduce.Job:  map 100% reduce 83%
16/12/08 22:28:57 INFO mapreduce.Job:  map 100% reduce 84%
16/12/08 22:29:03 INFO mapreduce.Job:  map 100% reduce 85%
16/12/08 22:29:09 INFO mapreduce.Job:  map 100% reduce 86%
16/12/08 22:29:12 INFO mapreduce.Job:  map 100% reduce 89%
16/12/08 22:29:15 INFO mapreduce.Job:  map 100% reduce 90%
16/12/08 22:29:18 INFO mapreduce.Job:  map 100% reduce 91%
16/12/08 22:29:24 INFO mapreduce.Job:  map 100% reduce 92%
16/12/08 22:29:27 INFO mapreduce.Job:  map 100% reduce 94%
16/12/08 22:29:30 INFO mapreduce.Job:  map 100% reduce 95%
16/12/08 22:29:33 INFO mapreduce.Job:  map 100% reduce 97%
16/12/08 22:29:37 INFO mapreduce.Job:  map 100% reduce 98%
16/12/08 22:29:41 INFO mapreduce.Job:  map 100% reduce 99%
16/12/08 22:29:46 INFO mapreduce.Job:  map 100% reduce 100%
16/12/08 22:29:47 INFO mapreduce.Job: Job job_1481253470973_0001 completed successfully
16/12/08 22:29:48 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2287863955
                FILE: Number of bytes written=4542379811
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5120012243
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=249
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=77
                Launched reduce tasks=6
                Data-local map tasks=77
                Total time spent by all maps in occupied slots (ms)=952368
                Total time spent by all reduces in occupied slots (ms)=506300
                Total time spent by all map tasks (ms)=952368
                Total time spent by all reduce tasks (ms)=506300
                Total vcore-seconds taken by all map tasks=952368
                Total vcore-seconds taken by all reduce tasks=506300
                Total megabyte-seconds taken by all map tasks=975224832
                Total megabyte-seconds taken by all reduce tasks=518451200
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Map output bytes=5222400000
                Map output materialized bytes=2244133956
                Input split bytes=12243
                Combine input records=0
                Combine output records=0
                Reduce input groups=51200000
                Reduce shuffle bytes=2244133956
                Reduce input records=51200000
                Reduce output records=51200000
                Spilled Records=102400000
                Shuffled Maps =462
                Failed Shuffles=0
                Merged Map outputs=462
                GC time elapsed (ms)=17933
                CPU time spent (ms)=601630
                Physical memory (bytes) snapshot=43714064384
                Virtual memory (bytes) snapshot=129859633152
                Total committed heap usage (bytes)=50337939456
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5120000000
        File Output Format Counters
                Bytes Written=5120000000
16/12/08 22:29:48 INFO terasort.TeraSort: done

real    3m26.809s
user    0m8.014s
sys     0m0.354s


```