Cloud provider : OpenStack
Release : Centos 7.2

Disk space (Result of Ansible command `ansible all -m shell -a "df -h" | grep /data`) :
/dev/vdb           493G     70M  467G   1% /data
/dev/vdb           493G     70M  467G   1% /data
/dev/vdb           493G     70M  467G   1% /data
/dev/vdb           493G     70M  467G   1% /data
/dev/vdb           493G     70M  467G   1% /data

Yum repolist enabled result :
worker3 | SUCCESS | rc=0 >>
Modules complémentaires chargés : fastestmirror
Determining fastest mirrors
 * base: ftp.pasteur.fr
 * epel: nl.mirror.babylon.network
 * extras: ftp.pasteur.fr
 * updates: centos.quelquesmots.fr
id du dépôt           nom du dépôt                                        statut
!base/7/x86_64        CentOS-7 - Base                                      9 007
!epel/x86_64          Extra Packages for Enterprise Linux 7 - x86_64      10 813
!extras/7/x86_64      CentOS-7 - Extras                                      393
!updates/7/x86_64     CentOS-7 - Updates                                   2 560
repolist: 22 773Repodata is over 2 weeks old. Install yum-cron? Or run: yum makecache fast

worker2 | SUCCESS | rc=0 >>
Modules complémentaires chargés : fastestmirror
Determining fastest mirrors
 * base: distrib-coffee.ipsl.jussieu.fr
 * epel: nl.mirror.babylon.network
 * extras: centos.quelquesmots.fr
 * updates: centos.quelquesmots.fr
id du dépôt           nom du dépôt                                        statut
!base/7/x86_64        CentOS-7 - Base                                      9 007
!epel/x86_64          Extra Packages for Enterprise Linux 7 - x86_64      10 813
!extras/7/x86_64      CentOS-7 - Extras                                      393
!updates/7/x86_64     CentOS-7 - Updates                                   2 560
repolist: 22 773Repodata is over 2 weeks old. Install yum-cron? Or run: yum makecache fast

master | SUCCESS | rc=0 >>
Modules complémentaires chargés : fastestmirror
Determining fastest mirrors
 * base: centos.mirror.fr.planethoster.net
 * epel: mirrors.coreix.net
 * extras: centos.quelquesmots.fr
 * updates: centos.quelquesmots.fr
id du dépôt           nom du dépôt                                        statut
!base/7/x86_64        CentOS-7 - Base                                      9 007
!epel/x86_64          Extra Packages for Enterprise Linux 7 - x86_64      10 813
!extras/7/x86_64      CentOS-7 - Extras                                      393
!updates/7/x86_64     CentOS-7 - Updates                                   2 560
repolist: 22 773Repodata is over 2 weeks old. Install yum-cron? Or run: yum makecache fast

manager | SUCCESS | rc=0 >>
Modules complémentaires chargés : fastestmirror
Determining fastest mirrors
 * base: centos.crazyfrogs.org
 * epel: epel.mirror.nucleus.be
 * extras: centos.quelquesmots.fr
 * updates: centos.quelquesmots.fr
id du dépôt           nom du dépôt                                        statut
!base/7/x86_64        CentOS-7 - Base                                      9 007
!epel/x86_64          Extra Packages for Enterprise Linux 7 - x86_64      10 813
!extras/7/x86_64      CentOS-7 - Extras                                      393
!updates/7/x86_64     CentOS-7 - Updates                                   2 560
repolist: 22 773Repodata is over 2 weeks old. Install yum-cron? Or run: yum makecache fast

worker1 | SUCCESS | rc=0 >>
Modules complémentaires chargés : fastestmirror
Determining fastest mirrors
 * base: mirrors.ircam.fr
 * epel: mirrors.coreix.net
 * extras: ftp.rezopole.net
 * updates: mirrors.atosworldline.com
id du dépôt           nom du dépôt                                        statut
!base/7/x86_64        CentOS-7 - Base                                      9 007
!epel/x86_64          Extra Packages for Enterprise Linux 7 - x86_64      10 813
!extras/7/x86_64      CentOS-7 - Extras                                      393
!updates/7/x86_64     CentOS-7 - Updates                                   2 560
repolist: 22 773Repodata is over 2 weeks old. Install yum-cron? Or run: yum makecache fast
