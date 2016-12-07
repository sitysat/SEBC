1. stop hive service
```
[root@ip-172-31-7-44 ~]# curl -X post -u cm:cloudera 'http://ec2-54-169-199-183.ap-southeast-1.compute.amazonaws.com:7180api/v12/clusters/cluster/services/hive/commands/stop'
{
  "id" : 1014,
  "name" : "Stop",
  "startTime" : "2016-12-07T03:12:47.348Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
```

2. start hive service
```
[root@ip-172-31-7-44 ~]# curl -X post -u cm:cloudera 'http://ec2-54-169-199-183.ap-southeast-1.compute.amazonaws.com:7180api/v12/clusters/cluster/services/hive/commands/start'
{
  "id" : 1018,
  "name" : "Start",
  "startTime" : "2016-12-07T03:13:37.504Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```


3. show current state of Hive service

curl http://ec2-54-169-199-183.ap-southeast-1.compute.amazonaws.com:7180/api/v12/clusters/cluster/services/hive
```

{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-7-44.ap-southeast-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-7-44.ap-southeast-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}
```