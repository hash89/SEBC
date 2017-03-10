# Teragen work

## The command
`$> sudo su neymar; cd;`

`$> time hadoop jar /opt/cloudera/parcels/CDH-5.9.1-1.cdh5.9.1.p0.4/jars/hadoop-examples.jar teragen -Dmapreduce.job.maps=8 -Ddfs.block.size=16777216 65536000 tgen640`

## Result
```
17/03/10 09:13:47 INFO client.RMProxy: Connecting to ResourceManager at master/192.168.3.4:8032
17/03/10 09:13:48 INFO terasort.TeraSort: Generating 65536000 using 8
17/03/10 09:13:48 INFO mapreduce.JobSubmitter: number of splits:8
17/03/10 09:13:48 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/03/10 09:13:48 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489136075627_0002
17/03/10 09:13:48 INFO impl.YarnClientImpl: Submitted application application_1489136075627_0002
17/03/10 09:13:48 INFO mapreduce.Job: The url to track the job: http://master:8088/proxy/application_1489136075627_0002/
17/03/10 09:13:48 INFO mapreduce.Job: Running job: job_1489136075627_0002
17/03/10 09:13:53 INFO mapreduce.Job: Job job_1489136075627_0002 running in uber mode : false
17/03/10 09:13:53 INFO mapreduce.Job:  map 0% reduce 0%
17/03/10 09:14:04 INFO mapreduce.Job:  map 2% reduce 0%
17/03/10 09:14:05 INFO mapreduce.Job:  map 8% reduce 0%
17/03/10 09:14:06 INFO mapreduce.Job:  map 11% reduce 0%
17/03/10 09:14:07 INFO mapreduce.Job:  map 14% reduce 0%
17/03/10 09:14:08 INFO mapreduce.Job:  map 17% reduce 0%
17/03/10 09:14:09 INFO mapreduce.Job:  map 19% reduce 0%
17/03/10 09:14:10 INFO mapreduce.Job:  map 21% reduce 0%
17/03/10 09:14:11 INFO mapreduce.Job:  map 24% reduce 0%
17/03/10 09:14:12 INFO mapreduce.Job:  map 25% reduce 0%
17/03/10 09:14:13 INFO mapreduce.Job:  map 27% reduce 0%
17/03/10 09:14:14 INFO mapreduce.Job:  map 31% reduce 0%
17/03/10 09:14:15 INFO mapreduce.Job:  map 32% reduce 0%
17/03/10 09:14:16 INFO mapreduce.Job:  map 35% reduce 0%
17/03/10 09:14:17 INFO mapreduce.Job:  map 37% reduce 0%
17/03/10 09:14:18 INFO mapreduce.Job:  map 39% reduce 0%
17/03/10 09:14:19 INFO mapreduce.Job:  map 42% reduce 0%
17/03/10 09:14:20 INFO mapreduce.Job:  map 44% reduce 0%
17/03/10 09:14:21 INFO mapreduce.Job:  map 46% reduce 0%
17/03/10 09:14:22 INFO mapreduce.Job:  map 49% reduce 0%
17/03/10 09:14:23 INFO mapreduce.Job:  map 51% reduce 0%
17/03/10 09:14:24 INFO mapreduce.Job:  map 53% reduce 0%
17/03/10 09:14:25 INFO mapreduce.Job:  map 56% reduce 0%
17/03/10 09:14:26 INFO mapreduce.Job:  map 57% reduce 0%
17/03/10 09:14:27 INFO mapreduce.Job:  map 59% reduce 0%
17/03/10 09:14:28 INFO mapreduce.Job:  map 61% reduce 0%
17/03/10 09:14:29 INFO mapreduce.Job:  map 63% reduce 0%
17/03/10 09:14:30 INFO mapreduce.Job:  map 64% reduce 0%
17/03/10 09:14:31 INFO mapreduce.Job:  map 67% reduce 0%
17/03/10 09:14:32 INFO mapreduce.Job:  map 70% reduce 0%
17/03/10 09:14:33 INFO mapreduce.Job:  map 72% reduce 0%
17/03/10 09:14:34 INFO mapreduce.Job:  map 74% reduce 0%
17/03/10 09:14:35 INFO mapreduce.Job:  map 77% reduce 0%
17/03/10 09:14:36 INFO mapreduce.Job:  map 79% reduce 0%
17/03/10 09:14:37 INFO mapreduce.Job:  map 80% reduce 0%
17/03/10 09:14:38 INFO mapreduce.Job:  map 82% reduce 0%
17/03/10 09:14:39 INFO mapreduce.Job:  map 84% reduce 0%
17/03/10 09:14:40 INFO mapreduce.Job:  map 85% reduce 0%
17/03/10 09:14:41 INFO mapreduce.Job:  map 87% reduce 0%
17/03/10 09:14:42 INFO mapreduce.Job:  map 89% reduce 0%
17/03/10 09:14:43 INFO mapreduce.Job:  map 90% reduce 0%
17/03/10 09:14:44 INFO mapreduce.Job:  map 92% reduce 0%
17/03/10 09:14:45 INFO mapreduce.Job:  map 94% reduce 0%
17/03/10 09:14:46 INFO mapreduce.Job:  map 95% reduce 0%
17/03/10 09:14:47 INFO mapreduce.Job:  map 97% reduce 0%
17/03/10 09:14:48 INFO mapreduce.Job:  map 99% reduce 0%
17/03/10 09:14:49 INFO mapreduce.Job:  map 100% reduce 0%
17/03/10 09:14:49 INFO mapreduce.Job: Job job_1489136075627_0002 completed successfully
17/03/10 09:14:49 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=978528
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
                Total time spent by all maps in occupied slots (ms)=392079
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=392079
                Total vcore-seconds taken by all map tasks=392079
                Total megabyte-seconds taken by all map tasks=401488896
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=682
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1066
                CPU time spent (ms)=97510
                Physical memory (bytes) snapshot=2463002624
                Virtual memory (bytes) snapshot=12626149376
                Total committed heap usage (bytes)=2697986048
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

real    1m3.397s
user    0m4.294s
sys     0m0.260s
```

## Time command

```
real    1m3.397s
user    0m4.294s
sys     0m0.260s
```

## Listing tgen640
`$> hdfs dfs -ls /user/neymar/tgen640`

result :
```
Found 9 items
-rw-r--r--   3 neymar neymar          0 2017-03-10 09:14 /user/neymar/tgen640/_SUCCESS
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:14 /user/neymar/tgen640/part-m-00000
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:14 /user/neymar/tgen640/part-m-00001
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:14 /user/neymar/tgen640/part-m-00002
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:14 /user/neymar/tgen640/part-m-00003
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:14 /user/neymar/tgen640/part-m-00004
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:14 /user/neymar/tgen640/part-m-00005
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:14 /user/neymar/tgen640/part-m-00006
-rw-r--r--   3 neymar neymar  819200000 2017-03-10 09:14 /user/neymar/tgen640/part-m-00007
```

## Blocks
`$> hdfs fsck /user/neymar/tgen640 -blocks`

Result :
```
Connecting to namenode via http://manager:50070
FSCK started by neymar (auth:SIMPLE) from /192.168.3.4 for path /user/neymar/tgen640 at Fri Mar 10 09:18:18 UTC 2017
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
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Fri Mar 10 09:18:18 UTC 2017 in 13 milliseconds


The filesystem under path '/user/neymar/tgen640' is HEALTHY
```
