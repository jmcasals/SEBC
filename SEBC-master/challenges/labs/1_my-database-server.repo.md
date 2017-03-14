sudo yum install mariadb-server
sudo service mariadb stop

sudo yum repolist
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
repo id                                                                  repo name                                                                               status
rhui-REGION-client-config-server-7/x86_64                                Red Hat Update Infrastructure 2.0 Client Configuration Server 7                              6
rhui-REGION-rhel-server-releases/7Server/x86_64                          Red Hat Enterprise Linux Server 7 (RPMs)                                                14,038
rhui-REGION-rhel-server-rh-common/7Server/x86_64                         Red Hat Enterprise Linux Server 7 RH Common (RPMs)                                         209
repolist: 14,253


---------------------------------------------------

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

GRANT REPLICATION SLAVE ON *.* TO root@34.251.202.66  IDENTIFIED BY 'cloudera';
GRANT REPLICATION SLAVE ON *.* TO root@34.252.42.151  IDENTIFIED BY 'lolo';
//rest of nodes....same thing

..........
SHOW MASTER STATUS;
+-------------------------+----------+--------------+------------------+
| File                    | Position | Binlog_Do_DB | Binlog_Ignore_DB |
+-------------------------+----------+--------------+------------------+
| mysql_binary_log.000004 |     2904 |              |                  |
+-------------------------+----------+--------------+------------------+
1 row in set (0.00 sec)


show SLAVE STATUS;
+----------------------------------+----------------+-------------+-------------+---------------+-------------------------+---------------------+--------------------------+---------------+-------------------------+------------------+-------------------+-----------------+---------------------+--------------------+------------------------+-------------------------+-----------------------------+------------+------------+--------------+---------------------+-----------------+-----------------+----------------+---------------+--------------------+--------------------+--------------------+-----------------+-------------------+----------------+-----------------------+-------------------------------+---------------+---------------+----------------+----------------+-----------------------------+------------------+
| Slave_IO_State                   | Master_Host    | Master_User | Master_Port | Connect_Retry | Master_Log_File         | Read_Master_Log_Pos | Relay_Log_File           | Relay_Log_Pos | Relay_Master_Log_File   | Slave_IO_Running | Slave_SQL_Running | Replicate_Do_DB | Replicate_Ignore_DB | Replicate_Do_Table | Replicate_Ignore_Table | Replicate_Wild_Do_Table | Replicate_Wild_Ignore_Table | Last_Errno | Last_Error | Skip_Counter | Exec_Master_Log_Pos | Relay_Log_Space | Until_Condition | Until_Log_File | Until_Log_Pos | Master_SSL_Allowed | Master_SSL_CA_File | Master_SSL_CA_Path | Master_SSL_Cert | Master_SSL_Cipher | Master_SSL_Key | Seconds_Behind_Master | Master_SSL_Verify_Server_Cert | Last_IO_Errno | Last_IO_Error | Last_SQL_Errno | Last_SQL_Error | Replicate_Ignore_Server_Ids | Master_Server_Id |
+----------------------------------+----------------+-------------+-------------+---------------+-------------------------+---------------------+--------------------------+---------------+-------------------------+------------------+-------------------+-----------------+---------------------+--------------------+------------------------+-------------------------+-----------------------------+------------+------------+--------------+---------------------+-----------------+-----------------+----------------+---------------+--------------------+--------------------+--------------------+-----------------+-------------------+----------------+-----------------------+-------------------------------+---------------+---------------+----------------+----------------+-----------------------------+------------------+
| Waiting for master to send event | 34.248.238.199 | root        |        3306 |            60 | mysql_binary_log.000004 |                2904 | mariadb-relay-bin.000004 |           987 | mysql_binary_log.000004 | Yes              | Yes               |                 |                     |                    |                        |                         |                             |          0 |            |            0 |                2904 |            1283 | None            |                |             0 | No                 |                    |                    |                 |                   |                |                     0 | No                            |             0 |               |              0 |                |                             |                1 |
+----------------------------------+----------------+-------------+-------------+---------------+-------------------------+---------------------+--------------------------+---------------+-------------------------+------------------+-------------------+-----------------+---------------------+--------------------+------------------------+-------------------------+-----------------------------+------------+------------+--------------+---------------------+-----------------+-----------------+----------------+---------------+--------------------+--------------------+--------------------+-----------------+-------------------+----------------+-----------------------+-------------------------------+---------------+---------------+----------------+----------------+-----------------------------+------------------+

etc...

----------------------------------------------------------------------------




