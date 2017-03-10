AWS

jm1_challenge
ec2-34-250-19-251.eu-west-1.compute.amazonaws.com
34.250.19.251
192.168.0.46
 
jm2_challenge
ec2-34-252-148-62.eu-west-1.compute.amazonaws.com
34.252.148.62
192.168.0.110
 
jm3_challenge
ec2-34-248-238-199.eu-west-1.compute.amazonaws.com
192.168.0.41
34.248.238.199

jm4_challenge
ec2-34-249-240-30.eu-west-1.compute.amazonaws.com
34.249.240.30
192.168.0.64
 
jm5_challenge
ec2-34-250-253-235.eu-west-1.compute.amazonaws.com
34.250.253.235
192.168.0.142


uname -a
Linux ip-192-168-0-110.eu-west-1.compute.internal 3.10.0-514.el7.x86_64 #1 SMP Wed Oct 19 11:24:13 EDT 2016 x86_64 x86_64 x86_64 GNU/Linux


df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda2       65G  2.5G   63G   4% /
devtmpfs        7.3G     0  7.3G   0% /dev
tmpfs           7.2G     0  7.2G   0% /dev/shm
tmpfs           7.2G   17M  7.2G   1% /run
tmpfs           7.2G     0  7.2G   0% /sys/fs/cgroup
tmpfs           1.5G     0  1.5G   0% /run/user/0
tmpfs           1.5G     0  1.5G   0% /run/user/996


yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
repo id                                                                  repo name                                                                               status
cloudera-manager                                                         Cloudera Manager                                                                             7
rhui-REGION-client-config-server-7/x86_64                                Red Hat Update Infrastructure 2.0 Client Configuration Server 7                              6
rhui-REGION-rhel-server-releases/7Server/x86_64                          Red Hat Enterprise Linux Server 7 (RPMs)                                                14,038
rhui-REGION-rhel-server-rh-common/7Server/x86_64                         Red Hat Enterprise Linux Server 7 RH Common (RPMs)                                         209
repolist: 14,260


adduser ronaldo -u 2016
adduser neymar -u 2016
adduser: UID 2016 is not unique
adduser neymar -u 2010
groupadd barca
groupadd merengues
usermod -G merengues neymar
usermod -G barca ronaldo

cat /etc/group |tail -2
barca:x:2017:ronaldo
merengues:x:2018:neymar
