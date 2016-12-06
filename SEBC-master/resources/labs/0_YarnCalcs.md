1 The assumption will be calculated based the configuration with ( 20 vCores, Ram 128 GB, 12 disks ) x 10 worker nodes. THe workload factor = 2 for the combination of ground work, YARN application and Impala query

2 We reserve resource with below configuration
			Memory	vCores
OS			8		2
NodeManager	1		1
DataNode	1		1
Impalad		32		4	with assumption (1 process hold 8 GB of RAM)
CM Agent	1		1
No HBASE and Solr

Note : avaialable resource per node will be 11 vCores, Ram 87040 Bytes for (yarn.nodemanager.resource) configuration

3 allow minimum allocation for yarn scheduler
with minimum 1 core, 1024 Bytes and maximum <=avalable vcore(11) and 11264 Bytes for memory allocation. I will not allow one container to consume most of available memory.
the incremental step will be 1 core and ram 1024 mb.


