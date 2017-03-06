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
  
  UNEXISTING DAEMONS
