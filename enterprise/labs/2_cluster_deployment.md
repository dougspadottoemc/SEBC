
` [ec2-user@ip-10-179-156-49 ~]$ curl -X GET -u "dougspadottoemc:cloudera" -i http://ec2-23-22-152-100.compute-1.amazonaws.com:7180/api/v2/cm/deployment `

``` HTTP/1.1 200 OK

Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=1hmd8jiaidohm14vo7k4ojo5g0;Path=/;HttpOnly
Content-Type: application/json
Date: Wed, 05 Apr 2017 13:07:45 GMT
Transfer-Encoding: chunked
Server: Jetty(6.1.26.cloudera.4)

{
  "timestamp" : "2017-04-05T13:07:44.989Z",
  "clusters" : [ {
    "name" : "dougspadottoemc",
    "version" : "CDH5",
    "services" : [ {
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
            "value" : "/dfs/dn1"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "8588674252"
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
            "value" : "/jn/edits"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn1"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn1"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "QjyIhQDULlFIu62Xshs32JPUY6EEre"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "bfO9cVyRvykugTXYooVZoYzlZXYn7X"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "U62jXw1dvXJxijnTH7hGtwbIdvoYHc"
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
        "name" : "hdfs-BALANCER-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-3c5aebf5cb1306e9b452b69e6a63b84f",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "65461979-bc0c-4d9e-8156-c9ad4203598e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "35elv556i4xd93hnqyhlz4ddx"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-b703c02679ba9f49263df0978c692d9b",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "8743d4e1-4bb6-4bb1-a48f-95f3d1e80ed5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dr7ut63skrr5opzs2dvx1n68l"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-ce7bbe6ba0ba658228d1d7799ae519ee",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "74d7883c-ac6b-4a9b-988f-be2ae6b71c11"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2hwdp38veutdwowyjn1728wep"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-d45096e224585b1232c846bccaeb6f47",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "6ff5c4c1-57d6-4a6f-8817-cea98b066c82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a0glsoh13w8bbxha4v27ja7yn"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-3c5aebf5cb1306e9b452b69e6a63b84f",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "65461979-bc0c-4d9e-8156-c9ad4203598e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e9c3ug2d9th26jadup7tswlcg"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7n0bo4u32w9a224p1efc6alsy"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-3c5aebf5cb1306e9b452b69e6a63b84f",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "65461979-bc0c-4d9e-8156-c9ad4203598e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e5537ihdtf7uqhpgtrmh6r6c1"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-3c5aebf5cb1306e9b452b69e6a63b84f",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "65461979-bc0c-4d9e-8156-c9ad4203598e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5afnhz0wwf885ruwjjex8uhdj"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1o3bxt5sjb1po5npdqhedmzmn"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-ce7bbe6ba0ba658228d1d7799ae519ee",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "74d7883c-ac6b-4a9b-988f-be2ae6b71c11"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6vpfkytptevy7cjo9jcb0w9fe"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-3c5aebf5cb1306e9b452b69e6a63b84f",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "65461979-bc0c-4d9e-8156-c9ad4203598e"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "hdfsdsemcha"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "hdfsdsemcha"
          }, {
            "name" : "namenode_id",
            "value" : "201"
          }, {
            "name" : "role_jceks_password",
            "value" : "3dmjq7ng5oby9gpitmdicip9w"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "hdfsdsemcha"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "hdfsdsemcha"
          }, {
            "name" : "namenode_id",
            "value" : "157"
          }, {
            "name" : "role_jceks_password",
            "value" : "3rptkz5vofpauz1qm51qyb0jz"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "8"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
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
            "value" : "/yarn/nm1"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "10752"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "52428800"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "8192"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "cm_yarn_container_usage_input_dir",
          "value" : "/tmp/cmYarnContainerMetrics1"
        }, {
          "name" : "cm_yarn_container_usage_output_dir",
          "value" : "/tmp/cmYarnContainerMetricsAggregate1"
        }, {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
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
          "value" : "v9VeRguBsVX7JxcFDTr1D63G3pW2JK"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-3c5aebf5cb1306e9b452b69e6a63b84f",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "65461979-bc0c-4d9e-8156-c9ad4203598e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "22rlv2fg71aqanm2vxny5dmwf"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-3c5aebf5cb1306e9b452b69e6a63b84f",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "65461979-bc0c-4d9e-8156-c9ad4203598e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2k1ux5qktm11eez13kf1ya1ir"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-b703c02679ba9f49263df0978c692d9b",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "8743d4e1-4bb6-4bb1-a48f-95f3d1e80ed5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d788maoir9g4mwg8kt5tsuadj"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-ce7bbe6ba0ba658228d1d7799ae519ee",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "74d7883c-ac6b-4a9b-988f-be2ae6b71c11"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2qoccjsqc892kuoqhnbyk0wsm"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-d45096e224585b1232c846bccaeb6f47",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "6ff5c4c1-57d6-4a6f-8817-cea98b066c82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1vzee4a5c3znbm0j3pyxu8or"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "174"
          }, {
            "name" : "role_jceks_password",
            "value" : "by24z6g98ildiq431ein9k4vq"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-10-179-156-49.ec2.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie_admin"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "52428800"
          } ]
        } ],
        "items" : [ {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8dmnrbilbe0baipeess7nppbd"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "52428800"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "52428800"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "3214881587"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "541"
          } ]
        }, {
          "roleType" : "WEBHCAT",
          "items" : [ {
            "name" : "hive_webhcat_java_heapsize",
            "value" : "52428800"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-10-179-156-49.ec2.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive_admin"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-3c5aebf5cb1306e9b452b69e6a63b84f",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "65461979-bc0c-4d9e-8156-c9ad4203598e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-b703c02679ba9f49263df0978c692d9b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "8743d4e1-4bb6-4bb1-a48f-95f3d1e80ed5"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-ce7bbe6ba0ba658228d1d7799ae519ee",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "74d7883c-ac6b-4a9b-988f-be2ae6b71c11"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-d45096e224585b1232c846bccaeb6f47",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "6ff5c4c1-57d6-4a6f-8817-cea98b066c82"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5gqknfznsrosngxd4gbnnf8zj"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4njbpw4o7p8ovtxmmga7i5lze"
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "WEBHCAT",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_webhcat_secret_key",
            "value" : "bq2uSkE74VKcfkZ9VOU37eCFqHToq4"
          }, {
            "name" : "role_jceks_password",
            "value" : "bgttdyhdwu49d7ve7z02e312k"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HUE_SERVER",
          "items" : [ {
            "name" : "hue_server_bind_wildcard",
            "value" : "true"
          } ]
        } ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-10-179-156-49.ec2.internal"
        }, {
          "name" : "database_password",
          "value" : "hue_admin"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-3c5aebf5cb1306e9b452b69e6a63b84f"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eno9spp80lnhdv8rl8x9ts58r"
          }, {
            "name" : "secret_key",
            "value" : "mbqAJC2tvLSHGdt4ZNz8J7YPw0fzDx"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "52428800"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-3c5aebf5cb1306e9b452b69e6a63b84f",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "65461979-bc0c-4d9e-8156-c9ad4203598e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7409fojsj40ipetl2bxm7vv4f"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-a89c5c6d0abf925e2a0511b2019dba01",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1bmt7lfdzjfnz7oyw2o0tg1ym"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-ce7bbe6ba0ba658228d1d7799ae519ee",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "74d7883c-ac6b-4a9b-988f-be2ae6b71c11"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cxml36lw3nc44fkuiaakq16n3"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579",
    "ipAddress" : "10.179.156.49",
    "hostname" : "ip-10-179-156-49.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "65461979-bc0c-4d9e-8156-c9ad4203598e",
    "ipAddress" : "10.183.49.219",
    "hostname" : "ip-10-183-49-219.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "74d7883c-ac6b-4a9b-988f-be2ae6b71c11",
    "ipAddress" : "10.186.166.75",
    "hostname" : "ip-10-186-166-75.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "8743d4e1-4bb6-4bb1-a48f-95f3d1e80ed5",
    "ipAddress" : "10.47.192.27",
    "hostname" : "ip-10-47-192-27.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "6ff5c4c1-57d6-4a6f-8817-cea98b066c82",
    "ipAddress" : "10.51.221.228",
    "hostname" : "ip-10-51-221-228.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-a89c5c6d0abf925e2a0511b2019dba01",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "93c89ba21f7bd19719b2c81aca87b14b6bcf137c765215b7746c3e41c14671a5",
    "pwSalt" : 369587309488758146,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-a89c5c6d0abf925e2a0511b2019dba01",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f42c605f84bae961f9d75f5728aa0eb6d3b63abec1f74a2837c86a89352669a9",
    "pwSalt" : -6792359844466168296,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-a89c5c6d0abf925e2a0511b2019dba01",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "defe24092af12a01f137612030c78e36d15ace2a1655bc7bb29db473f2b1c5d8",
    "pwSalt" : 4254815060193445887,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-a89c5c6d0abf925e2a0511b2019dba01",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "08bdb0993498a7b25fbf0dbe787f9bda2fb3591c28e7454c0f7b7054a3ee1570",
    "pwSalt" : -5585674934563716767,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-a89c5c6d0abf925e2a0511b2019dba01",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "9f94659095d57b6b9a340337a13476c5cd02ce68c19ec281e02f80ea7adcd35b",
    "pwSalt" : -492685144056083263,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "d717fd8e1c251f010a1304347efce6d7e5ac4dde8dae68c6991c1f118ed2e584",
    "pwSalt" : -1868296934557885087,
    "pwLogin" : true
  }, {
    "name" : "dougspadottoemc",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "7b6897be53885368a4dd4689d69d0b7a0f54ef56befe6b5ea170e8c88e612f68",
    "pwSalt" : 3688189136542015501,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "d0bd5853131fd1d3a883a1658ecfde4b90c24ea16f6ee6072f3d576716668e46",
    "pwSalt" : -5052172633151724778,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.10.1",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170319-2001",
    "gitHash" : "f226435f6fa5f545543c00245900ae43bea7a29c",
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
          "value" : "ip-10-179-156-49.ec2.internal"
        }, {
          "name" : "firehose_database_name",
          "value" : "amon"
        }, {
          "name" : "firehose_database_password",
          "value" : "amon_admin"
        }, {
          "name" : "firehose_database_user",
          "value" : "amon"
        }, {
          "name" : "firehose_heapsize",
          "value" : "620756992"
        } ]
      }, {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "620756992"
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
          "value" : "ip-10-179-156-49.ec2.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman_admin"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "620756992"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ {
        "name" : "service_health_suppression_mgmt_embedded_db_free_space",
        "value" : "true"
      } ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-a89c5c6d0abf925e2a0511b2019dba01",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "d4kyyymy07y7y5slmj3jhvo10"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-a89c5c6d0abf925e2a0511b2019dba01",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "b2ylx7d5jmq4fy67uzw44rwb0"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-a89c5c6d0abf925e2a0511b2019dba01",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4plm0301vgy95jbk3kj9uly1d"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-a89c5c6d0abf925e2a0511b2019dba01",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dldy6cwe83q2l0rvyiishd9rm"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-a89c5c6d0abf925e2a0511b2019dba01",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "a8nj5549piaoxl5mb3p5lqxzl"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-a89c5c6d0abf925e2a0511b2019dba01",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6mkzhbijmyl8tg178gihdr005"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 1:40"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://ec2-23-22-152-100.compute-1.amazonaws.com/cdh5.10/,http://ec2-23-22-152-100.compute-1.amazonaws.com/gpl_extras"
    } ]
  } ```