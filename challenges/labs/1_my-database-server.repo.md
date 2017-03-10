# MariaDB repo file

Command executed  : `ansible manager -m shell -a "cat /etc/yum.repos.d/mariadb.repo"`
```
manager | SUCCESS | rc=0 >>
[mariadb]
name = MariaDB
baseurl = http://yum.mariadb.org/5.5/centos7-amd64
gpgkey=https://yum.mariadb.org/RPM-GPG-KEY-MariaDB
gpgcheck=1
```
