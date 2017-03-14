AWS
Casals Cloudera BCCh-1		34.248.238.199		192.168.0.51
Casals Cloudera BCCh-2		34.250.19.251		192.168.0.205
Casals Cloudera BCCh-3		34.249.240.30		192.168.0.145
Casals Cloudera BCCh-4		34.251.103.54		192.168.0.212
Casals Cloudera BCCh-5		34.252.111.206		192.168.0.40

root/lolo


uname -a
Linux ip-192-168-0-110.eu-west-1.compute.internal 3.10.0-514.el7.x86_64 #1 SMP Wed Oct 19 11:24:13 EDT 2016 x86_64 x86_64 x86_64 GNU/Linux

df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda2       50G  1.2G   49G   3% /
devtmpfs        7.3G     0  7.3G   0% /dev
tmpfs           7.2G     0  7.2G   0% /dev/shm
tmpfs           7.2G   17M  7.2G   1% /run
tmpfs           7.2G     0  7.2G   0% /sys/fs/cgroup
tmpfs           1.5G     0  1.5G   0% /run/user/0

yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
repo id                                          repo name                status
rhui-REGION-client-config-server-7/x86_64        Red Hat Update Infrastru      6
rhui-REGION-rhel-server-releases/7Server/x86_64  Red Hat Enterprise Linux 14,038
rhui-REGION-rhel-server-rh-common/7Server/x86_64 Red Hat Enterprise Linux    209
repolist: 14,253
[root@ip-192-168-0-51 ~]#


adduser ronaldo -u 2016
adduser neymar -u 2010
groupadd barca
groupadd merengues
usermod -G merengues neymar
usermod -G barca ronaldo

cat /etc/passwd|tail -2
ronaldo:x:2016:2016::/home/ronaldo:/bin/bash
neymar:x:2010:2010::/home/neymar:/bin/bash

cat /etc/group |tail -2
barca:x:2017:ronaldo
merengues:x:2018:neymar
