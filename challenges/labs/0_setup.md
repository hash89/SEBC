# Cloud provider
Cloud provider : OpenStack

# Nodes
manager   84.39.48.22
master    84.39.49.7
worker1   84.39.49.14  
worker2   84.39.49.15
worker3   84.39.49.17

# Release
Centos 7.2

# Disk space
Disk space (Result of Ansible command `ansible all -m shell -a "df -h" | grep /data`) :
/dev/vdb            99G     60M   94G   1% /data
/dev/vdb            99G     60M   94G   1% /data
/dev/vdb            99G     60M   94G   1% /data
/dev/vdb            99G     60M   94G   1% /data
/dev/vdb            99G     60M   94G   1% /data

# Yum repo
Yum repolist enabled result :
```
Modules complémentaires chargés : fastestmirror
Determining fastest mirrors
 * base: distrib-coffee.ipsl.jussieu.fr
 * epel: mirrors.ircam.fr
 * extras: mirror.neify.es
 * updates: miroir.univ-paris13.fr
id du dépôt           nom du dépôt                                        statut
!base/7/x86_64        CentOS-7 - Base                                      9 363
!epel/x86_64          Extra Packages for Enterprise Linux 7 - x86_64      11 307
!extras/7/x86_64      CentOS-7 - Extras                                      311
!updates/7/x86_64     CentOS-7 - Updates                                   1 107
repolist: 22 088
```

# /etc/passwd

Command `ansible all -m shell -a "cat /etc/passwd" | grep neymar`
*each line represent a node*
```
neymar:x:2010:2010::/home/neymar:/bin/bash
neymar:x:2010:2010::/home/neymar:/bin/bash
neymar:x:2010:2010::/home/neymar:/bin/bash
neymar:x:2010:2010::/home/neymar:/bin/bash
neymar:x:2010:2010::/home/neymar:/bin/bash
```

Command `ansible all -m shell -a "cat /etc/passwd" | grep ronaldo`
*each line represent a node*
```
ronaldo:x:2016:2016::/home/ronaldo:/bin/bash
ronaldo:x:2016:2016::/home/ronaldo:/bin/bash
ronaldo:x:2016:2016::/home/ronaldo:/bin/bash
ronaldo:x:2016:2016::/home/ronaldo:/bin/bash
ronaldo:x:2016:2016::/home/ronaldo:/bin/bash
```

# /etc/group

Command `ansible all -m shell -a "cat /etc/group" | grep barca`
*each line represent a node*
```
barca:x:1001:ronaldo
barca:x:1001:ronaldo
barca:x:1001:ronaldo
barca:x:1001:ronaldo
barca:x:1001:ronaldo
```

Command `ansible all -m shell -a "cat /etc/group" | grep merengues`
*each line represent a node*
```
merengues:x:1002:neymar
merengues:x:1002:neymar
merengues:x:1002:neymar
merengues:x:1002:neymar
merengues:x:1002:neymar
```
