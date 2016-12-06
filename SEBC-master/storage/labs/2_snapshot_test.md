allow snapshot

[root@ip-172-31-7-44 ~]# sudo -u hdfs hadoop dfsadmin -allowSnapshot /user/sitysat/precious

create snapshot
[root@ip-172-31-7-44 ~]# sudo -u hdfs hadoop dfs -createSnapshot /user/sitysat/precious sebc-hdfs-test

recover from snapshot
[root@ip-172-31-7-44 home]# sudo -u hdfs hadoop fs -cp -ptopax /user/sitysat/precious/.snapshot/sebc-hdfs-test SEBC.zip
