1. replication using BDR
from WinZerZ_source to WinZerZ_replicate
[root@ip-172-31-7-45 ~]# hadoop fs -ls /tmp/WinZerZ_replicate/WinZerZ_source
Found 2 items
-rw-r--r--   3 root supergroup          0 2016-12-05 21:15 /tmp/WinZerZ_replicate/WinZerZ_source/_SUCCESS
-rw-r--r--   3 root supergroup  500000000 2016-12-05 21:15 /tmp/WinZerZ_replicate/WinZerZ_source/part-m-00000

FSCK check replication
##########################################################
[root@ip-172-31-7-44 cloudera-scm-server]# hdfs fsck /tmp/WinZerZ_replicate/WinZerZ_source -files -blocks
Connecting to namenode via http://ip-172-31-7-44.ap-southeast-1.compute.internal:50070
FSCK started by root (auth:SIMPLE) from /172.31.7.44 for path /tmp/WinZerZ_replicate/WinZerZ_source at Mon Dec 05 21:47:08 EST 2016
/tmp/WinZerZ_replicate/WinZerZ_source <dir>
/tmp/WinZerZ_replicate/WinZerZ_source/_SUCCESS 0 bytes, 0 block(s):  OK

/tmp/WinZerZ_replicate/WinZerZ_source/part-m-00000 500000000 bytes, 4 block(s):  OK
0. BP-527270424-172.31.7.44-1480956531176:blk_1073741889_1065 len=134217728 Live_repl=3
1. BP-527270424-172.31.7.44-1480956531176:blk_1073741890_1066 len=134217728 Live_repl=3
2. BP-527270424-172.31.7.44-1480956531176:blk_1073741891_1067 len=134217728 Live_repl=3
3. BP-527270424-172.31.7.44-1480956531176:blk_1073741892_1068 len=97346816 Live_repl=3

Status: HEALTHY
 Total size: 500000000 B
 Total dirs: 1
 Total files:   2
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Mon Dec 05 21:47:08 EST 2016 in 2 milliseconds


The filesystem under path '/tmp/WinZerZ_replicate/WinZerZ_source' is HEALTHY

##########################################################

[root@ip-172-31-13-24 ~]# hdfs fsck /tmp/WinZerZ_source -files -blocks
Connecting to namenode via http://ip-172-31-13-24.ap-southeast-1.compute.internal:50070
FSCK started by root (auth:SIMPLE) from /172.31.13.24 for path /tmp/WinZerZ_source at Mon Dec 05 21:44:40 EST 2016
/tmp/WinZerZ_source <dir>
/tmp/WinZerZ_source/_SUCCESS 0 bytes, 0 block(s):  OK

/tmp/WinZerZ_source/part-m-00000 500000000 bytes, 4 block(s):  OK
0. BP-1532971839-172.31.13.24-1480936560540:blk_1073743213_2389 len=134217728 Live_repl=3
1. BP-1532971839-172.31.13.24-1480936560540:blk_1073743214_2390 len=134217728 Live_repl=3
2. BP-1532971839-172.31.13.24-1480936560540:blk_1073743215_2391 len=134217728 Live_repl=3
3. BP-1532971839-172.31.13.24-1480936560540:blk_1073743216_2392 len=97346816 Live_repl=3

Status: HEALTHY
 Total size:	500000000 B
 Total dirs:	1
 Total files:	2
 Total symlinks:		0
 Total blocks (validated):	4 (avg. block size 125000000 B)
 Minimally replicated blocks:	4 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		3
 Number of racks:		1
FSCK ended at Mon Dec 05 21:44:40 EST 2016 in 2 milliseconds


The filesystem under path '/tmp/WinZerZ_source' is HEALTHY
