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
