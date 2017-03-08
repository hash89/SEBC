# Sentry connection

### Verifications
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

## As George User
```
[cloud@manager ~]$ sudo su george
[george@manager cloud]$ kinit george@SEBC.COM
Password for george@SEBC.COM:
[george@manager cloud]$
[george@manager cloud]$ beeline

Beeline version 1.1.0-cdh5.9.1 by Apache Hive
beeline>
beeline> !connect jdbc:hive2://master:10000/default;principal=hive/master@SEBC.COM
scan complete in 2ms
Connecting to jdbc:hive2://master:10000/default;principal=hive/master@SEBC.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.1)
Driver: Hive JDBC (version 1.1.0-cdh5.9.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://master:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170308151515_1bdb57e8-95fc-451a-a47f-e109e1c08701): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170308151515_1bdb57e8-95fc-451a-a47f-e109e1c08701); Time taken: 0.071 seconds
INFO  : Executing command(queryId=hive_20170308151515_1bdb57e8-95fc-451a-a47f-e109e1c08701): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308151515_1bdb57e8-95fc-451a-a47f-e109e1c08701); Time taken: 0.133 seconds
INFO  : OK
+--------------+--+
|   tab_name   |
+--------------+--+
| creditcards  |
| crimes       |
+--------------+--+
2 rows selected (0,295 seconds)
```

## As Ferdinand User

I load a dataset from Kaggle.com for the test. The table name is crimes in default base.
I grant as follow : `GRANT SELECT ON default.crimes TO ROLE writes;`

```
[cloud@manager ~]$ sudo su ferdinand
[ferdinand@manager cloud]$ kinit ferdinand@SEBC.COM
Password for ferdinand@SEBC.COM:
[ferdinand@manager cloud]$ beeline
Beeline version 1.1.0-cdh5.9.1 by Apache Hive
beeline> !connect jdbc:hive2://master:10000/default;principal=hive/master@SEBC.COM
scan complete in 1ms
Connecting to jdbc:hive2://master:10000/default;principal=hive/master@SEBC.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.1)
Driver: Hive JDBC (version 1.1.0-cdh5.9.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://master:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170308151919_00eb3eb4-9919-4cc6-bed7-cbe7b3aed348): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170308151919_00eb3eb4-9919-4cc6-bed7-cbe7b3aed348); Time taken: 0.053 seconds
INFO  : Executing command(queryId=hive_20170308151919_00eb3eb4-9919-4cc6-bed7-cbe7b3aed348): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170308151919_00eb3eb4-9919-4cc6-bed7-cbe7b3aed348); Time taken: 0.117 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
| crimes    |
+-----------+--+
1 row selected (0,258 seconds)
```
