1. create user sitysat and create home directory for sitysat user
[root@ip-172-31-7-46 ~]# sudo -u sitysat hadoop fs -ls /user/sitysat/
Found 1 items
drwxr-xr-x   - sitysat supergroup          0 2016-12-05 22:10 /user/sitysat/teragen_output

2. run teragen under sitysat user
[root@ip-172-31-7-44 cloudera-scm-server]# sudo -u sitysat time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-example.jar teragen -Dmapreduce.job.maps=4 -Ddfs.blocksize=33554432 100000000 teragen_output
Not a valid JAR: /opt/cloudera/parcels/CDH-5.8.2-1.cdh5.8.2.p0.3/jars/hadoop-example.jar
0.20user 0.03system 0:00.17elapsed 134%CPU (0avgtext+0avgdata 27744maxresident)k
0inputs+64outputs (0major+15434minor)pagefaults 0swaps
[root@ip-172-31-7-44 cloudera-scm-server]# su sitysat
[sitysat@ip-172-31-7-44 cloudera-scm-server]$ time hadoop jar /opt/cloudera/parcels/CDH/
bin/     etc/     include/ jars/    lib/     lib64/   libexec/ meta/    share/
[sitysat@ip-172-31-7-44 cloudera-scm-server]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Dmapreduce.job.maps=4 -Ddfs.blocksize=33554432 100000000 teragen_output
16/12/05 22:10:06 INFO Configuration.deprecation: session.id is deprecated. Instead, use dfs.metrics.session-id
16/12/05 22:10:06 INFO jvm.JvmMetrics: Initializing JVM Metrics with processName=JobTracker, sessionId=
16/12/05 22:10:06 INFO terasort.TeraSort: Generating 100000000 using 1
16/12/05 22:10:06 INFO mapreduce.JobSubmitter: number of splits:1
16/12/05 22:10:06 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_local281299161_0001
16/12/05 22:10:06 INFO mapreduce.Job: The url to track the job: http://localhost:8080/
16/12/05 22:10:06 INFO mapreduce.Job: Running job: job_local281299161_0001
16/12/05 22:10:06 INFO mapred.LocalJobRunner: OutputCommitter set in config null
16/12/05 22:10:06 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
16/12/05 22:10:06 INFO mapred.LocalJobRunner: OutputCommitter is org.apache.hadoop.mapreduce.lib.output.FileOutputCommitter
16/12/05 22:10:06 INFO mapred.LocalJobRunner: Waiting for map tasks
16/12/05 22:10:06 INFO mapred.LocalJobRunner: Starting task: attempt_local281299161_0001_m_000000_0
16/12/05 22:10:06 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
16/12/05 22:10:07 INFO mapred.Task:  Using ResourceCalculatorProcessTree : [ ]
16/12/05 22:10:07 INFO mapred.MapTask: Processing split: org.apache.hadoop.examples.terasort.TeraGen$RangeInputFormat$RangeInputSplit@1e7a5697
16/12/05 22:10:07 INFO mapreduce.Job: Job job_local281299161_0001 running in uber mode : false
16/12/05 22:10:07 INFO mapreduce.Job:  map 0% reduce 0%
16/12/05 22:10:13 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:13 INFO mapreduce.Job:  map 6% reduce 0%
16/12/05 22:10:16 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:16 INFO mapreduce.Job:  map 9% reduce 0%
16/12/05 22:10:19 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:19 INFO mapreduce.Job:  map 12% reduce 0%
16/12/05 22:10:22 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:22 INFO mapreduce.Job:  map 15% reduce 0%
16/12/05 22:10:25 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:25 INFO mapreduce.Job:  map 18% reduce 0%
16/12/05 22:10:28 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:28 INFO mapreduce.Job:  map 20% reduce 0%
16/12/05 22:10:31 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:31 INFO mapreduce.Job:  map 22% reduce 0%
16/12/05 22:10:34 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:34 INFO mapreduce.Job:  map 24% reduce 0%
16/12/05 22:10:37 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:37 INFO mapreduce.Job:  map 25% reduce 0%
16/12/05 22:10:40 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:40 INFO mapreduce.Job:  map 27% reduce 0%
16/12/05 22:10:43 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:43 INFO mapreduce.Job:  map 28% reduce 0%
16/12/05 22:10:46 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:46 INFO mapreduce.Job:  map 30% reduce 0%
16/12/05 22:10:49 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:49 INFO mapreduce.Job:  map 31% reduce 0%
16/12/05 22:10:52 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:52 INFO mapreduce.Job:  map 32% reduce 0%
16/12/05 22:10:55 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:55 INFO mapreduce.Job:  map 34% reduce 0%
16/12/05 22:10:58 INFO mapred.LocalJobRunner: map > map
16/12/05 22:10:58 INFO mapreduce.Job:  map 35% reduce 0%
16/12/05 22:11:01 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:01 INFO mapreduce.Job:  map 37% reduce 0%
16/12/05 22:11:04 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:04 INFO mapreduce.Job:  map 39% reduce 0%
16/12/05 22:11:07 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:10 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:10 INFO mapreduce.Job:  map 41% reduce 0%
16/12/05 22:11:13 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:13 INFO mapreduce.Job:  map 43% reduce 0%
16/12/05 22:11:16 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:16 INFO mapreduce.Job:  map 45% reduce 0%
16/12/05 22:11:19 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:19 INFO mapreduce.Job:  map 46% reduce 0%
16/12/05 22:11:22 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:22 INFO mapreduce.Job:  map 47% reduce 0%
16/12/05 22:11:25 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:25 INFO mapreduce.Job:  map 48% reduce 0%
16/12/05 22:11:28 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:28 INFO mapreduce.Job:  map 50% reduce 0%
16/12/05 22:11:31 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:31 INFO mapreduce.Job:  map 51% reduce 0%
16/12/05 22:11:34 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:34 INFO mapreduce.Job:  map 52% reduce 0%
16/12/05 22:11:37 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:37 INFO mapreduce.Job:  map 55% reduce 0%
16/12/05 22:11:40 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:40 INFO mapreduce.Job:  map 56% reduce 0%
16/12/05 22:11:43 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:43 INFO mapreduce.Job:  map 57% reduce 0%
16/12/05 22:11:46 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:46 INFO mapreduce.Job:  map 59% reduce 0%
16/12/05 22:11:49 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:49 INFO mapreduce.Job:  map 61% reduce 0%
16/12/05 22:11:52 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:52 INFO mapreduce.Job:  map 63% reduce 0%
16/12/05 22:11:55 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:55 INFO mapreduce.Job:  map 65% reduce 0%
16/12/05 22:11:58 INFO mapred.LocalJobRunner: map > map
16/12/05 22:11:58 INFO mapreduce.Job:  map 66% reduce 0%
16/12/05 22:12:01 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:01 INFO mapreduce.Job:  map 68% reduce 0%
16/12/05 22:12:04 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:04 INFO mapreduce.Job:  map 69% reduce 0%
16/12/05 22:12:07 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:07 INFO mapreduce.Job:  map 70% reduce 0%
16/12/05 22:12:10 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:10 INFO mapreduce.Job:  map 71% reduce 0%
16/12/05 22:12:13 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:13 INFO mapreduce.Job:  map 73% reduce 0%
16/12/05 22:12:16 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:16 INFO mapreduce.Job:  map 75% reduce 0%
16/12/05 22:12:19 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:19 INFO mapreduce.Job:  map 76% reduce 0%
16/12/05 22:12:22 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:22 INFO mapreduce.Job:  map 77% reduce 0%
16/12/05 22:12:25 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:25 INFO mapreduce.Job:  map 79% reduce 0%
16/12/05 22:12:28 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:28 INFO mapreduce.Job:  map 80% reduce 0%
16/12/05 22:12:31 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:31 INFO mapreduce.Job:  map 81% reduce 0%
16/12/05 22:12:34 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:34 INFO mapreduce.Job:  map 82% reduce 0%
16/12/05 22:12:37 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:37 INFO mapreduce.Job:  map 84% reduce 0%
16/12/05 22:12:40 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:40 INFO mapreduce.Job:  map 85% reduce 0%
16/12/05 22:12:43 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:43 INFO mapreduce.Job:  map 87% reduce 0%
16/12/05 22:12:46 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:46 INFO mapreduce.Job:  map 89% reduce 0%
16/12/05 22:12:49 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:49 INFO mapreduce.Job:  map 91% reduce 0%
16/12/05 22:12:52 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:52 INFO mapreduce.Job:  map 92% reduce 0%
16/12/05 22:12:55 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:55 INFO mapreduce.Job:  map 94% reduce 0%
16/12/05 22:12:58 INFO mapred.LocalJobRunner: map > map
16/12/05 22:12:58 INFO mapreduce.Job:  map 96% reduce 0%
16/12/05 22:13:01 INFO mapred.LocalJobRunner: map > map
16/12/05 22:13:01 INFO mapreduce.Job:  map 97% reduce 0%
16/12/05 22:13:04 INFO mapred.LocalJobRunner: map > map
16/12/05 22:13:04 INFO mapreduce.Job:  map 99% reduce 0%
16/12/05 22:13:05 INFO mapred.LocalJobRunner: map > map
16/12/05 22:13:06 INFO mapred.Task: Task:attempt_local281299161_0001_m_000000_0 is done. And is in the process of committing
16/12/05 22:13:06 INFO mapred.LocalJobRunner: map > map
16/12/05 22:13:06 INFO mapred.Task: Task attempt_local281299161_0001_m_000000_0 is allowed to commit now
16/12/05 22:13:06 INFO output.FileOutputCommitter: Saved output of task 'attempt_local281299161_0001_m_000000_0' to hdfs://ip-172-31-7-44.ap-southeast-1.compute.internal:8020/user/sitysat/teragen_output/_temporary/0/task_local281299161_0001_m_000000
16/12/05 22:13:06 INFO mapred.LocalJobRunner: map
16/12/05 22:13:06 INFO mapred.Task: Task 'attempt_local281299161_0001_m_000000_0' done.
16/12/05 22:13:06 INFO mapred.LocalJobRunner: Finishing task: attempt_local281299161_0001_m_000000_0
16/12/05 22:13:06 INFO mapred.LocalJobRunner: map task executor complete.
16/12/05 22:13:06 INFO mapreduce.Job:  map 100% reduce 0%
16/12/05 22:13:06 INFO mapreduce.Job: Job job_local281299161_0001 completed successfully
16/12/05 22:13:07 INFO mapreduce.Job: Counters: 21
        File System Counters
             FILE: Number of bytes read=276330
             FILE: Number of bytes written=564154
             FILE: Number of read operations=0
             FILE: Number of large read operations=0
             FILE: Number of write operations=0
             HDFS: Number of bytes read=0
             HDFS: Number of bytes written=10000000000
             HDFS: Number of read operations=4
             HDFS: Number of large read operations=0
             HDFS: Number of write operations=3
        Map-Reduce Framework
             Map input records=100000000
             Map output records=100000000
             Input split bytes=83
             Spilled Records=0
             Failed Shuffles=0
             Merged Map outputs=0
             GC time elapsed (ms)=1158
             Total committed heap usage (bytes)=211288064
        org.apache.hadoop.examples.terasort.TeraGen$Counters
             CHECKSUM=214760662691937609
        File Input Format Counters
             Bytes Read=0
        File Output Format Counters
             Bytes Written=10000000000

real    3m3.314s
user    1m56.293s
sys     0m7.337s

result file
[root@ip-172-31-7-46 ~]# -rw-r--r--   3 sitysat supergroup           0 2016-12-05 22:13 /user/sitysat/teragen_output/_SUCCESS
[root@ip-172-31-7-46 ~]# -rw-r--r--   3 sitysat supergroup       9.3 G 2016-12-05 22:13 /user/sitysat/teragen_output/part-m-00000

#################################################33
2. Terasort command
time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort teragen_output terasort_output



16/12/05 23:23:57 INFO mapred.Task: Task 'attempt_local969463593_0001_r_000000_0' done.
16/12/05 23:23:57 INFO mapred.LocalJobRunner: Finishing task: attempt_local969463593_0001_r_000000_0
16/12/05 23:23:57 INFO mapred.LocalJobRunner: reduce task executor complete.
16/12/05 23:23:57 INFO mapreduce.Job:  map 100% reduce 100%
16/12/05 23:23:57 INFO mapreduce.Job: Job job_local969463593_0001 completed successfully
16/12/05 23:23:57 INFO mapreduce.Job: Counters: 35
        File System Counters
             FILE: Number of bytes read=5008602359
             FILE: Number of bytes written=68866533724
             FILE: Number of read operations=0
             FILE: Number of large read operations=0
             FILE: Number of write operations=0
             HDFS: Number of bytes read=64001343400
             HDFS: Number of bytes written=2000000000
             HDFS: Number of read operations=5186
             HDFS: Number of large read operations=0
             HDFS: Number of write operations=124
        Map-Reduce Framework
             Map input records=20000000
             Map output records=20000000
             Map output bytes=2040000000
             Map output materialized bytes=2080000360
             Input split bytes=9840
             Combine input records=0
             Combine output records=0
             Reduce input groups=20000000
             Reduce shuffle bytes=2080000360
             Reduce input records=20000000
             Reduce output records=20000000
             Spilled Records=47920400
             Shuffled Maps =60
             Failed Shuffles=0
             Merged Map outputs=60
             GC time elapsed (ms)=5116
             Total committed heap usage (bytes)=15830876160
        Shuffle Errors
             BAD_ID=0
             CONNECTION=0
             IO_ERROR=0
             WRONG_LENGTH=0
             WRONG_MAP=0
             WRONG_REDUCE=0
        File Input Format Counters
             Bytes Read=2000000000
        File Output Format Counters
             Bytes Written=2000000000
16/12/05 23:23:57 INFO terasort.TeraSort: done

real    2m19.671s
user    2m24.245s
sys     0m14.360s

