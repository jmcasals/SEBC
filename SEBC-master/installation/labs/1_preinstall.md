
@ip-192-168-0-175 ec2-user]# uname -a
Linux ip-192-168-0-175.eu-west-1.compute.internal 3.10.0-514.el7.x86_64 #1 SMP Wed Oct 19 11:24:13 EDT 2016 x86_64 x86_64 x86_64 GNU/Linux

aws stack:

JM Cloudera 1
34.251.238.165

JM Cloudera 2
34.248.94.166

JM Cloudera 3
34.252.76.225

JM Cloudera 4
34.248.230.155

JM Cloudera 5
34.250.167.161

root
BoiraMick

m3.xlarge

Modelo		CPU virtual	Memoria (GiB)	Almacenamiento en SSD (GB)
m3.xlarge	4		15		2 x 40 

------------------------------------------------------------------
[root@ip-192-168-0-175 ec2-user]# sudo bash -c "echo 'vm.swappiness = 1' >> /etc/sysctl.conf"

[root@ip-192-168-0-175 ec2-user]# cat /etc/sysctl.conf                          # sysctl settings are defined through files in
# /usr/lib/sysctl.d/, /run/sysctl.d/, and /etc/sysctl.d/.
#
# Vendors settings live in /usr/lib/sysctl.d/.
# To override a whole file, create a new file with the same in
# /etc/sysctl.d/ and put new settings there. To override
# only specific settings, add a file with a lexically later
# name in /etc/sysctl.d/ and put new settings there.
#
# For more information, see sysctl.conf(5) and sysctl.d(5).
vm.swappiness = 1

--------------------------------------------------------

clear;mount

cgroup on /sys/fs/cgroup/net_cls,net_prio type cgroup (rw,nosuid,nodev,noexec,relatime,net_prio,net_cls)
cgroup on /sys/fs/cgroup/perf_event type cgroup (rw,nosuid,nodev,noexec,relatime,perf_event)
cgroup on /sys/fs/cgroup/blkio type cgroup (rw,nosuid,nodev,noexec,relatime,blkio)
cgroup on /sys/fs/cgroup/cpu,cpuacct type cgroup (rw,nosuid,nodev,noexec,relatime,cpuacct,cpu)
cgroup on /sys/fs/cgroup/cpuset type cgroup (rw,nosuid,nodev,noexec,relatime,cpuset)
cgroup on /sys/fs/cgroup/freezer type cgroup (rw,nosuid,nodev,noexec,relatime,freezer)
configfs on /sys/kernel/config type configfs (rw,relatime)
/dev/xvda2 on / type xfs (rw,relatime,seclabel,attr2,inode64,noquota)
selinuxfs on /sys/fs/selinux type selinuxfs (rw,relatime)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime,seclabel)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
mqueue on /dev/mqueue type mqueue (rw,relatime,seclabel)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=31,pgrp=1,timeout=300,minproto=5,maxproto=5,direct)
tmpfs on /run/user/1000 type tmpfs (rw,nosuid,nodev,relatime,seclabel,size=1497260k,mode=700,uid=1000,gid=1000)
[root@ip-192-168-0-175 ec2-user]# clear;mount
sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,relatime,seclabel)
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime)
devtmpfs on /dev type devtmpfs (rw,nosuid,seclabel,size=7598116k,nr_inodes=1899529,mode=755)
securityfs on /sys/kernel/security type securityfs (rw,nosuid,nodev,noexec,relatime)
tmpfs on /dev/shm type tmpfs (rw,nosuid,nodev,seclabel)
devpts on /dev/pts type devpts (rw,nosuid,noexec,relatime,seclabel,gid=5,mode=620,ptmxmode=000)
tmpfs on /run type tmpfs (rw,nosuid,nodev,seclabel,mode=755)
tmpfs on /sys/fs/cgroup type tmpfs (ro,nosuid,nodev,noexec,seclabel,mode=755)
cgroup on /sys/fs/cgroup/systemd type cgroup (rw,nosuid,nodev,noexec,relatime,xattr,release_agent=/usr/lib/systemd/systemd-cgroups-agent,name=systemd)
pstore on /sys/fs/pstore type pstore (rw,nosuid,nodev,noexec,relatime)
cgroup on /sys/fs/cgroup/devices type cgroup (rw,nosuid,nodev,noexec,relatime,devices)
cgroup on /sys/fs/cgroup/pids type cgroup (rw,nosuid,nodev,noexec,relatime,pids)
cgroup on /sys/fs/cgroup/hugetlb type cgroup (rw,nosuid,nodev,noexec,relatime,hugetlb)
cgroup on /sys/fs/cgroup/memory type cgroup (rw,nosuid,nodev,noexec,relatime,memory)
cgroup on /sys/fs/cgroup/net_cls,net_prio type cgroup (rw,nosuid,nodev,noexec,relatime,net_prio,net_cls)
cgroup on /sys/fs/cgroup/perf_event type cgroup (rw,nosuid,nodev,noexec,relatime,perf_event)
cgroup on /sys/fs/cgroup/blkio type cgroup (rw,nosuid,nodev,noexec,relatime,blkio)
cgroup on /sys/fs/cgroup/cpu,cpuacct type cgroup (rw,nosuid,nodev,noexec,relatime,cpuacct,cpu)
cgroup on /sys/fs/cgroup/cpuset type cgroup (rw,nosuid,nodev,noexec,relatime,cpuset)
cgroup on /sys/fs/cgroup/freezer type cgroup (rw,nosuid,nodev,noexec,relatime,freezer)
configfs on /sys/kernel/config type configfs (rw,relatime)
/dev/xvda2 on / type xfs (rw,relatime,seclabel,attr2,inode64,noquota)
selinuxfs on /sys/fs/selinux type selinuxfs (rw,relatime)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime,seclabel)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
mqueue on /dev/mqueue type mqueue (rw,relatime,seclabel)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=31,pgrp=1,timeout=300,minproto=5,maxproto=5,direct)
tmpfs on /run/user/1000 type tmpfs (rw,nosuid,nodev,relatime,seclabel,size=1497260k,mode=700,uid=1000,gid=1000)

-------------------------------------------------------------------
[root@ip-192-168-0-175 ec2-user]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda2       60G  982M   60G   2% /
devtmpfs        7.3G     0  7.3G   0% /dev
tmpfs           7.2G     0  7.2G   0% /dev/shm
tmpfs           7.2G   17M  7.2G   1% /run
tmpfs           7.2G     0  7.2G   0% /sys/fs/cgroup
tmpfs           1.5G     0  1.5G   0% /run/user/1000

--------------------------------------------------------

Disable transparent hugepage support:

[root@ip-192-168-0-51 ec2-user]# cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

-----------------------------------------------------------------
sudo wget install 

[root@ip-192-168-0-51 ec2-user]# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 192.168.0.51  netmask 255.255.255.0  broadcast 192.168.0.255
        inet6 fe80::7f:50ff:fefb:a6c3  prefixlen 64  scopeid 0x20<link>
        ether 02:7f:50:fb:a6:c3  txqueuelen 1000  (Ethernet)
        RX packets 2351  bytes 186192 (181.8 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2352  bytes 306173 (298.9 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 68  bytes 6260 (6.1 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 68  bytes 6260 (6.1 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

----------------------------------------------------------------------
sudo yum install bind-utils


[root@ip-192-168-0-51 ec2-user]# nslookup 192.168.0.51
Server:         192.168.0.2
Address:        192.168.0.2#53

Non-authoritative answer:
51.0.168.192.in-addr.arpa       name = ip-192-168-0-51.eu-west-1.compute.internal.

Authoritative answers can be found from:


        loop  txqueuelen 1  (Local Loopback)
        RX packets 68  bytes 6260 (6.1 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 68  bytes 6260 (6.1 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0


[root@ip-192-168-0-51 ec2-user]# nslookup 51.0.168.192.in-addr.-arpa
Server:         192.168.0.2
Address:        192.168.0.2#53

** server can't find 51.0.168.192.in-addr.-arpa: NXDOMAIN
-------------------------------------------------------------------

[root@ip-192-168-0-51 ec2-user]# service  nscd  status; service  ntpd  status
Redirecting to /bin/systemctl status  nscd.service
Unit nscd.service could not be found.
Redirecting to /bin/systemctl status  ntpd.service
Unit ntpd.service could not be found.
[root@ip-192-168-0-51 ec2-user]# /etc/rc.d/init.d/ [tab] NOT FOUND...
choose_repo         network             rhnsd
netconsole          rh-cloud-firstboot
[root@ip-192-168-0-51 ec2-user]# ps -aux|grep nscd



[root@ip-192-168-0-51 ec2-user]# service  nscd  status; service  ntpd  status
Redirecting to /bin/systemctl status  nscd.service
Unit nscd.service could not be found.
Redirecting to /bin/systemctl status  ntpd.service
Unit ntpd.service could not be found.
[root@ip-192-168-0-51 ec2-user]# /etc/rc.d/init.d/ [tab] NOT FOUND...
choose_repo         network             rhnsd
netconsole          rh-cloud-firstboot
[root@ip-192-168-0-51 ec2-user]# ps -aux|grep nscd
  
  [root@ip-192-168-0-175 ec2-user]# find / -type f -name "*nsc*"
  
  UNEXISTING DAEMONS??
yum install ntp
yum install nscd

Redirecting to /bin/systemctl status  ntpd.service
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-03-06 10:01:09 EST; 5s ago
  Process: 9943 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 9944 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─9944 /usr/sbin/ntpd -u ntp:ntp -g

Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:10 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: 0.0.0....
Mar 06 10:01:10 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: 0.0.0....
Mar 06 10:01:10 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: 0.0.0....

　
Hint: Some lines were ellipsized, use -l to show in full.
root@ip-192-168-0-51 ec2-user]# clear

　
[root@ip-192-168-0-51 ec2-user]# service nscd restart; service nscd status
Redirecting to /bin/systemctl restart  nscd.service
Redirecting to /bin/systemctl status  nscd.service
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-03-06 10:03:00 EST; 20ms ago
  Process: 9975 ExecStop=/usr/sbin/nscd --shutdown (code=exited, status=0/SUCCESS)
  Process: 9978 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 9979 (nscd)
   CGroup: /system.slice/nscd.service
           └─9979 /usr/sbin/nscd

Mar 06 10:03:00 ip-192-168-0-51.eu-west-1.compute.internal nscd[9979]: 9979 m...
Mar 06 10:03:00 ip-192-168-0-51.eu-west-1.compute.internal nscd[9979]: 9979 m...
Mar 06 10:03:00 ip-192-168-0-51.eu-west-1.compute.internal nscd[9979]: 9979 m...
Mar 06 10:03:00 ip-192-168-0-51.eu-west-1.compute.internal nscd[9979]: 9979 m...
Mar 06 10:03:00 ip-192-168-0-51.eu-west-1.compute.internal nscd[9979]: 9979 m...
Mar 06 10:03:00 ip-192-168-0-51.eu-west-1.compute.internal nscd[9979]: 9979 m...
Mar 06 10:03:00 ip-192-168-0-51.eu-west-1.compute.internal nscd[9979]: 9979 d...
Mar 06 10:03:00 ip-192-168-0-51.eu-west-1.compute.internal systemd[1]: Starte...
Mar 06 10:03:00 ip-192-168-0-51.eu-west-1.compute.internal nscd[9979]: 9979 s...
Mar 06 10:03:00 ip-192-168-0-51.eu-west-1.compute.internal nscd[9979]: 9979 A...
Hint: Some lines were ellipsized, use -l to show in full.
[root@ip-192-168-0-51 ec2-user]#

　
　
[root@ip-192-168-0-51 ec2-user]# service ntpd restart
Redirecting to /bin/systemctl restart  ntpd.service
[root@ip-192-168-0-51 ec2-user]# service ntpd status
Redirecting to /bin/systemctl status  ntpd.service
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-03-06 10:01:09 EST; 5s ago
  Process: 9943 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 9944 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─9944 /usr/sbin/ntpd -u ntp:ntp -g

Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:09 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: Listen...
Mar 06 10:01:10 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: 0.0.0....
Mar 06 10:01:10 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: 0.0.0....
Mar 06 10:01:10 ip-192-168-0-51.eu-west-1.compute.internal ntpd[9944]: 0.0.0....
Hint: Some lines were ellipsized, use -l to show in full.
[root@ip-192-168-0-51 ec2-user]#

service nscd restart; service nscd status;service ntpd restart; service ntpd status
