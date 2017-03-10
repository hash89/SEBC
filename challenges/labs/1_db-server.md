# My db server

## Db host
manager

## Version
Command : `mysql --version`

Output : `mysql  Ver 15.1 Distrib 5.5.54-MariaDB, for Linux (x86_64) using readline 5.1`

## Databases
```
[root@manager cloud]# mysql -u root -p
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 21
Server version: 5.5.54-MariaDB-wsrep MariaDB Server, wsrep_25.14.r9949137

Copyright (c) 2000, 2016, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)
```
