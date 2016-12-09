Command and output for hdfs dfs -ls /user
```
[root@ip-172-31-3-217 ~]# sudo -u hdfs hadoop fs -ls /user
Found 6 items
drwxrwxrwx   - mapred  hadoop          0 2016-12-08 21:28 /user/history
drwxrwxr-t   - hive    hive            0 2016-12-08 21:29 /user/hive
drwxrwxr-x   - hue     hue             0 2016-12-08 21:29 /user/hue
drwxrwxr-x   - oozie   oozie           0 2016-12-08 21:29 /user/oozie
drwxr-xr-x   - orchard shops           0 2016-12-08 21:31 /user/orchard
drwxr-xr-x   - raffles walks           0 2016-12-08 21:31 /user/raffles
```

The output from the CM API call ../api/v14/hosts
```
[root@ip-172-31-3-217 ~]# curl -u admin:admin 'http://172.31.3.217:7180/api/version'
v14
```