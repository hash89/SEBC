# Tuning for YARN

## Recap

| n° | maper | reducer | container RAM | ratio | total time  |
|----|-------|---------|---------------|-------|-------------|
|  1 |     8 |       1 |           512 |   0.8 |        2m28 |
|  2 |     8 |       1 |          1024 |   0.8 |        2m34 |
|  3 |     8 |       1 |          2048 |   0.5 |        2m48 |
|  4 |     8 |       1 |          2048 |   0.8 |        1m58 |
|  5 |    24 |       8 |          1024 |   0.8 |        1m50 |
|  6 |    24 |       8 |           512 |   0.8 |        1m51 |
|  7 |     8 |       8 |          1024 |   0.8 |        1m48 |
|  8 |     8 |       8 |           512 |   0.8 |        1m51 |


## Complete data
### Here is the output of the script with parameters as follow:
  - 8 mapper
  - 1 reducer
  - Container mem 512 and 1024
  - Map heapsize ratio 0.8
  - Reduce heapsize ratio 0.8

```
[hadrien@manager ~]$ ./YARNtest.sh
Testing loop started on mar. mars 7 15:07:04 UTC 2017
Mapper 8 | Reducer 1 | container memory 512 | MAP_MB 409 | RED_MB 409

real    0m49.312s
user    0m4.312s
sys     0m0.303s

real    1m39.036s
user    0m5.454s
sys     0m0.343s
Deleted /data/tg-10GB-8-1-512
Deleted /data/ts-10GB-8-1-512
Mapper 8 | Reducer 1 | container memory 1024 | MAP_MB 819 | RED_MB 819

real    0m52.408s
user    0m4.094s
sys     0m0.264s

real    1m42.191s
user    0m5.311s
sys     0m0.360s
Deleted /data/tg-10GB-8-1-1024
Deleted /data/ts-10GB-8-1-1024
Testing loop ended on mar. mars 7 15:12:14 UTC 2017
```

### Here is the output of the script with :
  - 8 mapper
  - 1 reducer
  - Container mem 2048
  - Map heapsize ratio 0.5
  - Reduce heapsize ratio 0.5

```
Testing loop started on mar. mars 7 15:17:20 UTC 2017
Mapper 8 | Reducer 1 | container memory 2048 | MAP_MB 1024 | RED_MB 1024

real    0m48.413s
user    0m4.097s
sys     0m0.298s

real    2m0.233s
user    0m5.858s
sys     0m0.362s
Deleted /data/tg-10GB-8-1-2048
Deleted /data/ts-10GB-8-1-2048
Testing loop ended on mar. mars 7 15:20:13 UTC 2017
```

### Here is the output of the script with :
  - 8 mapper
  - 1 reducer
  - Container mem 2048
  - Map heapsize ratio 0.8
  - Reduce heapsize ratio 0.8

```
Testing loop started on mar. mars 7 15:27:50 UTC 2017
Mapper 8 | Reducer 1 | container memory 2048 | MAP_MB 1638 | RED_MB 1638

real    0m1.938s
user    0m2.398s
sys     0m0.214s

real    1m57.134s
user    0m5.603s
sys     0m0.332s
Deleted /data/tg-10GB-8-1-2048
Testing loop ended on mar. mars 7 15:29:51 UTC 2017
```

### Here is the output of the script with :
  - 24 mapper
  - 8 reducer
  - Container mem 1024
  - Map heapsize ratio 0.8
  - Reduce heapsize ratio 0.8

```
Testing loop started on mar. mars 7 15:30:37 UTC 2017
Mapper 24 | Reducer 8 | container memory 1024 | MAP_MB 819 | RED_MB 819

real    0m50.542s
user    0m4.077s
sys     0m0.276s

real    1m0.906s
user    0m5.398s
sys     0m0.375s
Deleted /data/tg-10GB-24-8-1024
Testing loop ended on mar. mars 7 15:32:30 UTC 2017
```

### Here is the output of the script with :
  - 24 mapper
  - 8 reducer
  - Container mem 512
  - Map heapsize ratio 0.8
  - Reduce heapsize ratio 0.8

```
Testing loop started on mar. mars 7 15:35:18 UTC 2017
Mapper 24 | Reducer 8 | container memory 512 | MAP_MB 409 | RED_MB 409

real    0m48.594s
user    0m4.507s
sys     0m0.391s

real    1m3.133s
user    0m5.206s
sys     0m0.321s
Deleted /data/tg-10GB-24-8-512
Testing loop ended on mar. mars 7 15:37:11 UTC 2017
```

### Here is the output of the script with :
  - 8 mapper
  - 8 reducer
  - Container mem 1024
  - Map heapsize ratio 0.8
  - Reduce heapsize ratio 0.8

```
Testing loop started on mar. mars 7 15:52:17 UTC 2017
Mapper 8 | Reducer 8 | container memory 1024 | MAP_MB 819 | RED_MB 819

real    0m51.540s
user    0m4.546s
sys     0m0.339s

real    0m57.978s
user    0m5.366s
sys     0m0.345s
 Deleted /data/tg-10GB-8-8-1024
Testing loop ended on mar. mars 7 15:54:08 UTC 2017
```

### Here is the output of the script with :
  - 8 mapper
  - 8 reducer
  - Container mem 512
  - Map heapsize ratio 0.8
  - Reduce heapsize ratio 0.8

```
Testing loop started on mar. mars 7 15:54:56 UTC 2017
Mapper 8 | Reducer 8 | container memory 512 | MAP_MB 409 | RED_MB 409

real    0m50.377s
user    0m4.038s
sys     0m0.319s

real    1m1.049s
user    0m5.684s
sys     0m0.382s
Deleted /data/tg-10GB-8-8-512
Testing loop ended on mar. mars 7 15:56:50 UTC 2017
```
