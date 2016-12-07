Use the API on the command line to:

#Report the latest available version of the API
```
curl 'http://ec2-54-169-199-183.ap-southeast-1.compute.amazonaws.com:7180/api/version'
v14
```

#Report the CM version
```
curl 'http://ec2-54-169-199-183.ap-southeast-1.compute.amazonaws.com:7180/api/version'
{
  "version" : "5.9.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20161006-1801",
  "gitHash" : "898a5e032c080e18833dfc58180761f6ef2ea351",
  "snapshot" : false
}
```

#List all CM users
```
curl -u cm:cloudera 'http://ec2-54-169-199-183.ap-southeast-1.compute.amazonaws.com:7180/api/v14/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "cm",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
```

#Report the database server in use by CM
```
curl -u cm:cloudera 'http://ec2-54-169-199-183.ap-southeast-1.compute.amazonaws.com:7180/api/v14/cm/scmDbInfo'

{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```