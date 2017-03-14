

ls -lFa /etc/yum.repos.d
total 40
drwxr-xr-x.  2 root root  148 Mar 10 03:02 ./
drwxr-xr-x. 77 root root 8192 Mar 10 04:11 ../
-rw-r--r--   1 root root  195 Nov 15 23:51 cloudera-manager.repo
-rw-r--r--.  1 root root  358 Oct 20 13:01 redhat.repo
-rw-r--r--   1 root root  607 Mar 10 02:34 redhat-rhui-client-config.repo
-rw-r--r--.  1 root root 8679 Mar 10 02:34 redhat-rhui.repo
-rw-r--r--   1 root root   80 Mar 10 02:34 rhui-load-balancers.conf
sudo /usr/bin/mysql_secure_installation -> To set root password
sudo /usr/bin/mysql_secure_installation
Remove anonymous users? [Y/n] y
... Success!
 
Normally, root should only be allowed to connect from 'localhost'.                                                                                                    This
ensures that someone cannot guess at the root password from the netw                                                                                                  ork.
 
Disallow root login remotely? [Y/n] y
... Success!
 
By default, MariaDB comes with a database named 'test' that anyone c                                                                                                  an
access.  This is also intended only for testing, and should be remov                                                                                                  ed
before moving into a production environment.
 
Remove test database and access to it? [Y/n] y
- Dropping test database...
... Success!
- Removing privileges on test database...
... Success!
 
Reloading the privilege tables will ensure that all changes made so                                                                                                   far
will take effect immediately.
 
Reload privilege tables now? [Y/n] y
... Success!
 
Cleaning up...
 
All done!  If you've completed all of the above steps, your MariaDB
installation should now be secure.
 
 
JDBC:
wget http://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.30.tar.gz
tar zxvf mysql-connector-java-5.1.31.tar.gz
mkdir /usr/share/java
cp mysql-connector-java-5.1.30/mysql-connector-java-5.1.30-bin.jar  /usr/share/java/mysql-connector-java.jar

