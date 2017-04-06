### Initial show tables

```
[root@ip-10-179-156-49 /]# beeline
Beeline version 1.1.0-cdh5.10.1 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-10-179-156-49.ec2.internal@CLOUDERA.BOOTCAMP
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-10-179-156-49.ec2.internal@CLOUDERA.BOOTCAMP
Connected to: Apache Hive (version 1.1.0-cdh5.10.1)
Driver: Hive JDBC (version 1.1.0-cdh5.10.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170405220101_4bed6fd1-4a2d-4c74-930f-707291196045): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170405220101_4bed6fd1-4a2d-4c74-930f-707291196045); Time taken: 0.77 seconds
INFO  : Executing command(queryId=hive_20170405220101_4bed6fd1-4a2d-4c74-930f-707291196045): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170405220101_4bed6fd1-4a2d-4c74-930f-707291196045); Time taken: 0.437 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.597 seconds)

```

### George, reader of default

```
[root@ip-10-179-156-49 ~]# kinit george
Password for george@CLOUDERA.BOOTCAMP:
[root@ip-10-179-156-49 ~]# beeline
Beeline version 1.1.0-cdh5.10.1 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-10-179-                                                                                                             156-49.ec2.internal@CLOUDERA.BOOTCAMP
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-10-179-156-                                                                                                             49.ec2.internal@CLOUDERA.BOOTCAMP
Connected to: Apache Hive (version 1.1.0-cdh5.10.1)
Driver: Hive JDBC (version 1.1.0-cdh5.10.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170405221818_0494b833-a6e9-4e6f-bc9b-6c                                                                                                             0643b9dadd): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, t                                                                                                             ype:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170405221818_0494b833-a6e9-4e                                                                                                             6f-bc9b-6c0643b9dadd); Time taken: 0.074 seconds
INFO  : Executing command(queryId=hive_20170405221818_0494b833-a6e9-4e6f-bc9b-6c                                                                                                             0643b9dadd): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170405221818_0494b833-a6e9-4e                                                                                                             6f-bc9b-6c0643b9dadd); Time taken: 0.161 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.341 seconds)
```

### Ferdinand, inserter only on sample_07 
```
[root@ip-10-179-156-49 ~]# kinit ferdinand
Password for ferdinand@CLOUDERA.BOOTCAMP:
[root@ip-10-179-156-49 ~]# beeline
Beeline version 1.1.0-cdh5.10.1 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-10-179-                                                                                                             156-49.ec2.internal@CLOUDERA.BOOTCAMP
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-10-179-156-                                                                                                             49.ec2.internal@CLOUDERA.BOOTCAMP
Connected to: Apache Hive (version 1.1.0-cdh5.10.1)
Driver: Hive JDBC (version 1.1.0-cdh5.10.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170405221414_f381642a-c66b-4cb5-8abe-94                                                                                                             addfd612d2): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, t                                                                                                             ype:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170405221414_f381642a-c66b-4c                                                                                                             b5-8abe-94addfd612d2); Time taken: 0.07 seconds
INFO  : Executing command(queryId=hive_20170405221414_f381642a-c66b-4cb5-8abe-94                                                                                                             addfd612d2): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170405221414_f381642a-c66b-4c                                                                                                             b5-8abe-94addfd612d2); Time taken: 0.153 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.329 seconds)
```
