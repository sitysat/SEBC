The full teragen command
```
[raffles@ip-172-31-3-217 root]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Ddfs.blocksize=67108864 -Dmapreduce.job.maps=8 51200000 tgen512m

```

The output of the time command
```
real    2m38.226s
user    1m3.759s
sys     0m3.622s
```
The command and output of hdfs dfs -ls /user/raffles/tgen512m
```
[raffles@ip-172-31-3-217 root]$ hdfs dfs -ls /user/raffles/tgen512m
Found 2 items
-rw-r--r--   3 raffles walks          0 2016-12-08 21:51 /user/raffles/tgen512m/_SUCCESS
-rw-r--r--   3 raffles walks 5120000000 2016-12-08 21:51 /user/raffles/tgen512m/part-m-00000

```
Show how many blocks are linked to this directory

answer 77 blocks in this directory
```
[raffles@ip-172-31-3-217 root]$  hdfs fsck -blocks /user/raffles/tgen512m
Connecting to namenode via http://ip-172-31-3-217.ap-southeast-1.compute.internal:50070
FSCK started by raffles (auth:SIMPLE) from /172.31.3.217 for path /user/raffles/tgen512m at Thu Dec 08 21:56:44 EST 2016
..Status: HEALTHY
 Total size:    5120000000 B
 Total dirs:    1
 Total files:   2
 Total symlinks:                0
 Total blocks (validated):      77 (avg. block size 66493506 B)
 Minimally replicated blocks:   77 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Thu Dec 08 21:56:44 EST 2016 in 3 milliseconds


The filesystem under path '/user/raffles/tgen512m' is HEALTHY

```