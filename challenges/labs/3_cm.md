# Hdfs /user dir

```
[cloud@master ~]$ hdfs dfs -ls /user
Found 6 items
drwxrwxrwx   - mapred  hadoop           0 2017-03-10 08:54 /user/history
drwxrwxr-t   - hive    hive             0 2017-03-10 08:55 /user/hive
drwxrwxr-x   - hue     hue              0 2017-03-10 08:55 /user/hue
drwxr-xr-x   - neymar  neymar           0 2017-03-10 08:59 /user/neymar
drwxrwxr-x   - oozie   oozie            0 2017-03-10 08:56 /user/oozie
drwxr-xr-x   - ronaldo ronaldo          0 2017-03-10 08:59 /user/ronaldo
```


## API v14 hosts

```
{
  items: [
    {
      hostId: "5f347029-c7f6-4a08-87f8-597feb7578d6",
      ipAddress: "192.168.3.6",
      hostname: "manager",
      rackId: "/default",
      hostUrl: "http://master:7180/cmf/hostRedirect/5f347029-c7f6-4a08-87f8-597feb7578d6",
      maintenanceMode: false,
      maintenanceOwners: [ ],
      commissionState: "COMMISSIONED",
      numCores: 4,
      numPhysicalCores: 4,
      totalPhysMemBytes: 16262545408
    },
    {
      hostId: "300344c6-e18c-4212-9eb0-7da9c98db8bd",
      ipAddress: "192.168.3.4",
      hostname: "master",
      rackId: "/default",
      hostUrl: "http://master:7180/cmf/hostRedirect/300344c6-e18c-4212-9eb0-7da9c98db8bd",
      maintenanceMode: false,
      maintenanceOwners: [ ],
      commissionState: "COMMISSIONED",
      numCores: 4,
      numPhysicalCores: 4,
      totalPhysMemBytes: 16262545408
    },
    {
      hostId: "00a51f17-58a2-4980-8cde-27ccec6813a4",
      ipAddress: "192.168.3.7",
      hostname: "worker1",
      rackId: "/default",
      hostUrl: "http://master:7180/cmf/hostRedirect/00a51f17-58a2-4980-8cde-27ccec6813a4",
      maintenanceMode: false,
      maintenanceOwners: [ ],
      commissionState: "COMMISSIONED",
      numCores: 4,
      numPhysicalCores: 4,
      totalPhysMemBytes: 16262545408
    },
    {
      hostId: "0291d98f-6f56-4e77-85f7-f09ec0fb6b33",
      ipAddress: "192.168.3.3",
      hostname: "worker2",
      rackId: "/default",
      hostUrl: "http://master:7180/cmf/hostRedirect/0291d98f-6f56-4e77-85f7-f09ec0fb6b33",
      maintenanceMode: false,
      maintenanceOwners: [ ],
      commissionState: "COMMISSIONED",
      numCores: 4,
      numPhysicalCores: 4,
      totalPhysMemBytes: 16262545408
    },
    {
      hostId: "a62dec44-b313-4d1c-b36d-8b9bf64d9e07",
      ipAddress: "192.168.3.5",
      hostname: "worker3",
      rackId: "/default",
      hostUrl: "http://master:7180/cmf/hostRedirect/a62dec44-b313-4d1c-b36d-8b9bf64d9e07",
      maintenanceMode: false,
      maintenanceOwners: [ ],
      commissionState: "COMMISSIONED",
      numCores: 4,
      numPhysicalCores: 4,
      totalPhysMemBytes: 16262545408
    }
  ]
}
```
