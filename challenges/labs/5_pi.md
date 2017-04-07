### Command
`[ec2-user@ip-10-146-51-155 ~]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar pi 8 2048`
 
 ### Output
 ```
Number of Maps  = 8
Samples per Map = 2048
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Starting Job
17/04/07 13:51:29 INFO client.RMProxy: Connecting to ResourceManager at ip-10-146-51-155.ec2.internal/10.146.51.155:8032
17/04/07 13:51:29 INFO hdfs.DFSClient: Created token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@DOUGSPADOTTOEMC.BR, renewer=yarn, realUser=, issueDate=1491587489662, maxDate=1492192289662, sequenceNumber=2, masterKeyId=2 on 10.146.51.155:8020
17/04/07 13:51:29 INFO security.TokenCache: Got dt for hdfs://ip-10-146-51-155.ec2.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.146.51.155:8020, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@DOUGSPADOTTOEMC.BR, renewer=yarn, realUser=, issueDate=1491587489662, maxDate=1492192289662, sequenceNumber=2, masterKeyId=2)
17/04/07 13:51:29 INFO input.FileInputFormat: Total input paths to process : 8
17/04/07 13:51:29 INFO mapreduce.JobSubmitter: number of splits:8
17/04/07 13:51:30 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1491586701749_0002
17/04/07 13:51:30 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.146.51.155:8020, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@DOUGSPADOTTOEMC.BR, renewer=yarn, realUser=, issueDate=1491587489662, maxDate=1492192289662, sequenceNumber=2, masterKeyId=2)
17/04/07 13:51:30 INFO impl.YarnClientImpl: Submitted application application_1491586701749_0002
17/04/07 13:51:30 INFO mapreduce.Job: The url to track the job: http://ip-10-146-51-155.ec2.internal:8088/proxy/application_1491586701749_0002/
17/04/07 13:51:30 INFO mapreduce.Job: Running job: job_1491586701749_0002
17/04/07 13:51:38 INFO mapreduce.Job: Job job_1491586701749_0002 running in uber mode : false
17/04/07 13:51:38 INFO mapreduce.Job:  map 0% reduce 0%
17/04/07 13:51:45 INFO mapreduce.Job:  map 25% reduce 0%
17/04/07 13:51:46 INFO mapreduce.Job:  map 38% reduce 0%
17/04/07 13:51:49 INFO mapreduce.Job:  map 63% reduce 0%
17/04/07 13:51:52 INFO mapreduce.Job:  map 100% reduce 0%
17/04/07 13:51:59 INFO mapreduce.Job:  map 100% reduce 100%
17/04/07 13:51:59 INFO mapreduce.Job: Job job_1491586701749_0002 completed successfully
17/04/07 13:51:59 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=94
                FILE: Number of bytes written=1135903
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=2296
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=35
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=8
                Launched reduce tasks=1
                Data-local map tasks=8
                Total time spent by all maps in occupied slots (ms)=68554
                Total time spent by all reduces in occupied slots (ms)=3565
                Total time spent by all map tasks (ms)=68554
                Total time spent by all reduce tasks (ms)=3565
                Total vcore-seconds taken by all map tasks=68554
                Total vcore-seconds taken by all reduce tasks=3565
                Total megabyte-seconds taken by all map tasks=70199296
                Total megabyte-seconds taken by all reduce tasks=3650560
        Map-Reduce Framework
                Map input records=8
                Map output records=16
                Map output bytes=144
                Map output materialized bytes=280
                Input split bytes=1352
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=280
                Reduce input records=16
                Reduce output records=0
                Spilled Records=32
                Shuffled Maps =8
                Failed Shuffles=0
                Merged Map outputs=8
                GC time elapsed (ms)=487
                CPU time spent (ms)=6580
                Physical memory (bytes) snapshot=3999903744
                Virtual memory (bytes) snapshot=14235037696
                Total committed heap usage (bytes)=4519886848
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=944
        File Output Format Counters
                Bytes Written=97
Job Finished in 29.846 seconds
Estimated value of Pi is 3.14111328125000000000
```