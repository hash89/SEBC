## Terasort kerberised
Command `$> time hadoop jar /opt/cloudera/parcels/CDH-5.9.1-1.cdh5.9.1.p0.4/jars/hadoop-examples.jar terasort tgen640 tsort640m`

Result :
```
INFO terasort.TeraSort: starting
17/03/10 10:19:47 INFO hdfs.DFSClient: Created token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@HASH89.ES, renewer=yarn, realUser=, issueDate=1489141186934, maxDate=1489745986934, sequenceNumber=1, masterKeyId=2 on 192.168.3.6:8020
17/03/10 10:19:47 INFO security.TokenCache: Got dt for hdfs://manager:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 192.168.3.6:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@HASH89.ES, renewer=yarn, realUser=, issueDate=1489141186934, maxDate=1489745986934, sequenceNumber=1, masterKeyId=2)
17/03/10 10:19:47 INFO input.FileInputFormat: Total input paths to process : 8
Spent 372ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 377ms
Sampling 10 splits of 392
Making 6 from 100000 sampled records
Computing parititions took 595ms
Spent 973ms computing partitions.
17/03/10 10:19:47 INFO client.RMProxy: Connecting to ResourceManager at master/192.168.3.4:8032
17/03/10 10:19:48 INFO mapreduce.JobSubmitter: number of splits:392
17/03/10 10:19:48 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489140967203_0001
17/03/10 10:19:48 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 192.168.3.6:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@HASH89.ES, renewer=yarn, realUser=, issueDate=1489141186934, maxDate=1489745986934, sequenceNumber=1, masterKeyId=2)
17/03/10 10:19:49 INFO impl.YarnClientImpl: Submitted application application_1489140967203_0001
17/03/10 10:19:49 INFO mapreduce.Job: The url to track the job: http://master:8088/proxy/application_1489140967203_0001/
17/03/10 10:19:49 INFO mapreduce.Job: Running job: job_1489140967203_0001
17/03/10 10:19:56 INFO mapreduce.Job: Job job_1489140967203_0001 running in uber mode : false
17/03/10 10:19:56 INFO mapreduce.Job:  map 0% reduce 0%
17/03/10 10:20:03 INFO mapreduce.Job:  map 1% reduce 0%
17/03/10 10:20:06 INFO mapreduce.Job:  map 2% reduce 0%
17/03/10 10:20:07 INFO mapreduce.Job:  map 3% reduce 0%
17/03/10 10:20:12 INFO mapreduce.Job:  map 5% reduce 0%
17/03/10 10:20:17 INFO mapreduce.Job:  map 6% reduce 0%
17/03/10 10:20:18 INFO mapreduce.Job:  map 7% reduce 0%
17/03/10 10:20:20 INFO mapreduce.Job:  map 8% reduce 0%
17/03/10 10:20:24 INFO mapreduce.Job:  map 9% reduce 0%
17/03/10 10:20:25 INFO mapreduce.Job:  map 10% reduce 0%
17/03/10 10:20:31 INFO mapreduce.Job:  map 12% reduce 0%
17/03/10 10:20:33 INFO mapreduce.Job:  map 13% reduce 0%
17/03/10 10:20:37 INFO mapreduce.Job:  map 14% reduce 0%
17/03/10 10:20:38 INFO mapreduce.Job:  map 15% reduce 0%
17/03/10 10:20:42 INFO mapreduce.Job:  map 16% reduce 0%
17/03/10 10:20:43 INFO mapreduce.Job:  map 17% reduce 0%
17/03/10 10:20:46 INFO mapreduce.Job:  map 18% reduce 0%
17/03/10 10:20:50 INFO mapreduce.Job:  map 20% reduce 0%
17/03/10 10:20:55 INFO mapreduce.Job:  map 21% reduce 0%
17/03/10 10:20:56 INFO mapreduce.Job:  map 22% reduce 0%
17/03/10 10:20:59 INFO mapreduce.Job:  map 23% reduce 0%
17/03/10 10:21:02 INFO mapreduce.Job:  map 24% reduce 0%
17/03/10 10:21:03 INFO mapreduce.Job:  map 25% reduce 0%
17/03/10 10:21:06 INFO mapreduce.Job:  map 26% reduce 0%
17/03/10 10:21:08 INFO mapreduce.Job:  map 27% reduce 0%
17/03/10 10:21:10 INFO mapreduce.Job:  map 28% reduce 0%
17/03/10 10:21:13 INFO mapreduce.Job:  map 29% reduce 0%
17/03/10 10:21:14 INFO mapreduce.Job:  map 30% reduce 0%
17/03/10 10:21:19 INFO mapreduce.Job:  map 31% reduce 0%
17/03/10 10:21:20 INFO mapreduce.Job:  map 32% reduce 0%
17/03/10 10:21:24 INFO mapreduce.Job:  map 33% reduce 0%
17/03/10 10:21:26 INFO mapreduce.Job:  map 34% reduce 0%
17/03/10 10:21:29 INFO mapreduce.Job:  map 35% reduce 0%
17/03/10 10:21:31 INFO mapreduce.Job:  map 36% reduce 0%
17/03/10 10:21:33 INFO mapreduce.Job:  map 37% reduce 0%
17/03/10 10:21:38 INFO mapreduce.Job:  map 38% reduce 0%
17/03/10 10:21:39 INFO mapreduce.Job:  map 39% reduce 0%
17/03/10 10:21:40 INFO mapreduce.Job:  map 40% reduce 0%
17/03/10 10:21:44 INFO mapreduce.Job:  map 41% reduce 0%
17/03/10 10:21:45 INFO mapreduce.Job:  map 42% reduce 0%
17/03/10 10:21:50 INFO mapreduce.Job:  map 44% reduce 0%
17/03/10 10:21:55 INFO mapreduce.Job:  map 45% reduce 0%
17/03/10 10:21:56 INFO mapreduce.Job:  map 46% reduce 0%
17/03/10 10:21:57 INFO mapreduce.Job:  map 47% reduce 0%
17/03/10 10:22:02 INFO mapreduce.Job:  map 49% reduce 0%
17/03/10 10:22:07 INFO mapreduce.Job:  map 50% reduce 0%
17/03/10 10:22:08 INFO mapreduce.Job:  map 51% reduce 0%
17/03/10 10:22:10 INFO mapreduce.Job:  map 52% reduce 0%
17/03/10 10:22:13 INFO mapreduce.Job:  map 53% reduce 0%
17/03/10 10:22:15 INFO mapreduce.Job:  map 54% reduce 0%
17/03/10 10:22:20 INFO mapreduce.Job:  map 56% reduce 0%
17/03/10 10:22:22 INFO mapreduce.Job:  map 57% reduce 0%
17/03/10 10:22:25 INFO mapreduce.Job:  map 58% reduce 0%
17/03/10 10:22:26 INFO mapreduce.Job:  map 59% reduce 0%
17/03/10 10:22:32 INFO mapreduce.Job:  map 60% reduce 0%
17/03/10 10:22:33 INFO mapreduce.Job:  map 61% reduce 0%
17/03/10 10:22:36 INFO mapreduce.Job:  map 62% reduce 0%
17/03/10 10:22:38 INFO mapreduce.Job:  map 63% reduce 0%
17/03/10 10:22:39 INFO mapreduce.Job:  map 64% reduce 0%
17/03/10 10:22:44 INFO mapreduce.Job:  map 65% reduce 0%
17/03/10 10:22:45 INFO mapreduce.Job:  map 66% reduce 0%
17/03/10 10:22:48 INFO mapreduce.Job:  map 67% reduce 0%
17/03/10 10:22:51 INFO mapreduce.Job:  map 69% reduce 0%
17/03/10 10:22:56 INFO mapreduce.Job:  map 70% reduce 0%
17/03/10 10:22:57 INFO mapreduce.Job:  map 71% reduce 0%
17/03/10 10:23:01 INFO mapreduce.Job:  map 72% reduce 0%
17/03/10 10:23:03 INFO mapreduce.Job:  map 73% reduce 0%
17/03/10 10:23:06 INFO mapreduce.Job:  map 74% reduce 0%
17/03/10 10:23:08 INFO mapreduce.Job:  map 75% reduce 0%
17/03/10 10:23:09 INFO mapreduce.Job:  map 76% reduce 0%
17/03/10 10:23:13 INFO mapreduce.Job:  map 77% reduce 0%
17/03/10 10:23:15 INFO mapreduce.Job:  map 78% reduce 0%
17/03/10 10:23:16 INFO mapreduce.Job:  map 79% reduce 0%
17/03/10 10:23:20 INFO mapreduce.Job:  map 80% reduce 0%
17/03/10 10:23:21 INFO mapreduce.Job:  map 81% reduce 0%
17/03/10 10:23:25 INFO mapreduce.Job:  map 82% reduce 0%
17/03/10 10:23:28 INFO mapreduce.Job:  map 83% reduce 0%
17/03/10 10:23:33 INFO mapreduce.Job:  map 84% reduce 0%
17/03/10 10:23:36 INFO mapreduce.Job:  map 84% reduce 7%
17/03/10 10:23:38 INFO mapreduce.Job:  map 84% reduce 13%
17/03/10 10:23:39 INFO mapreduce.Job:  map 85% reduce 18%
17/03/10 10:23:41 INFO mapreduce.Job:  map 85% reduce 21%
17/03/10 10:23:42 INFO mapreduce.Job:  map 85% reduce 23%
17/03/10 10:23:43 INFO mapreduce.Job:  map 86% reduce 23%
17/03/10 10:23:45 INFO mapreduce.Job:  map 86% reduce 24%
17/03/10 10:23:47 INFO mapreduce.Job:  map 87% reduce 24%
17/03/10 10:23:50 INFO mapreduce.Job:  map 88% reduce 24%
17/03/10 10:23:55 INFO mapreduce.Job:  map 89% reduce 24%
17/03/10 10:23:56 INFO mapreduce.Job:  map 89% reduce 25%
17/03/10 10:24:00 INFO mapreduce.Job:  map 90% reduce 25%
17/03/10 10:24:05 INFO mapreduce.Job:  map 91% reduce 25%
17/03/10 10:24:09 INFO mapreduce.Job:  map 92% reduce 25%
17/03/10 10:24:12 INFO mapreduce.Job:  map 92% reduce 26%
17/03/10 10:24:13 INFO mapreduce.Job:  map 93% reduce 26%
17/03/10 10:24:17 INFO mapreduce.Job:  map 94% reduce 26%
17/03/10 10:24:22 INFO mapreduce.Job:  map 95% reduce 26%
17/03/10 10:24:27 INFO mapreduce.Job:  map 96% reduce 26%
17/03/10 10:24:30 INFO mapreduce.Job:  map 96% reduce 27%
17/03/10 10:24:32 INFO mapreduce.Job:  map 97% reduce 27%
17/03/10 10:24:37 INFO mapreduce.Job:  map 98% reduce 27%
17/03/10 10:24:42 INFO mapreduce.Job:  map 99% reduce 27%
17/03/10 10:24:45 INFO mapreduce.Job:  map 99% reduce 28%
17/03/10 10:24:47 INFO mapreduce.Job:  map 100% reduce 28%
17/03/10 10:24:48 INFO mapreduce.Job:  map 100% reduce 44%
17/03/10 10:24:50 INFO mapreduce.Job:  map 100% reduce 58%
17/03/10 10:24:51 INFO mapreduce.Job:  map 100% reduce 62%
17/03/10 10:24:53 INFO mapreduce.Job:  map 100% reduce 66%
17/03/10 10:24:54 INFO mapreduce.Job:  map 100% reduce 74%
17/03/10 10:24:56 INFO mapreduce.Job:  map 100% reduce 78%
17/03/10 10:24:57 INFO mapreduce.Job:  map 100% reduce 85%
17/03/10 10:24:58 INFO mapreduce.Job:  map 100% reduce 86%
17/03/10 10:24:59 INFO mapreduce.Job:  map 100% reduce 88%
17/03/10 10:25:00 INFO mapreduce.Job:  map 100% reduce 89%
17/03/10 10:25:03 INFO mapreduce.Job:  map 100% reduce 95%
17/03/10 10:25:06 INFO mapreduce.Job:  map 100% reduce 97%
17/03/10 10:25:09 INFO mapreduce.Job:  map 100% reduce 99%
17/03/10 10:25:12 INFO mapreduce.Job:  map 100% reduce 100%
17/03/10 10:25:12 INFO mapreduce.Job: Job job_1489140967203_0001 completed successfully
17/03/10 10:25:12 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2914131515
                FILE: Number of bytes written=5806881143
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553645864
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=1194
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=392
                Launched reduce tasks=6
                Data-local map tasks=392
                Total time spent by all maps in occupied slots (ms)=1738912
                Total time spent by all reduces in occupied slots (ms)=478287
                Total time spent by all map tasks (ms)=1738912
                Total time spent by all reduce tasks (ms)=478287
                Total vcore-seconds taken by all map tasks=1738912
                Total vcore-seconds taken by all reduce tasks=478287
                Total megabyte-seconds taken by all map tasks=1780645888
                Total megabyte-seconds taken by all reduce tasks=489765888
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2843199072
                Input split bytes=45864
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2843199072
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =2352
                Failed Shuffles=0
                Merged Map outputs=2352
                GC time elapsed (ms)=25117
                CPU time spent (ms)=871870
                Physical memory (bytes) snapshot=197422424064
                Virtual memory (bytes) snapshot=630040301568
                Total committed heap usage (bytes)=230563512320
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
17/03/10 10:25:12 INFO terasort.TeraSort: done

real    5m27.801s
user    0m6.287s
sys     0m0.392s
```
