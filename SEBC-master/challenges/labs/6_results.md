Login to beeline
```
beeline > !connect jdbc:hive2://172.31.3.217:10000/default;principal=hive/ip-172-31-3-217.ap-southeast-1.compute.internal@SITYSAT.SG
```
Create an overlord role that has rights to the default database
```
CREATE ROLE overlord;
GRANT ALL ON DATABASE default TO ROLE overlord;


```

Map the walks group to this role
```
GRANT ROLE overlord to GROUP walks;
```
Create an worker role that has SELECT privileges on all tables in default
```
0: jdbc:hive2://172.31.3.217:10000/default> CREATE ROLE worker;
INFO  : Compiling command(queryId=hive_20161208225757_3295ef87-75e3-48f7-a169-7c8ba1bd984c): CREATE ROLE worker
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161208225757_3295ef87-75e3-48f7-a169-7c8ba1bd984c); Time taken: 0.068 seconds
INFO  : Executing command(queryId=hive_20161208225757_3295ef87-75e3-48f7-a169-7c8ba1bd984c): CREATE ROLE worker
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208225757_3295ef87-75e3-48f7-a169-7c8ba1bd984c); Time taken: 0.043 seconds
INFO  : OK
No rows affected (0.124 seconds)


0: jdbc:hive2://172.31.3.217:10000/default> GRANT SELECT ON DATABASE default TO ROLE worker;
INFO  : Compiling command(queryId=hive_20161208225858_d721f597-85dd-4817-83f2-7fc9245b6302): GRANT SELECT ON DATABASE default TO ROLE worker
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161208225858_d721f597-85dd-4817-83f2-7fc9245b6302); Time taken: 0.054 seconds
INFO  : Executing command(queryId=hive_20161208225858_d721f597-85dd-4817-83f2-7fc9245b6302): GRANT SELECT ON DATABASE default TO ROLE worker
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208225858_d721f597-85dd-4817-83f2-7fc9245b6302); Time taken: 0.037 seconds
INFO  : OK
No rows affected (0.104 seconds)

```
Map the shops group to this role
```
0: jdbc:hive2://172.31.3.217:10000/default> GRANT ROLE worker to group shops;
INFO  : Compiling command(queryId=hive_20161208225858_cf853b6e-804a-43d0-b7c8-7e72ceaa472e): GRANT ROLE worker to group shops
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161208225858_cf853b6e-804a-43d0-b7c8-7e72ceaa472e); Time taken: 0.053 seconds
INFO  : Executing command(queryId=hive_20161208225858_cf853b6e-804a-43d0-b7c8-7e72ceaa472e): GRANT ROLE worker to group shops
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208225858_cf853b6e-804a-43d0-b7c8-7e72ceaa472e); Time taken: 0.035 seconds
INFO  : OK
No rows affected (0.101 seconds)
```

Login to beeline as the principal for orchard
```
[orchard@ip-172-31-3-219 root]$ beeline
2016-12-08 22:54:24,705 WARN  [main] mapreduce.TableMapReduceUtil: The hbase-prefix-tree module jar containing PrefixTreeCodec is not present.  Continuing without it.
Beeline version 1.1.0-cdh5.9.0 by Apache Hive
beeline> !connect jdbc:hive2://172.31.3.217:10000/default;principal=hive/ip-172-31-3-217.ap-southeast-1.compute.internal@SITYSAT.SG
scan complete in 2ms
Connecting to jdbc:hive2://172.31.3.217:10000/default;principal=hive/ip-172-31-3-217.ap-southeast-1.compute.internal@SITYSAT.SG
Connected to: Apache Hive (version 1.1.0-cdh5.9.0)
Driver: Hive JDBC (version 1.1.0-cdh5.9.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ

0: jdbc:hive2://172.31.3.217:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20161208225858_092216ae-6099-44a7-a452-9fddb2317962): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161208225858_092216ae-6099-44a7-a452-9fddb2317962); Time taken: 0.056 seconds
INFO  : Executing command(queryId=hive_20161208225858_092216ae-6099-44a7-a452-9fddb2317962): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208225858_092216ae-6099-44a7-a452-9fddb2317962); Time taken: 0.108 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.183 seconds)



```

Login to beeline as the principal for raffles
```
0: jdbc:hive2://172.31.3.217:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20161208225353_a00ff243-a125-409c-897b-f293e83b807a): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161208225353_a00ff243-a125-409c-897b-f293e83b807a); Time taken: 0.215 seconds
INFO  : Executing command(queryId=hive_20161208225353_a00ff243-a125-409c-897b-f293e83b807a): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208225353_a00ff243-a125-409c-897b-f293e83b807a); Time taken: 0.223 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
```