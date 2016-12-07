use curl on the endpoint ./api/v2/cm/deployment

'''
[root@ip-172-31-7-44 ~]# curl -u cm:cloudera 'http://localhost:7180/api/v2/cm/deployment'

{
  "timestamp" : "2016-12-07T02:51:28.555Z",
  "clusters" : [ {
    "name" : "sitysat/SEBC",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "875560960"
          }, {
            "name" : "role_health_suppression_hivemetastore_canary_health",
            "value" : "true"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "875560960"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "3545550028"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "596"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-7-44.ap-southeast-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "silent"
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "hivedb"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-486d5634ff61c266e65468f40028b8ee",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-00724fd297c0f00de"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-746675fa0ba9d0c97fb8782479545644",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0f3fd2f1af18c964e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-84297081ecfe5aa6c84770315d889413",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-09c31b64f43b1a9ba"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-c7735b5e301e46551d021530f176f9e8",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0a36e1a1bf37a2cbb"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-f64663d4e4afd64308f21d29e221794e",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0598663189a357460"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-f64663d4e4afd64308f21d29e221794e",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-0598663189a357460"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ajmokskhc0180e4zw4td1ly09"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-f64663d4e4afd64308f21d29e221794e",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-0598663189a357460"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dh9fjkp0ddl1a0v6uzdesz3vw"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "875560960"
          } ]
        } ],
        "items" : [ {
          "name" : "service_health_suppression_zookeeper_canary_health",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-486d5634ff61c266e65468f40028b8ee",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-00724fd297c0f00de"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2ippg0uivd65tf7br2b8j5pu0"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-c7735b5e301e46551d021530f176f9e8",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0a36e1a1bf37a2cbb"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "59gste4ofmlpkswql0unys6rx"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-f64663d4e4afd64308f21d29e221794e",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0598663189a357460"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "65gv5zlrm1bc11anzoahjigzq"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-7-44.ap-southeast-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "silent"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "database_user",
          "value" : "huedb"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-486d5634ff61c266e65468f40028b8ee"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-486d5634ff61c266e65468f40028b8ee",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-00724fd297c0f00de"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "69c7ms9a0grpp0axoip9vq7tw"
          }, {
            "name" : "secret_key",
            "value" : "veEwn8aKofHLPG5cNXWWRGGLC5XnTt"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-7-42.ap-southeast-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "silent"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "ooziedb"
          }, {
            "name" : "role_health_suppression_oozie_server_web_metric_collection",
            "value" : "true"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-f64663d4e4afd64308f21d29e221794e",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-0598663189a357460"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2n7ovybwokeacf5a9xzfpxqd9"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "875560960"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "role_health_suppression_nodemanager_local_data_directories_free_space",
            "value" : "true"
          }, {
            "name" : "role_health_suppression_nodemanager_log_directories_free_space",
            "value" : "true"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/data/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/data/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "4527"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "875560960"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "4527"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "hWIgv9Q1iTTd3vztoMJXUPDaXWti6e"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-GATEWAY-486d5634ff61c266e65468f40028b8ee",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-00724fd297c0f00de"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-f64663d4e4afd64308f21d29e221794e",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-0598663189a357460"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dy0yptxtqhlde2p3ye6qeo6em"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-746675fa0ba9d0c97fb8782479545644",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0f3fd2f1af18c964e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4f096qiogpjaiowbvkfw8p9e"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-84297081ecfe5aa6c84770315d889413",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-09c31b64f43b1a9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1g58079af2jpt1xnv9klevfju"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-c7735b5e301e46551d021530f176f9e8",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0a36e1a1bf37a2cbb"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e3mra8pjylkxvdldjbsi3b6fr"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-f64663d4e4afd64308f21d29e221794e",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-0598663189a357460"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "81"
          }, {
            "name" : "role_jceks_password",
            "value" : "8ut6xyv203thz3qxdw5tz9u4w"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/data/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3157052211"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          }, {
            "name" : "role_health_suppression_datanode_data_directories_free_space",
            "value" : "true"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/data/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/data/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "role_health_suppression_name_node_ha_checkpoint_age",
            "value" : "true"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/data/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "875560960"
          } ]
        } ],
        "items" : [ {
          "name" : "core_site_safety_valve",
          "value" : "<property><name>fs.s3n.awsAccessKeyId</name><value>AKIAI4YRUHDASUYNLBBQ</value></property><property><name>fs.s3n.awsSecretAccessKey</name><value>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</value></property>"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "7XvTad6ByqBGFewWomaWjkvJRQNOFi"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "skjVkYxYUkNRZQPoMFFMNxgcLbP9tP"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "uD67uH2SmjVTOvWIMFTAlGWcmlfP9I"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-486d5634ff61c266e65468f40028b8ee",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-00724fd297c0f00de"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-746675fa0ba9d0c97fb8782479545644",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0f3fd2f1af18c964e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a3thpd72xancdmbv92xau4afk"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-84297081ecfe5aa6c84770315d889413",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-09c31b64f43b1a9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3e8j6jh211bu39x3dir1zjyw"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-c7735b5e301e46551d021530f176f9e8",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0a36e1a1bf37a2cbb"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ca2ypl27irw5mz0euk91g9qev"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-486d5634ff61c266e65468f40028b8ee",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-00724fd297c0f00de"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9ehbhhv3xcdzcb52s5edqfctl"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-f64663d4e4afd64308f21d29e221794e",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0598663189a357460"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "agpirmd3c0p81hs3rh7cyo7nl"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-486d5634ff61c266e65468f40028b8ee",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-00724fd297c0f00de"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "zek69tamomyhslimy8rjweem"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-746675fa0ba9d0c97fb8782479545644",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0f3fd2f1af18c964e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7harot8e43j1ww4mhil7gwhgf"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-84297081ecfe5aa6c84770315d889413",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-09c31b64f43b1a9ba"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "50pf01af2gwwd9ubr6rn6wkai"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-c7735b5e301e46551d021530f176f9e8",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0a36e1a1bf37a2cbb"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "n6dcp22xub9je0jlu40bsvmn"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-486d5634ff61c266e65468f40028b8ee",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-00724fd297c0f00de"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "namenodeHA"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "namenodeHA"
          }, {
            "name" : "namenode_id",
            "value" : "84"
          }, {
            "name" : "role_jceks_password",
            "value" : "7nwhjxmgx54q8vpj2j1r0zcpx"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-f64663d4e4afd64308f21d29e221794e",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0598663189a357460"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "namenodeHA"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "namenodeHA"
          }, {
            "name" : "namenode_id",
            "value" : "100"
          }, {
            "name" : "role_jceks_password",
            "value" : "7u36u1oqwj2ghte0hcytii8ww"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-0598663189a357460",
    "ipAddress" : "172.31.7.42",
    "hostname" : "ip-172-31-7-42.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0a36e1a1bf37a2cbb",
    "ipAddress" : "172.31.7.43",
    "hostname" : "ip-172-31-7-43.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-00724fd297c0f00de",
    "ipAddress" : "172.31.7.44",
    "hostname" : "ip-172-31-7-44.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-09c31b64f43b1a9ba",
    "ipAddress" : "172.31.7.45",
    "hostname" : "ip-172-31-7-45.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0f3fd2f1af18c964e",
    "ipAddress" : "172.31.7.46",
    "hostname" : "ip-172-31-7-46.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__71fbf038-8cff-4e2f-a3c3-4bb99748a673",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "be172a79112b6cc6b8bb808f4e47d2108d67afeda2f4d589195f0f18cd87b30f",
    "pwSalt" : 8530657443900610829,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-486d5634ff61c266e65468f40028b8ee",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b8a66f74984a9e09b03c53a2aedadce6c7615f25e4fae4066b01dad83a17dd85",
    "pwSalt" : -5504578255949994047,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-f64663d4e4afd64308f21d29e221794e",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "79dbb058e6ea43ce927aaf6245ef892bca28e6cc4ce6dcc9d7f8d527b6bb608d",
    "pwSalt" : -1167846691811313900,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-f64663d4e4afd64308f21d29e221794e",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f49210f94f146d4c5d8984f5025e8d0d6906e768058b2983a474d08410957ec8",
    "pwSalt" : 5416398694646329381,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-f64663d4e4afd64308f21d29e221794e",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f5aa14e674e1fc1bea287ea75f8916dfaad6e84a948d16a53057f8c18420463c",
    "pwSalt" : 6574492854630205693,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "e5f383670bd80dc1249ac71a24c07a02c32c9dd178d1ddad94961dc955bd6905",
    "pwSalt" : 4307588492051885034,
    "pwLogin" : true
  }, {
    "name" : "cm",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "dbb52843fe6782f4688fa7684c9a3ba28e3d69cf9f2460b393c375fc0d54e1c3",
    "pwSalt" : -4947859719332048433,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "60899c6d263e75ed407f3e7247e89603612811d486763c1f9878f175e857023c",
    "pwSalt" : -1900482732835905901,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20160916-1426",
    "gitHash" : "d23c620f3a3bbd85d8511d6ebba49beaaab14b75",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-7-44.ap-southeast-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "report"
        }, {
          "name" : "headlamp_database_password",
          "value" : "silent"
        }, {
          "name" : "headlamp_database_user",
          "value" : "reportdb"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "661651456"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-486d5634ff61c266e65468f40028b8ee",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-00724fd297c0f00de"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6fzollc1f2mxf9c5zcjttg66m"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-486d5634ff61c266e65468f40028b8ee",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-00724fd297c0f00de"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "d200ey0ajvpj1o71eu0eig662"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-f64663d4e4afd64308f21d29e221794e",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-0598663189a357460"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "12ru4dk1ld42w761y9lw3f2b7"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-f64663d4e4afd64308f21d29e221794e",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-0598663189a357460"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "244y2yvpu6nvsk5mscns3p1fh"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-f64663d4e4afd64308f21d29e221794e",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-0598663189a357460"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "aoc2bw08ts8omkh7jky36xbjj"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/27/2012 17:00"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://172.31.13.24/parcels/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
'''
