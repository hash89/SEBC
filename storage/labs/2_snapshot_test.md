# Test HDFS Snapshots
Command run in my local filesystem: `scp SEBC.zip cloud@84.39.48.222:/tmp/`
(I needed to chown the file for my user)

Commands run as Hadrien user :
1. hdfs dfs -mkdir /data/precious
2. hdfs dfs -put /tmp/SEBC.zip /data/precious

On the Cloudera manager > Cluster > 'Cluster Name' > HDFS > File Brower

- I navigate to /data/precious and enable snapshot for that directory
- I create a snapshot sebc-hdfs-test for /data/precious

I delete the /precisous directory as asked like that : `hdfs dfs -rm -r /data/precious`

And here is the ouput : `rm: Failed to move to trash: hdfs://master:8020/data/precious: The directory /data/precious cannot be deleted since /data/precious is snapshottable and already has snapshots`

Now, let's delete the ZIp file : `hdfs dfs -rm /data/precious/SEBC.zip`

Here is the outppu : `7/03/07 13:48:06 INFO fs.TrashPolicyDefault: Moved: 'hdfs://master:8020/data/precious/SEBC.zip' to trash at: hdfs://master:8020/user/hadrien/.Trash/Current/data/precious/SEBC.zip`

So the file move to trash. Now we can restore it via Cloudera Manager HDFS File Browser > Navigate to /data/precious > 'Restore Directory from snapshot'

I choose thee first option. And the file come back !
