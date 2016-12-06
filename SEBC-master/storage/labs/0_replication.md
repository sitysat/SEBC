1. replication using BDR
from WinZerZ_source to WinZerZ_replicate
[root@ip-172-31-7-45 ~]# hadoop fs -ls /tmp/WinZerZ_replicate/WinZerZ_source
Found 2 items
-rw-r--r--   3 root supergroup          0 2016-12-05 21:15 /tmp/WinZerZ_replicate/WinZerZ_source/_SUCCESS
-rw-r--r--   3 root supergroup  500000000 2016-12-05 21:15 /tmp/WinZerZ_replicate/WinZerZ_source/part-m-00000