# Sentry connection

```
!connect jdbc:hive2://master:10000/default;principal=hive/master@SEBC.COM
Connecting to jdbc:hive2://master:10000/default;principal=hive/master@SEBC.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.1)
Driver: Hive JDBC (version 1.1.0-cdh5.9.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://master:10000/default>
0: jdbc:hive2://master:10000/default>
0: jdbc:hive2://master:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170308150101_d3e2fe6a-e259-4eb0-a410-3b9c999ac9d8): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170308150101_d3e2fe6a-e259-4eb0-a410-3b9c999ac9d8); Time taken: 0.589 seconds
INFO  : Executing command(queryId=hive_20170308150101_d3e2fe6a-e259-4eb0-a410-3b9c999ac9d8): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308150101_d3e2fe6a-e259-4eb0-a410-3b9c999ac9d8); Time taken: 0.244 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2,145 seconds)
0: jdbc:hive2://master:10000/default> use default;
Error: Error while compiling statement: FAILED: SemanticException No valid privileges
 User hadrien does not have privileges for SWITCHDATABASE
 The required privileges: Server=server1->Db=*->Table=+->Column=*->action=select;Server=server1->Db=*->Table=+->Column=*->action=insert; (state=42000,code=40000)
0: jdbc:hive2://master:10000/default>
0: jdbc:hive2://master:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170308150101_d536bb19-770b-4835-acda-5ff605dc10ec): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170308150101_d536bb19-770b-4835-acda-5ff605dc10ec); Time taken: 0.069 seconds
INFO  : Executing command(queryId=hive_20170308150101_d536bb19-770b-4835-acda-5ff605dc10ec): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308150101_d536bb19-770b-4835-acda-5ff605dc10ec); Time taken: 0.099 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0,184 seconds)
```
