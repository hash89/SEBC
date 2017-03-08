{
  "timestamp" : "2017-03-07T22:52:34.530Z",
  "clusters" : [ {
    "name" : "hadrien",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "4331667456"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "3865470566"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "7390127718"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "409"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "1243"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "manager"
        }, {
          "name" : "hive_metastore_database_password",
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
        "name" : "hive-GATEWAY-0a08f646af3af74044b8ff51e017da68",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-bbe05f525ee3007a4516c95a1c98c1b0",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "32757190-8091-49f8-8c1c-d1d1d4c7a9d7"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-c73523af861eb3ba024550869b1acb7e",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "0451e04f-8f54-407b-881b-260f0627f931"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-cbaa1f0a95d16f6d7bcbf8ab6ec41d61",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "d793ed05-3d2c-4ff5-84c2-af64edaf9f78"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-e2ee137fc3a22bd5c397aa9d43d0631e",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "9563db2e-43be-4c4e-a0ef-3e1cbe2fda21"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-0a08f646af3af74044b8ff51e017da68",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "68elxf45aupj05960au5bduqn"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-e2ee137fc3a22bd5c397aa9d43d0631e",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "9563db2e-43be-4c4e-a0ef-3e1cbe2fda21"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "af6uxa7cpdeccpe7zffpl2rph"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-bbe05f525ee3007a4516c95a1c98c1b0",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "32757190-8091-49f8-8c1c-d1d1d4c7a9d7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aqzdnh3rhze2xtp6s4zw0pmxy"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-c73523af861eb3ba024550869b1acb7e",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "0451e04f-8f54-407b-881b-260f0627f931"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1sscdqh5vdnk9z6fdu6hr7zex"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-cbaa1f0a95d16f6d7bcbf8ab6ec41d61",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "d793ed05-3d2c-4ff5-84c2-af64edaf9f78"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "alrooq7qg66n783xpbzcbusg7"
          }, {
            "name" : "serverId",
            "value" : "2"
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
          "value" : "manager"
        }, {
          "name" : "database_password",
          "value" : "hue"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-e2ee137fc3a22bd5c397aa9d43d0631e"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-0a08f646af3af74044b8ff51e017da68",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "33z2tnx7vfqso1pfssq2d8uen"
          }, {
            "name" : "secret_key",
            "value" : "Kei21Nvp4sK8ksxMOJJjLHYpcnbaob"
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
            "value" : "manager"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
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
        "name" : "oozie-OOZIE_SERVER-0a08f646af3af74044b8ff51e017da68",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "231pq8qv1iu6cqjfxnpntfdbz"
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
            "value" : "12"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
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
            "value" : "7"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "15918"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "15918"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "7"
          }, {
            "name" : "yarn_scheduler_minimum_allocation_mb",
            "value" : "2048"
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
          "name" : "yarn_fs_scheduled_allocations",
          "value" : "{\"defaultFairSharePreemptionThreshold\":null,\"defaultFairSharePreemptionTimeout\":null,\"defaultMinSharePreemptionTimeout\":null,\"defaultQueueSchedulingPolicy\":\"drf\",\"queueMaxAMShareDefault\":null,\"queueMaxAppsDefault\":null,\"queuePlacementRules\":[{\"create\":true,\"name\":\"specified\",\"queue\":null,\"rules\":null},{\"create\":null,\"name\":\"nestedUserQueue\",\"queue\":null,\"rules\":[{\"create\":null,\"name\":\"default\",\"queue\":\"users\",\"rules\":null}]},{\"create\":null,\"name\":\"default\",\"queue\":null,\"rules\":null}],\"queues\":[{\"aclAdministerApps\":\"*\",\"aclSubmitApps\":\" \",\"allowPreemptionFrom\":null,\"fairSharePreemptionThreshold\":null,\"fairSharePreemptionTimeout\":null,\"minSharePreemptionTimeout\":null,\"name\":\"root\",\"queues\":[{\"aclAdministerApps\":\"*\",\"aclSubmitApps\":\"*\",\"allowPreemptionFrom\":null,\"fairSharePreemptionThreshold\":null,\"fairSharePreemptionTimeout\":null,\"minSharePreemptionTimeout\":null,\"name\":\"default\",\"queues\":[],\"schedulablePropertiesList\":[{\"impalaDefaultQueryMemLimit\":null,\"impalaDefaultQueryOptions\":null,\"impalaMaxMemory\":null,\"impalaMaxQueuedQueries\":null,\"impalaMaxRunningQueries\":null,\"impalaQueueTimeout\":null,\"maxAMShare\":null,\"maxResources\":null,\"maxRunningApps\":null,\"minResources\":null,\"scheduleName\":\"default\",\"weight\":1.0}],\"schedulingPolicy\":\"drf\",\"type\":null},{\"aclAdministerApps\":\"*\",\"aclSubmitApps\":\"*\",\"allowPreemptionFrom\":null,\"fairSharePreemptionThreshold\":null,\"fairSharePreemptionTimeout\":null,\"minSharePreemptionTimeout\":null,\"name\":\"users\",\"queues\":[],\"schedulablePropertiesList\":[{\"impalaDefaultQueryMemLimit\":null,\"impalaDefaultQueryOptions\":null,\"impalaMaxMemory\":null,\"impalaMaxQueuedQueries\":null,\"impalaMaxRunningQueries\":null,\"impalaQueueTimeout\":null,\"maxAMShare\":null,\"maxResources\":null,\"maxRunningApps\":null,\"minResources\":null,\"scheduleName\":\"default\",\"weight\":4.0}],\"schedulingPolicy\":\"drf\",\"type\":\"parent\"}],\"schedulablePropertiesList\":[{\"impalaDefaultQueryMemLimit\":null,\"impalaDefaultQueryOptions\":null,\"impalaMaxMemory\":null,\"impalaMaxQueuedQueries\":null,\"impalaMaxRunningQueries\":null,\"impalaQueueTimeout\":null,\"maxAMShare\":null,\"maxResources\":null,\"maxRunningApps\":null,\"minResources\":null,\"scheduleName\":\"default\",\"weight\":1.0}],\"schedulingPolicy\":\"drf\",\"type\":null}],\"userMaxAppsDefault\":null,\"users\":[]}"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "VGNckQAiONmVmke35scvBGkSmtuKia"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-0a08f646af3af74044b8ff51e017da68",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dgposq4ct7dvz1ufi2w2pgjfd"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-bbe05f525ee3007a4516c95a1c98c1b0",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "32757190-8091-49f8-8c1c-d1d1d4c7a9d7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1r27f8e75l3cf0gsi9aakf74a"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-c73523af861eb3ba024550869b1acb7e",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "0451e04f-8f54-407b-881b-260f0627f931"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6f0gqerro2gndzgjpir2zfxe8"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-cbaa1f0a95d16f6d7bcbf8ab6ec41d61",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "d793ed05-3d2c-4ff5-84c2-af64edaf9f78"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ifrz1qt0rudqrx4u8va33ype"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-e2ee137fc3a22bd5c397aa9d43d0631e",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "9563db2e-43be-4c4e-a0ef-3e1cbe2fda21"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "151"
          }, {
            "name" : "role_jceks_password",
            "value" : "41ue5gi9zjnshbbmxcezfodt7"
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
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
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
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/data/dfs/snn"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "dNWNbee9a0eGctMyQgRpzr7XWdnrxB"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "dfs_namenode_acls_enabled",
          "value" : "true"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "PVHaJoXaQ6031JqVMIKPYAM4zQQDUK"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "dW6SLbusKaWTFZ1yCzqbvpFaQXvmKw"
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
        "name" : "hdfs-BALANCER-0a08f646af3af74044b8ff51e017da68",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-bbe05f525ee3007a4516c95a1c98c1b0",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "32757190-8091-49f8-8c1c-d1d1d4c7a9d7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "715erdbxeuba2xe48sq66c6uh"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-c73523af861eb3ba024550869b1acb7e",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "0451e04f-8f54-407b-881b-260f0627f931"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9lqp7svsugzy8bu34bg2e6zjg"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-cbaa1f0a95d16f6d7bcbf8ab6ec41d61",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "d793ed05-3d2c-4ff5-84c2-af64edaf9f78"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ga38694kphpyp2laa1swie3i"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-0a08f646af3af74044b8ff51e017da68",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "f1socwy57oqi5oj6j9mxk747"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-e2ee137fc3a22bd5c397aa9d43d0631e",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "9563db2e-43be-4c4e-a0ef-3e1cbe2fda21"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3hi8n8xg4v21wyiu3401j2sgh"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-bbe05f525ee3007a4516c95a1c98c1b0",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "32757190-8091-49f8-8c1c-d1d1d4c7a9d7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bd4tv426vev6oytjlkmof3y8r"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-c73523af861eb3ba024550869b1acb7e",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "0451e04f-8f54-407b-881b-260f0627f931"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3tdhtiotnh3tbdgyvo4cwq1px"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-cbaa1f0a95d16f6d7bcbf8ab6ec41d61",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "d793ed05-3d2c-4ff5-84c2-af64edaf9f78"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a2yxw9ec8w99e0nci28vlyakx"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-0a08f646af3af74044b8ff51e017da68",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "161"
          }, {
            "name" : "role_jceks_password",
            "value" : "cy8ta159e0iqge30yp4d8zf83"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-e2ee137fc3a22bd5c397aa9d43d0631e",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "9563db2e-43be-4c4e-a0ef-3e1cbe2fda21"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "156"
          }, {
            "name" : "role_jceks_password",
            "value" : "a76e86pykdychv4kacs4q3i6z"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-bbe05f525ee3007a4516c95a1c98c1b0",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "32757190-8091-49f8-8c1c-d1d1d4c7a9d7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2q8h29xw6zlwbpdn0istft49q"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-c73523af861eb3ba024550869b1acb7e",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "0451e04f-8f54-407b-881b-260f0627f931"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ez8bz37shwjljs981emha42ez"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-cbaa1f0a95d16f6d7bcbf8ab6ec41d61",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "d793ed05-3d2c-4ff5-84c2-af64edaf9f78"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4gd9vlbedui4969feutp4qiji"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f",
    "ipAddress" : "192.168.3.5",
    "hostname" : "manager",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "9563db2e-43be-4c4e-a0ef-3e1cbe2fda21",
    "ipAddress" : "192.168.3.6",
    "hostname" : "master",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "d793ed05-3d2c-4ff5-84c2-af64edaf9f78",
    "ipAddress" : "192.168.3.4",
    "hostname" : "worker1",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "0451e04f-8f54-407b-881b-260f0627f931",
    "ipAddress" : "192.168.3.3",
    "hostname" : "worker2",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "32757190-8091-49f8-8c1c-d1d1d4c7a9d7",
    "ipAddress" : "192.168.3.7",
    "hostname" : "worker3",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-0a08f646af3af74044b8ff51e017da68",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "6e0073b1aad038a53f974aabef78f34a4956ecd0f5c2776be93b2cd9897dbcbb",
    "pwSalt" : -6436140918297839611,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-0a08f646af3af74044b8ff51e017da68",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "028b202c8a25b308f6d21411f33ba89731525dee0244faa9aba03025f01f23dc",
    "pwSalt" : -7104529936527979618,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-0a08f646af3af74044b8ff51e017da68",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "070807c5aad87a9e15f04628bbc21a91ff3f6b29a750ce1c3a8ea55ff9a32de3",
    "pwSalt" : 4171205031468847444,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-0a08f646af3af74044b8ff51e017da68",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "8cfd0907e42c951ead72d9f4645a26774be2a5553806b21e4b4d8e1e2fd17de0",
    "pwSalt" : 1571508406943924752,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-0a08f646af3af74044b8ff51e017da68",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "de053acf9298b5cc6beaed4079c34486b8916c713a147e1b75038a4fca8d2c83",
    "pwSalt" : -2280062806641015282,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "c2b5a712c5ca9b33831cebce3f3a7c79e91af324518a22123d25e6599d650c0a",
    "pwSalt" : -5837076034357463580,
    "pwLogin" : true
  }, {
    "name" : "hadrien",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "59b68fec0896120ef0d2d88f156ad9ab61e2dd8d692e218e90473472db570075",
    "pwSalt" : 4904273053084548072,
    "pwLogin" : true
  }, {
    "name" : "minotaur ",
    "roles" : [ "ROLE_OPERATOR" ],
    "pwHash" : "58754ec9737fccea74a810d93a5870ff8d30bcd7ebdf0a7a56e52c6e32610d89",
    "pwSalt" : 5013923119374249285,
    "pwLogin" : true
  }, {
    "name" : "minotaur2",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "320fb2b0362f7d87949eff64bdd1ffed361167b9abe1d4cb9a344194691f28e8",
    "pwSalt" : 8481805111931286874,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161019-1013",
    "gitHash" : "518f0d6d44abc87bc392646e4369a20c8192b7cf",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "manager"
        }, {
          "name" : "firehose_database_name",
          "value" : "amon"
        }, {
          "name" : "firehose_database_password",
          "value" : "amon"
        }, {
          "name" : "firehose_database_user",
          "value" : "amon"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "manager"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-0a08f646af3af74044b8ff51e017da68",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "e53rqd7hpiw9lp3gqzvcwl4ns"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-0a08f646af3af74044b8ff51e017da68",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "e67yfhpeudlchmzn52anp3fp9"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-0a08f646af3af74044b8ff51e017da68",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dele4jve3q43f4tn290z4cnnc"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-0a08f646af3af74044b8ff51e017da68",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2x5we00yb37whj7aiqkb8zrvy"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-0a08f646af3af74044b8ff51e017da68",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5apxiorzhrjf2ak6b5kxspwpt"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-0a08f646af3af74044b8ff51e017da68",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "b1336861-337e-4cbb-a777-7e38d742506f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "cz9x6w86euocj6krp7betly09"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/21/2012 3:40"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "NOT_ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}