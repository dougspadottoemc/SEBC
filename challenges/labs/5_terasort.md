### Command
`hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort tgen640 tsort640m`

### Output
``
17/04/07 13:43:34 INFO terasort.TeraSort: starting
17/04/07 13:43:35 INFO hdfs.DFSClient: Created token for neymar: HDFS_DELEGATION_TOKEN owner=ne                                                                                              ymar@DOUGSPADOTTOEMC.BR, renewer=yarn, realUser=, issueDate=1491587015930, maxDate=149219181593                                                                                              0, sequenceNumber=1, masterKeyId=2 on 10.146.51.155:8020
17/04/07 13:43:35 INFO security.TokenCache: Got dt for hdfs://ip-10-146-51-155.ec2.internal:802                                                                                              0; Kind: HDFS_DELEGATION_TOKEN, Service: 10.146.51.155:8020, Ident: (token for neymar: HDFS_DEL                                                                                              EGATION_TOKEN owner=neymar@DOUGSPADOTTOEMC.BR, renewer=yarn, realUser=, issueDate=1491587015930                                                                                              , maxDate=1492191815930, sequenceNumber=1, masterKeyId=2)
17/04/07 13:43:36 INFO input.FileInputFormat: Total input paths to process : 8
Spent 487ms computing base-splits.
Spent 7ms computing TeraScheduler splits.
Computing input splits took 495ms
Sampling 10 splits of 392
Making 8 from 100000 sampled records
Computing parititions took 1013ms
Spent 1510ms computing partitions.
17/04/07 13:43:37 INFO client.RMProxy: Connecting to ResourceManager at ip-10-146-51-155.ec2.in                                                                                              ternal/10.146.51.155:8032
17/04/07 13:43:37 INFO mapreduce.JobSubmitter: number of splits:392
17/04/07 13:43:37 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1491586701749_000                                                                                              1
17/04/07 13:43:37 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.146.51.                                                                                              155:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@DOUGSPADOTTOEMC.BR, rene                                                                                              wer=yarn, realUser=, issueDate=1491587015930, maxDate=1492191815930, sequenceNumber=1, masterKe                                                                                              yId=2)
17/04/07 13:43:39 INFO impl.YarnClientImpl: Submitted application application_1491586701749_000                                                                                              1
17/04/07 13:43:39 INFO mapreduce.Job: The url to track the job: http://ip-10-146-51-155.ec2.int                                                                                              ernal:8088/proxy/application_1491586701749_0001/
17/04/07 13:43:39 INFO mapreduce.Job: Running job: job_1491586701749_0001
17/04/07 13:43:49 INFO mapreduce.Job: Job job_1491586701749_0001 running in uber mode : false
17/04/07 13:43:49 INFO mapreduce.Job:  map 0% reduce 0%
17/04/07 13:43:59 INFO mapreduce.Job:  map 1% reduce 0%
17/04/07 13:44:05 INFO mapreduce.Job:  map 2% reduce 0%
17/04/07 13:44:08 INFO mapreduce.Job:  map 3% reduce 0%
17/04/07 13:44:09 INFO mapreduce.Job:  map 4% reduce 0%
17/04/07 13:44:13 INFO mapreduce.Job:  map 5% reduce 0%
17/04/07 13:44:16 INFO mapreduce.Job:  map 6% reduce 0%
17/04/07 13:44:22 INFO mapreduce.Job:  map 7% reduce 0%
17/04/07 13:44:23 INFO mapreduce.Job:  map 8% reduce 0%
17/04/07 13:44:25 INFO mapreduce.Job:  map 9% reduce 0%
17/04/07 13:44:29 INFO mapreduce.Job:  map 10% reduce 0%
17/04/07 13:44:34 INFO mapreduce.Job:  map 11% reduce 0%
17/04/07 13:44:35 INFO mapreduce.Job:  map 12% reduce 0%
17/04/07 13:44:37 INFO mapreduce.Job:  map 13% reduce 0%
17/04/07 13:44:41 INFO mapreduce.Job:  map 14% reduce 0%
17/04/07 13:44:43 INFO mapreduce.Job:  map 15% reduce 0%
17/04/07 13:44:48 INFO mapreduce.Job:  map 16% reduce 0%
17/04/07 13:44:49 INFO mapreduce.Job:  map 17% reduce 0%
17/04/07 13:44:52 INFO mapreduce.Job:  map 18% reduce 0%
17/04/07 13:44:58 INFO mapreduce.Job:  map 19% reduce 0%
17/04/07 13:44:59 INFO mapreduce.Job:  map 20% reduce 0%
17/04/07 13:45:02 INFO mapreduce.Job:  map 21% reduce 0%
17/04/07 13:45:07 INFO mapreduce.Job:  map 22% reduce 0%
17/04/07 13:45:10 INFO mapreduce.Job:  map 23% reduce 0%
17/04/07 13:45:11 INFO mapreduce.Job:  map 24% reduce 0%
17/04/07 13:45:15 INFO mapreduce.Job:  map 25% reduce 0%
17/04/07 13:45:18 INFO mapreduce.Job:  map 26% reduce 0%
17/04/07 13:45:19 INFO mapreduce.Job:  map 27% reduce 0%
17/04/07 13:45:24 INFO mapreduce.Job:  map 28% reduce 0%
17/04/07 13:45:26 INFO mapreduce.Job:  map 29% reduce 0%
17/04/07 13:45:29 INFO mapreduce.Job:  map 30% reduce 0%
17/04/07 13:45:35 INFO mapreduce.Job:  map 31% reduce 0%
17/04/07 13:45:36 INFO mapreduce.Job:  map 32% reduce 0%
17/04/07 13:45:37 INFO mapreduce.Job:  map 33% reduce 0%
17/04/07 13:45:41 INFO mapreduce.Job:  map 34% reduce 0%
17/04/07 13:45:48 INFO mapreduce.Job:  map 36% reduce 0%
17/04/07 13:45:49 INFO mapreduce.Job:  map 37% reduce 0%
17/04/07 13:45:54 INFO mapreduce.Job:  map 38% reduce 0%
17/04/07 13:45:57 INFO mapreduce.Job:  map 39% reduce 0%
17/04/07 13:46:00 INFO mapreduce.Job:  map 40% reduce 0%
17/04/07 13:46:02 INFO mapreduce.Job:  map 41% reduce 0%
17/04/07 13:46:05 INFO mapreduce.Job:  map 42% reduce 0%
17/04/07 13:46:09 INFO mapreduce.Job:  map 43% reduce 0%
17/04/07 13:46:13 INFO mapreduce.Job:  map 44% reduce 0%
17/04/07 13:46:14 INFO mapreduce.Job:  map 45% reduce 0%
17/04/07 13:46:16 INFO mapreduce.Job:  map 46% reduce 0%
17/04/07 13:46:22 INFO mapreduce.Job:  map 47% reduce 0%
17/04/07 13:46:23 INFO mapreduce.Job:  map 48% reduce 0%
17/04/07 13:46:25 INFO mapreduce.Job:  map 49% reduce 0%
17/04/07 13:46:30 INFO mapreduce.Job:  map 50% reduce 0%
17/04/07 13:46:33 INFO mapreduce.Job:  map 51% reduce 0%
17/04/07 13:46:36 INFO mapreduce.Job:  map 52% reduce 0%
17/04/07 13:46:38 INFO mapreduce.Job:  map 53% reduce 0%
17/04/07 13:46:42 INFO mapreduce.Job:  map 54% reduce 0%
17/04/07 13:46:44 INFO mapreduce.Job:  map 55% reduce 0%
17/04/07 13:46:49 INFO mapreduce.Job:  map 56% reduce 0%
17/04/07 13:46:50 INFO mapreduce.Job:  map 57% reduce 0%
17/04/07 13:46:53 INFO mapreduce.Job:  map 58% reduce 0%
17/04/07 13:46:57 INFO mapreduce.Job:  map 59% reduce 0%
17/04/07 13:47:00 INFO mapreduce.Job:  map 60% reduce 0%
17/04/07 13:47:02 INFO mapreduce.Job:  map 61% reduce 0%
17/04/07 13:47:05 INFO mapreduce.Job:  map 62% reduce 0%
17/04/07 13:47:09 INFO mapreduce.Job:  map 63% reduce 0%
17/04/07 13:47:12 INFO mapreduce.Job:  map 64% reduce 0%
17/04/07 13:47:13 INFO mapreduce.Job:  map 65% reduce 0%
17/04/07 13:47:16 INFO mapreduce.Job:  map 66% reduce 0%
17/04/07 13:47:21 INFO mapreduce.Job:  map 67% reduce 0%
17/04/07 13:47:24 INFO mapreduce.Job:  map 68% reduce 0%
17/04/07 13:47:26 INFO mapreduce.Job:  map 69% reduce 0%
17/04/07 13:47:28 INFO mapreduce.Job:  map 70% reduce 0%
17/04/07 13:47:33 INFO mapreduce.Job:  map 71% reduce 0%
17/04/07 13:47:36 INFO mapreduce.Job:  map 72% reduce 0%
17/04/07 13:47:38 INFO mapreduce.Job:  map 73% reduce 0%
17/04/07 13:47:41 INFO mapreduce.Job:  map 74% reduce 0%
17/04/07 13:47:45 INFO mapreduce.Job:  map 75% reduce 0%
17/04/07 13:47:46 INFO mapreduce.Job:  map 76% reduce 0%
17/04/07 13:47:50 INFO mapreduce.Job:  map 77% reduce 0%
17/04/07 13:47:51 INFO mapreduce.Job:  map 78% reduce 0%
17/04/07 13:47:55 INFO mapreduce.Job:  map 79% reduce 0%
17/04/07 13:48:00 INFO mapreduce.Job:  map 80% reduce 0%
17/04/07 13:48:02 INFO mapreduce.Job:  map 81% reduce 0%
17/04/07 13:48:04 INFO mapreduce.Job:  map 82% reduce 0%
17/04/07 13:48:09 INFO mapreduce.Job:  map 83% reduce 0%
17/04/07 13:48:12 INFO mapreduce.Job:  map 84% reduce 0%
17/04/07 13:48:14 INFO mapreduce.Job:  map 85% reduce 0%
17/04/07 13:48:23 INFO mapreduce.Job:  map 85% reduce 7%
17/04/07 13:48:24 INFO mapreduce.Job:  map 85% reduce 11%
17/04/07 13:48:26 INFO mapreduce.Job:  map 86% reduce 11%
17/04/07 13:48:28 INFO mapreduce.Job:  map 86% reduce 18%
17/04/07 13:48:29 INFO mapreduce.Job:  map 87% reduce 25%
17/04/07 13:48:35 INFO mapreduce.Job:  map 88% reduce 25%
17/04/07 13:48:38 INFO mapreduce.Job:  map 89% reduce 25%
17/04/07 13:48:40 INFO mapreduce.Job:  map 89% reduce 26%
17/04/07 13:48:46 INFO mapreduce.Job:  map 90% reduce 26%
17/04/07 13:48:47 INFO mapreduce.Job:  map 91% reduce 26%
17/04/07 13:48:53 INFO mapreduce.Job:  map 92% reduce 27%
17/04/07 13:48:57 INFO mapreduce.Job:  map 93% reduce 27%
17/04/07 13:49:03 INFO mapreduce.Job:  map 94% reduce 27%
17/04/07 13:49:07 INFO mapreduce.Job:  map 95% reduce 27%
17/04/07 13:49:11 INFO mapreduce.Job:  map 95% reduce 28%
17/04/07 13:49:12 INFO mapreduce.Job:  map 96% reduce 28%
17/04/07 13:49:17 INFO mapreduce.Job:  map 97% reduce 28%
17/04/07 13:49:22 INFO mapreduce.Job:  map 98% reduce 28%
17/04/07 13:49:27 INFO mapreduce.Job:  map 99% reduce 28%
17/04/07 13:49:28 INFO mapreduce.Job:  map 99% reduce 29%
17/04/07 13:49:30 INFO mapreduce.Job:  map 100% reduce 29%
17/04/07 13:49:34 INFO mapreduce.Job:  map 100% reduce 32%
17/04/07 13:49:35 INFO mapreduce.Job:  map 100% reduce 46%
17/04/07 13:49:36 INFO mapreduce.Job:  map 100% reduce 50%
17/04/07 13:49:40 INFO mapreduce.Job:  map 100% reduce 63%
17/04/07 13:49:41 INFO mapreduce.Job:  map 100% reduce 68%
17/04/07 13:49:42 INFO mapreduce.Job:  map 100% reduce 70%
17/04/07 13:49:44 INFO mapreduce.Job:  map 100% reduce 78%
17/04/07 13:49:46 INFO mapreduce.Job:  map 100% reduce 93%
17/04/07 13:49:47 INFO mapreduce.Job:  map 100% reduce 94%
17/04/07 13:49:48 INFO mapreduce.Job:  map 100% reduce 96%
17/04/07 13:49:50 INFO mapreduce.Job:  map 100% reduce 98%
17/04/07 13:49:55 INFO mapreduce.Job:  map 100% reduce 100%
17/04/07 13:49:56 INFO mapreduce.Job: Job job_1491586701749_0001 completed successfully
17/04/07 13:49:57 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2908717120
                FILE: Number of bytes written=5802693699
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553654488
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=1200
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=392
                Launched reduce tasks=8
                Data-local map tasks=392
                Total time spent by all maps in occupied slots (ms)=3344319
                Total time spent by all reduces in occupied slots (ms)=722552
                Total time spent by all map tasks (ms)=3344319
                Total time spent by all reduce tasks (ms)=722552
                Total vcore-seconds taken by all map tasks=3344319
                Total vcore-seconds taken by all reduce tasks=722552
                Total megabyte-seconds taken by all map tasks=3424582656
                Total megabyte-seconds taken by all reduce tasks=739893248
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2843187873
                Input split bytes=54488
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2843187873
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =3136
                Failed Shuffles=0
                Merged Map outputs=3136
                GC time elapsed (ms)=49009
                CPU time spent (ms)=1506850
                Physical memory (bytes) snapshot=192506941440
                Virtual memory (bytes) snapshot=630698692608
                Total committed heap usage (bytes)=223917637632
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=6553600000
        File Output Format Counters
                Bytes Written=6553600000
17/04/07 13:49:57 INFO terasort.TeraSort: done
``
