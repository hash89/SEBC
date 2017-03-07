## Replicate to another cluster

*Note : As no one near me has a cluster to test it I use the distCP and BDR on my own cluster*

Executed command : `hadoop jar /opt/cloudera/parcels/CDH-5.8.4-1.cdh5.8.4.p0.5/jars/hadoop-examples-2.6.0-mr1-cdh5.8.4.jar teragen -Dmapreduce. job.maps=100 1000000 /data/teragendir/secondteragen`

### DistCP test
distCP command : `hadoop distcp hdfs://master:8020/data/teragendir/secondteragen hdfs://master:8020/data/distcpdir`

Result :
```
17/03/07 10:52:28 INFO tools.DistCp: Input Options: DistCpOptions{atomicCommit=false, syncFolder=false, deleteMissing=false, ignoreFailures=false, overwrite=false, append=false, useDiff=false, useRdiff=false, fromSnapshot=null, toSnapshot=null, skipCRC=false, blocking=true, numListstatusThreads=0, maxMaps=20, mapBandwidth=100, sslConfigurationFile='null', copyStrategy='uniformsize', preserveStatus=[], preserveRawXattrs=false, atomicWorkPath=null, logPath=null, sourceFileListing=null, sourcePaths=[hdfs://master:8020/data/teragendir/secondteragen], targetPath=hdfs://master:8020/data/distcpdir, targetPathExists=false, filtersFile='null'}
17/03/07 10:52:28 INFO client.RMProxy: Connecting to ResourceManager at master/192.168.3.6:8032
17/03/07 10:52:28 INFO tools.SimpleCopyListing: Paths (files+dirs) cnt = 102; dirCnt = 1
17/03/07 10:52:28 INFO tools.SimpleCopyListing: Build file listing completed.
17/03/07 10:52:28 INFO Configuration.deprecation: io.sort.mb is deprecated. Instead, use mapreduce.task.io.sort.mb
17/03/07 10:52:28 INFO Configuration.deprecation: io.sort.factor is deprecated. Instead, use mapreduce.task.io.sort.factor
17/03/07 10:52:28 INFO tools.DistCp: Number of paths in the copy list: 102
17/03/07 10:52:28 INFO tools.DistCp: Number of paths in the copy list: 102
17/03/07 10:52:28 INFO client.RMProxy: Connecting to ResourceManager at master/192.168.3.6:8032
17/03/07 10:52:29 INFO mapreduce.JobSubmitter: number of splits:20
17/03/07 10:52:29 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1488880986131_0008
17/03/07 10:52:29 INFO impl.YarnClientImpl: Submitted application application_1488880986131_0008
17/03/07 10:52:29 INFO mapreduce.Job: The url to track the job: http://master:8088/proxy/application_1488880986131_0008/
17/03/07 10:52:29 INFO tools.DistCp: DistCp job-id: job_1488880986131_0008
17/03/07 10:52:29 INFO mapreduce.Job: Running job: job_1488880986131_0008
17/03/07 10:52:36 INFO mapreduce.Job: Job job_1488880986131_0008 running in uber mode : false
17/03/07 10:52:36 INFO mapreduce.Job:  map 0% reduce 0%
17/03/07 10:52:46 INFO mapreduce.Job:  map 10% reduce 0%
17/03/07 10:52:47 INFO mapreduce.Job:  map 35% reduce 0%
17/03/07 10:52:48 INFO mapreduce.Job:  map 100% reduce 0%
17/03/07 10:52:49 INFO mapreduce.Job: Job job_1488880986131_0008 completed successfully
17/03/07 10:52:49 INFO mapreduce.Job: Counters: 33
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=2501230
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1000024676
                HDFS: Number of bytes written=1000000000
                HDFS: Number of read operations=1270
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=243
        Job Counters
                Launched map tasks=20
                Other local map tasks=20
                Total time spent by all maps in occupied slots (ms)=194547
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=194547
                Total vcore-seconds taken by all map tasks=194547
                Total megabyte-seconds taken by all map tasks=199216128
        Map-Reduce Framework
                Map input records=102
                Map output records=0
                Input split bytes=2360
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1298
                CPU time spent (ms)=42150
                Physical memory (bytes) snapshot=5215490048
                Virtual memory (bytes) snapshot=31962492928
                Total committed heap usage (bytes)=11203510272
        File Input Format Counters
                Bytes Read=22316
        File Output Format Counters
                Bytes Written=0
        org.apache.hadoop.tools.mapred.CopyMapper$Counter
                BYTESCOPIED=1000000000
                BYTESEXPECTED=1000000000
                COPY=102
```

*Note : I can see the new directory in HUE interface*

Let's run the check `hdfs fsck /data/distcpdir  -files -blocks`

With result :
```
Connecting to namenode via http://master:50070
FSCK started by hadrien (auth:SIMPLE) from /192.168.3.5 for path /data/distcpdir at Tue Mar 07 10:55:59 UTC 2017
/data/distcpdir <dir>
/data/distcpdir/_SUCCESS 0 bytes, 0 block(s):  OK

/data/distcpdir/part-m-00000 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744023_3199 len=10000000 Live_repl=3

/data/distcpdir/part-m-00001 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744042_3218 len=10000000 Live_repl=3

/data/distcpdir/part-m-00002 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744062_3238 len=10000000 Live_repl=3

/data/distcpdir/part-m-00003 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744082_3258 len=10000000 Live_repl=3

/data/distcpdir/part-m-00004 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744098_3274 len=10000000 Live_repl=3

[...]

/data/distcpdir/part-m-00097 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744057_3233 len=10000000 Live_repl=3

/data/distcpdir/part-m-00098 10000000 bytes, 1 block(s):
 OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744078_3254 len=10000000 Live_repl=3

/data/distcpdir/part-m-00099 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744093_3269 len=10000000 Live_repl=3

Status: HEALTHY
 Total size:    1000000000 B
 Total dirs:    1
 Total files:   101
 Total symlinks:                0
 Total blocks (validated):      100 (avg. block size 10000000 B)
 Minimally replicated blocks:   100 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Mar 07 10:55:59 UTC 2017 in 17 milliseconds


The filesystem under path '/data/distcpdir' is HEALTHY
```

### BDR replication test
In the Backup > Replication schedules, I create a schedule that I run imediatly from /data/teragendir/secondteragen to /data/bdrdir
it run succefuly.

Let's run the check on the new directory : `hdfs fsck /data/bdrdir -files -blocks`

Result :
```
Connecting to namenode via http://master:50070
FSCK started by hadrien (auth:SIMPLE) from /192.168.3.5 for path /data/bdrdir at Tue Mar 07 11:05:36 UTC 2017
/data/bdrdir <dir>
/data/bdrdir/secondteragen <dir>
/data/bdrdir/secondteragen/_SUCCESS 0 bytes, 0 block(s):  OK

/data/bdrdir/secondteragen/part-m-00000 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744222_3398 len=10000000 Live_repl=3

/data/bdrdir/secondteragen/part-m-00001 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744234_3410 len=10000000 Live_repl=3

/data/bdrdir/secondteragen/part-m-00002 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744240_3416 len=10000000 Live_repl=3

/data/bdrdir/secondteragen/part-m-00003 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744223_3399 len=10000000 Live_repl=3

/data/bdrdir/secondteragen/part-m-00004 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744239_3415 len=10000000 Live_repl=3

/data/bdrdir/secondteragen/part-m-00005 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744244_3420 len=10000000 Live_repl=3
1.

[...]

/data/bdrdir/secondteragen/part-m-00097 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744322_3498 len=10000000 Live_repl=3

/data/bdrdir/secondteragen/part-m-00098 10000000 bytes, 1 block(s):
 OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744226_3402 len=10000000 Live_repl=3

/data/bdrdir/secondteragen/part-m-00099 10000000 bytes, 1 block(s):  OK
0. BP-804592472-192.168.3.6-1488819445600:blk_1073744237_3413 len=10000000 Live_repl=3

Status: HEALTHY
 Total size:    1000000000 B
 Total dirs:    2
 Total files:   101
 Total symlinks:                0
 Total blocks (validated):      100 (avg. block size 10000000 B)
 Minimally replicated blocks:   100 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Mar 07 11:05:36 UTC 2017 in 8 milliseconds


The filesystem under path '/data/bdrdir' is HEALTHY
```
