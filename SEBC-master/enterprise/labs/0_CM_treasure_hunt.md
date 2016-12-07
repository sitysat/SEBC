#What is ubertask optimization?
```
the small-jobs "ubertask" optimization, which runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the following maxmaps, maxreduces, and maxbytes settings. 
Note that configurations for application masters also affect the "Small" definition - yarn.app.mapreduce.am.resource.mb must be larger than both mapreduce.map.memory.mb and mapreduce.reduce.memory.mb, and yarn.app.mapreduce.am.resource.cpu-vcores must be larger than both mapreduce.map.cpu.vcores and mapreduce.reduce.cpu.vcores to enable ubertask. 
```

#Where in CM is the Kerberos Security Realm value displayed?
```
HADOOP.COM
```

#Which CDH service(s) host a property for enabling Kerberos authentication?
```
under menu Administration > Security
```

#How do you upgrade the CM agents?
```
1. automatic update by cloudera manager
2. manually update by yum install
```

#Give the tsquery statement used to chart Hue's CPU utilization?
```
SELECT cpu_system_rate + cpu_user_rate WHERE entityName = "hue-HUE_SERVER-486d5634ff61c266e65468f40028b8ee" AND category = ROLE
```

#Name all the roles that make up the Hive service
```
1. Hive Metastore Server
2. WebHCat Server
3. HiveServer2
4. Gateway
```

#What steps must be completed before integrating Cloudera Manager with Kerberos?
```
1. Set up a working KDC. Cloudera Manager supports MIT KDC and Active Directory.
2. The KDC should be configured to have non-zero ticket lifetime and renewal lifetime. CDH will not work properly if tickets are not renewable.
3. OpenLdap client libraries should be installed on the Cloudera Manager Server host if you want to use Active Directory. Also, Kerberos client libraries should be installed on ALL hosts.
4. Cloudera Manager needs an account that has permissions to create other accounts in the KDC.
```
