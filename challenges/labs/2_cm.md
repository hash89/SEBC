# Repo cloudera

```
[root@manager yum.repos.d]# ls -l /etc/yum.repos.d/
total 44
-rw-r--r--. 1 root root 1664  9 déc.   2015 CentOS-Base.repo
-rw-r--r--. 1 root root 1309  9 déc.   2015 CentOS-CR.repo
-rw-r--r--. 1 root root  649  9 déc.   2015 CentOS-Debuginfo.repo
-rw-r--r--. 1 root root  290  9 déc.   2015 CentOS-fasttrack.repo
-rw-r--r--. 1 root root  630  9 déc.   2015 CentOS-Media.repo
-rw-r--r--. 1 root root 1331  9 déc.   2015 CentOS-Sources.repo
-rw-r--r--. 1 root root 1952  9 déc.   2015 CentOS-Vault.repo
-rw-r--r--  1 root root  271 10 mars  08:31 cloudera-cdh5.9.repo
-rw-r--r--. 1 root root  957 23 juil.  2016 epel.repo
-rw-r--r--. 1 root root 1056 23 juil.  2016 epel-testing.repo
-rw-r--r--  1 root root  143 10 mars  08:13 mariadb.repo
```

# Prepare database
`/usr/share/cmf/schema/scm_prepare_database.sh mysql scm scm scm -h manager`
