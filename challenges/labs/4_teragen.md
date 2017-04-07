### Teragen
```
[neymar@ip-10-181-102-132 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=8 -Ddfs.block.size=16777216 65536000 /user/neymar/tgen640
17/04/07 12:49:26 INFO client.RMProxy: Connecting to ResourceManager at ip-10-146-51-155.ec2.internal/10.146.51.155:8032
17/04/07 12:49:27 INFO terasort.TeraGen: Generating 65536000 using 8
17/04/07 12:49:27 INFO mapreduce.JobSubmitter: number of splits:8
17/04/07 12:49:27 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/04/07 12:49:27 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/04/07 12:49:27 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1491582511297_0001
17/04/07 12:49:28 INFO impl.YarnClientImpl: Submitted application application_1491582511297_0001
17/04/07 12:49:28 INFO mapreduce.Job: The url to track the job: http://ip-10-146-51-155.ec2.internal:8088/proxy/application_1491582511297_0001/
17/04/07 12:49:28 INFO mapreduce.Job: Running job: job_1491582511297_0001
17/04/07 12:49:35 INFO mapreduce.Job: Job job_1491582511297_0001 running in uber mode : false
17/04/07 12:49:35 INFO mapreduce.Job:  map 0% reduce 0%
17/04/07 12:49:53 INFO mapreduce.Job:  map 8% reduce 0%
17/04/07 12:49:54 INFO mapreduce.Job:  map 27% reduce 0%
17/04/07 12:49:55 INFO mapreduce.Job:  map 30% reduce 0%
17/04/07 12:49:59 INFO mapreduce.Job:  map 31% reduce 0%
17/04/07 12:50:01 INFO mapreduce.Job:  map 32% reduce 0%
17/04/07 12:50:06 INFO mapreduce.Job:  map 33% reduce 0%
17/04/07 12:50:07 INFO mapreduce.Job:  map 34% reduce 0%
17/04/07 12:50:23 INFO mapreduce.Job:  map 35% reduce 0%
17/04/07 12:50:24 INFO mapreduce.Job:  map 37% reduce 0%
17/04/07 12:50:29 INFO mapreduce.Job:  map 40% reduce 0%
17/04/07 12:50:30 INFO mapreduce.Job:  map 47% reduce 0%
17/04/07 12:50:35 INFO mapreduce.Job:  map 49% reduce 0%
17/04/07 12:50:36 INFO mapreduce.Job:  map 52% reduce 0%
17/04/07 12:50:42 INFO mapreduce.Job:  map 53% reduce 0%
17/04/07 12:50:53 INFO mapreduce.Job:  map 54% reduce 0%
17/04/07 12:50:54 INFO mapreduce.Job:  map 57% reduce 0%
17/04/07 12:51:00 INFO mapreduce.Job:  map 58% reduce 0%
17/04/07 12:51:06 INFO mapreduce.Job:  map 59% reduce 0%
17/04/07 12:51:07 INFO mapreduce.Job:  map 60% reduce 0%
17/04/07 12:51:13 INFO mapreduce.Job:  map 61% reduce 0%
17/04/07 12:51:18 INFO mapreduce.Job:  map 63% reduce 0%
17/04/07 12:51:19 INFO mapreduce.Job:  map 70% reduce 0%
17/04/07 12:51:24 INFO mapreduce.Job:  map 71% reduce 0%
17/04/07 12:51:25 INFO mapreduce.Job:  map 74% reduce 0%
17/04/07 12:51:30 INFO mapreduce.Job:  map 75% reduce 0%
17/04/07 12:51:31 INFO mapreduce.Job:  map 76% reduce 0%
17/04/07 12:51:37 INFO mapreduce.Job:  map 78% reduce 0%
17/04/07 12:51:42 INFO mapreduce.Job:  map 79% reduce 0%
17/04/07 12:51:43 INFO mapreduce.Job:  map 82% reduce 0%
17/04/07 12:51:49 INFO mapreduce.Job:  map 84% reduce 0%
17/04/07 12:51:54 INFO mapreduce.Job:  map 86% reduce 0%
17/04/07 12:51:55 INFO mapreduce.Job:  map 91% reduce 0%
17/04/07 12:52:01 INFO mapreduce.Job:  map 94% reduce 0%
17/04/07 12:52:05 INFO mapreduce.Job:  map 95% reduce 0%
17/04/07 12:52:06 INFO mapreduce.Job:  map 98% reduce 0%
17/04/07 12:52:07 INFO mapreduce.Job:  map 100% reduce 0%
17/04/07 12:52:07 INFO mapreduce.Job: Job job_1491582511297_0001 completed successfully
17/04/07 12:52:07 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=997632
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=682
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=32
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=8
                Other local map tasks=8
                Total time spent by all maps in occupied slots (ms)=1179031
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=1179031
                Total vcore-seconds taken by all map tasks=1179031
                Total megabyte-seconds taken by all map tasks=1207327744
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=682
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1518
                CPU time spent (ms)=145330
                Physical memory (bytes) snapshot=2732240896
                Virtual memory (bytes) snapshot=12663369728
                Total committed heap usage (bytes)=2832203776
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000
```

### Time for Teragen
```
real    2m43.137s
user    0m6.488s
sys     0m0.320s
```

### hdfs to the output dir
```
[neymar@ip-10-181-102-132 ~]$ hdfs dfs -ls /user/neymar/tgen640
Found 9 items
-rw-r--r--   3 neymar merengues          0 2017-04-07 12:52 /user/neymar/tgen640/_SUCCESS
-rw-r--r--   3 neymar merengues  819200000 2017-04-07 12:52 /user/neymar/tgen640/part-m-00000
-rw-r--r--   3 neymar merengues  819200000 2017-04-07 12:52 /user/neymar/tgen640/part-m-00001
-rw-r--r--   3 neymar merengues  819200000 2017-04-07 12:52 /user/neymar/tgen640/part-m-00002
-rw-r--r--   3 neymar merengues  819200000 2017-04-07 12:52 /user/neymar/tgen640/part-m-00003
-rw-r--r--   3 neymar merengues  819200000 2017-04-07 12:52 /user/neymar/tgen640/part-m-00004
-rw-r--r--   3 neymar merengues  819200000 2017-04-07 12:51 /user/neymar/tgen640/part-m-00005
-rw-r--r--   3 neymar merengues  819200000 2017-04-07 12:52 /user/neymar/tgen640/part-m-00006
-rw-r--r--   3 neymar merengues  819200000 2017-04-07 12:52 /user/neymar/tgen640/part-m-00007
```

### Blocks on the directory
```
[neymar@ip-10-181-102-132 ~]$ hdfs  fsck /user/neymar/tgen640 -blocks
Connecting to namenode via http://ip-10-146-51-155.ec2.internal:50070
FSCK started by neymar (auth:SIMPLE) from /10.181.102.132 for path /user/neymar/tgen640 at Fri Apr 07 12:55:28 EDT 2017
.........Status: HEALTHY
 Total size:    6553600000 B
 Total dirs:    1
 Total files:   9
 Total symlinks:                0
 Total blocks (validated):      392 (avg. block size 16718367 B)
 Minimally replicated blocks:   392 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Fri Apr 07 12:55:28 EDT 2017 in 21 milliseconds


The filesystem under path '/user/neymar/tgen640' is HEALTHY
```