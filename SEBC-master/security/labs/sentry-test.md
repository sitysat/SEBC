Use beeline to confirm your principal sees no tables

```
beeline> !connect jdbc:hive2://172.31.1.144:10000/default;principal=hive/ip-172-31-1-144.ap-southeast-1.compute.internal@GBCHADOOP.COM
Connecting to jdbc:hive2://172.31.1.144:10000/default;principal=hive/ip-172-31-1-144.ap-southeast-1.compute.internal@GBCHADOOP.COM
Enter username for jdbc:hive2://172.31.1.144:10000/default;principal=hive/ip-172-31-1-144.ap-southeast-1.compute.internal@GBCHADOOP.COM:
Enter password for jdbc:hive2://172.31.1.144:10000/default;principal=hive/ip-172-31-1-144.ap-southeast-1.compute.internal@GBCHADOOP.COM:
Connected to: Apache Hive (version 1.1.0-cdh5.8.2)
Driver: Hive JDBC (version 1.1.0-cdh5.8.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://172.31.1.144:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20161207225858_6de83c2f-6942-4b26-a828-c995c46da39e): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161207225858_6de83c2f-6942-4b26-a828-c995c46da39e); Time taken: 0.735 seconds
INFO  : Executing command(queryId=hive_20161207225858_6de83c2f-6942-4b26-a828-c995c46da39e): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161207225858_6de83c2f-6942-4b26-a828-c995c46da39e); Time taken: 0.24 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.319 seconds)
```

