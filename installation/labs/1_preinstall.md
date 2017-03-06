# Preinstall

## Check VM Swappiness
Executed commands :
- `ansible all -m sysctl -a "name=vm.swappiness value=1 state=present"`
- `ansible all -m shell -a "echo \"1\" > /proc/sys/vm/swappiness" --become`
- `ansible all -m shell -a "cat /proc/sys/vm/swappiness"`

Result :
```
worker1 | SUCCESS | rc=0 >>
1
```

## Check Volumes attributes
Executed command : `ansible all -m shell -a "mount -l"`

Result :
```
worker1 | SUCCESS | rc=0 >>
sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,relatime)
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime)
devtmpfs on /dev type devtmpfs (rw,nosuid,size=15985296k,nr_inodes=3996324,mode=755)
securityfs on /sys/kernel/security type securityfs (rw,nosuid,nodev,noexec,relatime)
tmpfs on /dev/shm type tmpfs (rw,nosuid,nodev)
devpts on /dev/pts type devpts (rw,nosuid,noexec,relatime,gid=5,mode=620,ptmxmode=000)
tmpfs on /run type tmpfs (rw,nosuid,nodev,mode=755)
tmpfs on /sys/fs/cgroup type tmpfs (ro,nosuid,nodev,noexec,mode=755)
cgroup on /sys/fs/cgroup/systemd type cgroup (rw,nosuid,nodev,noexec,relatime,xattr,release_agent=/usr/lib/systemd/systemd-cgroups-agent,name=systemd)
pstore on /sys/fs/pstore type pstore (rw,nosuid,nodev,noexec,relatime)
cgroup on /sys/fs/cgroup/cpuset type cgroup (rw,nosuid,nodev,noexec,relatime,cpuset)
cgroup on /sys/fs/cgroup/blkio type cgroup (rw,nosuid,nodev,noexec,relatime,blkio)
cgroup on /sys/fs/cgroup/cpu,cpuacct type cgroup (rw,nosuid,nodev,noexec,relatime,cpuacct,cpu)
cgroup on /sys/fs/cgroup/devices type cgroup (rw,nosuid,nodev,noexec,relatime,devices)
cgroup on /sys/fs/cgroup/perf_event type cgroup (rw,nosuid,nodev,noexec,relatime,perf_event)
cgroup on /sys/fs/cgroup/hugetlb type cgroup (rw,nosuid,nodev,noexec,relatime,hugetlb)
cgroup on /sys/fs/cgroup/freezer type cgroup (rw,nosuid,nodev,noexec,relatime,freezer)
cgroup on /sys/fs/cgroup/net_cls type cgroup (rw,nosuid,nodev,noexec,relatime,net_cls)
cgroup on /sys/fs/cgroup/memory type cgroup (rw,nosuid,nodev,noexec,relatime,memory)
configfs on /sys/kernel/config type configfs (rw,relatime)
/dev/vda1 on / type xfs (rw,relatime,attr2,inode64,noquota)
rpc_pipefs on /var/lib/nfs/rpc_pipefs type rpc_pipefs (rw,relatime)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=26,pgrp=1,timeout=300,minproto=5,maxproto=5,direct)

mqueue on /dev/mqueue type mqueue (rw,relatime)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime)
nfsd on /proc/fs/nfsd type nfsd (rw,relatime)
/dev/vdb on /data type ext3 (rw,relatime,data=ordered)
tmpfs on /run/user/1000 type tmpfs (rw,nosuid,nodev,relatime,size=3200784k,mode=700,uid=1000,gid=1000)
```

## Reserve space of any non-root, ext-based volumes

Executed command : `ansible all -m shell -a "cat /etc/fstab"`

Result
```
worker1 | SUCCESS | rc=0 >>

#
# /etc/fstab
# Created by anaconda on Mon Sep  5 11:52:12 2016
#
# Accessible filesystems, by reference, are maintained under '/dev/disk'
# See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info
#
/dev/vda1 /                       xfs     defaults        0 0
/data /dev/vdb ext4 rw 0 0
/dev/vdb /data ext3 rw 0 0
```

## Disable transparent hugepage support
Executed command : `ansible all -m shell -a "echo \"never\" > /sys/kernel/mm/transparent_hugepage/defrag"`

## List of network interface
Executed command : `ansible all -m shell -a "ip a" --become`

Result :
```
manager | SUCCESS | rc=0 >>
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP qlen 1000
    link/ether 02:b0:44:33:ad:34 brd ff:ff:ff:ff:ff:ff
    inet 192.168.3.5/24 brd 192.168.3.255 scope global eth0
       valid_lft forever preferred_lft forever
    inet6 fe80::b0:44ff:fe33:ad34/64 scope link
       valid_lft forever preferred_lft forever
```

## Lookups
Executed command : `getent hosts master`

Result :
```
$> getent hosts master
fe80::9c:d4ff:fe8c:128d master
```
(The same for every hosts)

## Nscd service
Executed command: `ansible all -m yum -a "name=nscd  state=latest" --become` in order to install Nscd service

Result :
```
SUCCESS => {
    "changed": true,
    "msg": "Repository cloudera-cdh5 is listed more than once in the configuration\n",
    "rc": 0,
    "results": [
        "Modules complémentaires chargés : fastestmirror\nLoading mirror speeds from cached hostfile\n * base: mirrors.ircam.fr\n * epel: mirror.23media.de\n * extras: distrib-coffee.ipsl.jussieu.fr\n * updates: ftp.ciril.fr\nRésolution des dépendances\n--> Lancement de la transaction de test\n---> Le paquet nscd.x86_64 0:2.17-157.el7_3.1 sera installé\n--> Résolution des dépendances terminée\n\nDépendances résolues\n\n================================================================================\n Package       Architecture    Version                   Dépôt            Taille\n================================================================================\nInstallation :\n nscd          x86_64          2.17-157.el7_3.1          updates          267 k\n\nRésumé de la transaction\n================================================================================\nInstallation   1 Paquet\n\nTaille totale des téléchargements : 267 k\nTaille d'installation : 179 k\nDownloading packages:\nRunning transaction check\nRunning transaction test\nTransaction test succeeded\nRunning transaction\n  Installation : nscd-2.17-157.el7_3.1.x86_64
        1/1 \n  Vérification : nscd-2.17-157.el7_3.1.x86_64                               1/1 \n\nInstallé :\n  nscd.x86_64 0:2.17-157.el7_3.1                                                \n\nTerminé !\n"
    ]
}
```
(On every nodes)

Executed command : ` ansible all -m service -a "name=nscd state=started"  --become` in order to start the service.

Executed command : `ansible all -m shell -a "systemctl status nscd"` to check the status

Result
```
worker3 | SUCCESS | rc=0 >>
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since lun. 2017-03-06 14:17:58 UTC; 33s ago
  Process: 20449 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 20450 (nscd)
   CGroup: /system.slice/nscd.service
           └─20450 /usr/sbin/nscd

mars 06 14:17:58 worker3 nscd[20450]: 20450 monitoring file `/etc/hosts` (4)
mars 06 14:17:58 worker3 nscd[20450]: 20450 monitoring directory `/etc` (2)
mars 06 14:17:58 worker3 nscd[20450]: 20450 monitoring file `/etc/resolv.conf` (5)
mars 06 14:17:58 worker3 nscd[20450]: 20450 monitoring directory `/etc` (2)
mars 06 14:17:58 worker3 nscd[20450]: 20450 monitoring file `/etc/services` (6)
mars 06 14:17:58 worker3 nscd[20450]: 20450 monitoring directory `/etc` (2)
mars 06 14:17:58 worker3 nscd[20450]: 20450 disabled inotify-based monitoring for file `/etc/netgroup': No such file or directory
mars 06 14:17:58 worker3 nscd[20450]: 20450 stat failed for file `/etc/netgroup'; will try again later: No such file or directory
mars 06 14:17:58 worker3 systemd[1]: Started Name Service Cache Daemon.
mars 06 14:18:17 worker3 nscd[20450]: 20450 checking for monitored file `/etc/netgroup': No such file or directory
```
## Ntpd Service
Executed command : `ansible all -m service -a "name=ntpd state=started"  --become` to start Ntpd service

Executed command : `ansible all -m shell -a "systemctl status ntpd" --become`

Result :
```
worker1 | SUCCESS | rc=0 >>
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since lun. 2017-03-06 14:20:34 UTC; 30s ago
  Process: 20455 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 20456 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─20456 /usr/sbin/ntpd -u ntp:ntp -g

mars 06 14:20:34 worker1 ntpd[20456]: Listen and drop on 1 v6wildcard :: UDP 123
mars 06 14:20:34 worker1 ntpd[20456]: Listen normally on 2 lo 127.0.0.1 UDP 123
mars 06 14:20:34 worker1 ntpd[20456]: Listen normally on 3 eth0 192.168.3.4 UDP 123
mars 06 14:20:34 worker1 ntpd[20456]: Listen normally on 4 lo ::1 UDP 123
mars 06 14:20:34 worker1 ntpd[20456]: Listen normally on 5 eth0 fe80::ae:a0ff:fe2e:4f2d UDP 123
mars 06 14:20:34 worker1 ntpd[20456]: Listening on routing socket on fd #22 for interface updates
mars 06 14:20:34 worker1 ntpd[20456]: 0.0.0.0 c016 06 restart
mars 06 14:20:34 worker1 ntpd[20456]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
mars 06 14:20:34 worker1 ntpd[20456]: 0.0.0.0 c011 01 freq_not_set
mars 06 14:20:41 worker1 ntpd[20456]: 0.0.0.0 c614 04 freq_mode
```
