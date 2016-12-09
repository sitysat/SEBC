List the region, AMI ID, and OS you are using
```
region : singapore
AMI ID : RHEL-6.7_HVM-20160412-x86_64-1-Hourly2-GP2 (ami-d5489db6)
OS : RHEL-6.7

SEBC-CL-SIT-CM, i-3c1fdf9b, 172.31.3.217, 54.251.167.20, ec2-54-251-167-20.ap-southeast-1.compute.amazonaws.com

SEBC-CL-SIT-RM, i-3d1fdf9a, 172.31.3.218, 54.169.150.25, 
ec2-54-169-150-25.ap-southeast-1.compute.amazonaws.com

SEBC-CL-SIT-DN1, i-8222e225, 172.31.3.219, 54.169.222.243, 
ec2-54-169-222-243.ap-southeast-1.compute.amazonaws.com

SEBC-CL-SIT-DN2, i-8322e224, 172.31.3.220, 54.169.204.85, 
ec2-54-169-204-85.ap-southeast-1.compute.amazonaws.com

SEBC-CL-SIT-DN3, i-8022e227, 172.31.3.221, 54.179.150.179, 
ec2-54-179-150-179.ap-southeast-1.compute.amazonaws.com
```

List the volume space you have available on each node
```
Instance type : m3.xlarge
Root Disk : 30 GiB (/dev/sda1)
			50 GiB (/dev/sdb)
```

The command and output for yum repolist enabled
```
yum repolist

[root@ip-172-31-3-217 ~]# yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, security
repo id                                         repo name                                                                     status
cloudera-manager                                Cloudera Manager 5.x                                                               7
mysql                                           MySQL Community Server 5.x                                                       316
rhui-REGION-client-config-server-6              Red Hat Update Infrastructure 2.0 Client Configuration Server 6                    6
rhui-REGION-rhel-server-releases                Red Hat Enterprise Linux Server 6 (RPMs)                                      18,378
rhui-REGION-rhel-server-rh-common               Red Hat Enterprise Linux Server 6 RH Common (RPMs)                               129
```

List the /etc/passwd entries for raffles and orchard in your setup file
```
orchard:x:2800:2800::/home/orchard:/bin/bash
raffles:x:2700:2700::/home/raffles:/bin/bash
```

List the /etc/group entries for shops and walks in your setup file
```
shops:x:1100:orchard
walks:x:1200:raffles
```
