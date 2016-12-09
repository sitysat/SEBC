Run the Hadoop pi program as the user orchard

```
[orchard@ip-172-31-3-219 root]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-mapreduce-examples-2.6.0-cdh5.9.0.jar pi 10 100
Number of Maps  = 10
Samples per Map = 100
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Starting Job
16/12/08 22:28:44 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-3-218.ap-southeast-1.compute.internal/172.31.3.218:8032
16/12/08 22:28:44 INFO hdfs.DFSClient: Created token for orchard: HDFS_DELEGATION_TOKEN owner=orchard@SITYSAT.SG, renewer=yarn, realUser=, issueDate=1481254124851, maxDate=1481858924851, sequenceNumber=2, masterKeyId=2 on 172.31.3.217:8020
16/12/08 22:28:44 INFO security.TokenCache: Got dt for hdfs://ip-172-31-3-217.ap-southeast-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.3.217:8020, Ident: (token for orchard: HDFS_DELEGATION_TOKEN owner=orchard@SITYSAT.SG, renewer=yarn, realUser=, issueDate=1481254124851, maxDate=1481858924851, sequenceNumber=2, masterKeyId=2)
16/12/08 22:28:45 INFO input.FileInputFormat: Total input paths to process : 10
16/12/08 22:28:45 INFO mapreduce.JobSubmitter: number of splits:10
16/12/08 22:28:45 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1481253470973_0002
16/12/08 22:28:45 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.3.217:8020, Ident: (token for orchard: HDFS_DELEGATION_TOKEN owner=orchard@SITYSAT.SG, renewer=yarn, realUser=, issueDate=1481254124851, maxDate=1481858924851, sequenceNumber=2, masterKeyId=2)
16/12/08 22:28:45 INFO impl.YarnClientImpl: Submitted application application_1481253470973_0002
16/12/08 22:28:45 INFO mapreduce.Job: The url to track the job: http://ip-172-31-3-218.ap-southeast-1.compute.internal:8088/proxy/application_1481253470973_0002/
16/12/08 22:28:45 INFO mapreduce.Job: Running job: job_1481253470973_0002
16/12/08 22:28:59 INFO mapreduce.Job: Job job_1481253470973_0002 running in uber mode : false
16/12/08 22:28:59 INFO mapreduce.Job:  map 0% reduce 0%
16/12/08 22:29:13 INFO mapreduce.Job:  map 20% reduce 0%
16/12/08 22:29:14 INFO mapreduce.Job:  map 30% reduce 0%
16/12/08 22:29:21 INFO mapreduce.Job:  map 40% reduce 0%
16/12/08 22:29:22 INFO mapreduce.Job:  map 60% reduce 0%
16/12/08 22:29:27 INFO mapreduce.Job:  map 70% reduce 0%
16/12/08 22:29:29 INFO mapreduce.Job:  map 90% reduce 0%
16/12/08 22:29:32 INFO mapreduce.Job:  map 100% reduce 0%
16/12/08 22:29:42 INFO mapreduce.Job:  map 100% reduce 100%
16/12/08 22:29:43 INFO mapreduce.Job: Job job_1481253470973_0002 completed successfully
16/12/08 22:29:43 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=98
                FILE: Number of bytes written=1367727
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=3050
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=43
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=10
                Launched reduce tasks=1
                Data-local map tasks=10
                Total time spent by all maps in occupied slots (ms)=77945
                Total time spent by all reduces in occupied slots (ms)=9587
                Total time spent by all map tasks (ms)=77945
                Total time spent by all reduce tasks (ms)=9587
                Total vcore-seconds taken by all map tasks=77945
                Total vcore-seconds taken by all reduce tasks=9587
                Total megabyte-seconds taken by all map tasks=79815680
                Total megabyte-seconds taken by all reduce tasks=9817088
        Map-Reduce Framework
                Map input records=10
                Map output records=20
                Map output bytes=180
                Map output materialized bytes=340
                Input split bytes=1870
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=340
                Reduce input records=20
                Reduce output records=0
                Spilled Records=40
                Shuffled Maps =10
                Failed Shuffles=0
                Merged Map outputs=10
                GC time elapsed (ms)=487
                CPU time spent (ms)=7910
                Physical memory (bytes) snapshot=4707471360
                Virtual memory (bytes) snapshot=17273593856
                Total committed heap usage (bytes)=5458886656
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1180
        File Output Format Counters
                Bytes Written=97
Job Finished in 59.124 seconds
Estimated value of Pi is 3.14800000000000000000

real    1m2.577s
user    0m6.100s
sys     0m0.331s
```