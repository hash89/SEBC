# Test HDFS performance

I run a first teragen with the configuration :
- 1 vcore / 1 Go RAM by container
- Option -Dmapreduce.job.maps=200 (a little too much)
It start at 17/03/07 11:18:06 and end at 17/03/07 11:29:36 (approx. 10 min)
Because of the configuration of Yarn and the number of vCores available I can't run more than 24 maps.
Command : `hadoop jar /opt/cloudera/parcels/CDH-5.8.4-1.cdh5.8.4.p0.5/jars/hadoop-examples-2.6.0-mr1-cdh5.8.4.jar teragen -Dmapreduce.job.maps=200 1000000000 teragen-10go`

So I decided to change the configuration yarn.scheduler.minimum-allocation-mb to 2 Go and re launch the teragen with 24 maps in order to have all the memory available working on the teragen job, with this configuration :
- 1 vcore / 2 Go RAM by container
- Option -Dmapreduce.job.maps=24 (a little more tuned)
it start at 17/03/07 12:36:43 and end at 12:46:37 (approx. 10 min)
Command : `hadoop jar /opt/cloudera/parcels/CDH-5.8.4-1.cdh5.8.4.p0.5/jars/hadoop-examples-2.6.0-mr1-cdh5.8.4.jar teragen -Dmapreduce.job.maps=24 1000000000 teragen-10go-2`

## 10 Go file
All these commands are run under hdfs /data/hadrien dir with my user "hadrien"

### Teragen
Command: `hadoop jar /opt/cloudera/parcels/CDH-5.8.4-1.cdh5.8.4.p0.5/jars/hadoop-examples-2.6.0-mr1-cdh5.8.4.jar teragen -Ddfs.block.size=33554432 -Dmapreduce.job.maps=4 1000000000 teragen-10go-3`

In the RessourceManager Web UI I can see that it start at 13:50:57 and end at 14:02:10 (approx. 12 min)

### Terasort
Command: `hadoop jar /opt/cloudera/parcels/CDH-5.8.4-1.cdh5.8.4.p0.5/jars/hadoop-examples-2.6.0-mr1-cdh5.8.4.jar terasort -Ddfs.block.size=33554432 -Dmapreduce.job.maps=4 teragen-10go-3 terasort-output`

it start at 14:03:59 and end at 14:26:20 (approx. 23 min)

### Teravalidate
Command: `hadoop jar /opt/cloudera/parcels/CDH-5.8.4-1.cdh5.8.4.p0.5/jars/hadoop-examples-2.6.0-mr1-cdh5.8.4.jar teravalidate terasort-output teravalidate-output`

It start at 14:28:39 and end at 14:34:09 (approx. 6 min)
