## Pi program
Command : `$> time hadoop jar /opt/cloudera/parcels/CDH-5.9.1-1.cdh5.9.1.p0.4/jars/hadoop-examples.jar pi 10 10`

Result :
```
Number of Maps  = 10
Samples per Map = 100
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Starting Job
17/03/10 10:26:34 INFO client.RMProxy: Connecting to ResourceManager at master/192.168.3.4:8032
17/03/10 10:26:35 INFO hdfs.DFSClient: Created token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@HASH89.ES, renewer=yarn, realUser=, issueDate=1489141595009, maxDate=1489746395009, sequenceNumber=2, masterKeyId=2 on 192.168.3.6:8020
17/03/10 10:26:35 INFO security.TokenCache: Got dt for hdfs://manager:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 192.168.3.6:8020, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@HASH89.ES, renewer=yarn, realUser=, issueDate=1489141595009, maxDate=1489746395009, sequenceNumber=2, masterKeyId=2)
17/03/10 10:26:35 INFO input.FileInputFormat: Total input paths to process : 10
17/03/10 10:26:35 INFO mapreduce.JobSubmitter: number of splits:10
17/03/10 10:26:35 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489140967203_0002
17/03/10 10:26:35 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 192.168.3.6:8020, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@HASH89.ES, renewer=yarn, realUser=, issueDate=1489141595009, maxDate=1489746395009, sequenceNumber=2, masterKeyId=2)
17/03/10 10:26:35 INFO impl.YarnClientImpl: Submitted application application_1489140967203_0002
17/03/10 10:26:35 INFO mapreduce.Job: The url to track the job: http://master:8088/proxy/application_1489140967203_0002/
17/03/10 10:26:35 INFO mapreduce.Job: Running job: job_1489140967203_0002
17/03/10 10:26:42 INFO mapreduce.Job: Job job_1489140967203_0002 running in uber mode : false
17/03/10 10:26:42 INFO mapreduce.Job:  map 0% reduce 0%
17/03/10 10:26:48 INFO mapreduce.Job:  map 20% reduce 0%
17/03/10 10:26:51 INFO mapreduce.Job:  map 50% reduce 0%
17/03/10 10:26:52 INFO mapreduce.Job:  map 100% reduce 0%
17/03/10 10:26:57 INFO mapreduce.Job:  map 100% reduce 100%
17/03/10 10:26:57 INFO mapreduce.Job: Job job_1489140967203_0002 completed successfully
17/03/10 10:26:57 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=97
                FILE: Number of bytes written=1361313
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=2650
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=43
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=10
                Launched reduce tasks=1
                Data-local map tasks=10
                Total time spent by all maps in occupied slots (ms)=56113
                Total time spent by all reduces in occupied slots (ms)=2647
                Total time spent by all map tasks (ms)=56113
                Total time spent by all reduce tasks (ms)=2647
                Total vcore-seconds taken by all map tasks=56113
                Total vcore-seconds taken by all reduce tasks=2647
                Total megabyte-seconds taken by all map tasks=57459712
                Total megabyte-seconds taken by all reduce tasks=2710528
        Map-Reduce Framework
                Map input records=10
                Map output records=20
                Map output bytes=180
                Map output materialized bytes=340
                Input split bytes=1470
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=340
                Reduce input records=20
                Reduce output records=0
                Spilled Records=40
                Shuffled Maps =10
                Failed Shuffles=0
                Merged Map outputs=10
                GC time elapsed (ms)=299
                CPU time spent (ms)=5250
                Physical memory (bytes) snapshot=4771491840
                Virtual memory (bytes) snapshot=17338126336
                Total committed heap usage (bytes)=5819072512
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1180
        File Output Format Counters
                Bytes Written=97
Job Finished in 22.32 seconds
Estimated value of Pi is 3.14800000000000000000

real    0m24.712s
user    0m3.999s
sys     0m0.237s
```
