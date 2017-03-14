sudo yum install mariadb-server
sudo service mariadb stop
 
---------------------------------------------------

mkdir -p /usr/share/java/
cp -v ./mysql-connector-java-5.1.30.tar.gz /usr/share/java/
ls /usr/share/java

---------------------------------------------------

/usr/bin/mysql_secure_installation

NOTE: RUNNING ALL PARTS OF THIS SCRIPT IS RECOMMENDED FOR ALL MariaDB
      SERVERS IN PRODUCTION USE!  PLEASE READ EACH STEP CAREFULLY!

In order to log into MariaDB to secure it, we'll need the current
password for the root user.  If you've just installed MariaDB, and
you haven't set the root password yet, the password will be blank,
so you should just press enter here.

Enter current password for root (enter for none):
OK, successfully used password, moving on...

Setting the root password ensures that nobody can log into the MariaDB
root user without the proper authorisation.

Set root password? [Y/n] Y
New password:
Re-enter new password:
Password updated successfully!
Reloading privilege tables..
 ... Success!


By default, a MariaDB installation has an anonymous user, allowing anyone
to log into MariaDB without having to have a user account created for
them.  This is intended only for testing, and to make the installation
go a bit smoother.  You should remove them before moving into a
production environment.

Remove anonymous users? [Y/n] y
 ... Success!

Normally, root should only be allowed to connect from 'localhost'.  This
ensures that someone cannot guess at the root password from the network.

Disallow root login remotely? [Y/n] y
 ... Success!

By default, MariaDB comes with a database named 'test' that anyone can
access.  This is also intended only for testing, and should be removed
before moving into a production environment.

Remove test database and access to it? [Y/n] y
 - Dropping test database...
 ... Success!
 - Removing privileges on test database...
 ... Success!

Reloading the privilege tables will ensure that all changes made so far
will take effect immediately.

Reload privilege tables now? [Y/n] y
 ... Success!

Cleaning up...

All done!  If you've completed all of the above steps, your MariaDB
installation should now be secure.

Thanks for using MariaDB!

---------------------------------------------------

service mariadb restart
Redirecting to /bin/systemctl restart  mariadb.service
[root@ip-192-168-0-110 ~]# mysql -u root -p
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 2
Server version: 5.5.52-MariaDB MariaDB Server

Copyright (c) 2000, 2016, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> CREATE DATABASE scm;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> CREATE DATABASE rman;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> CREATE DATABASE hive
    -> ;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> CREATE DATABASE oozie;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> CREATE DATABASE hue;
Query OK, 1 row affected (0.00 sec)


MariaDB [(none)]> CREATE DATABASE sentry;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> exit

# mysql -u root -p
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 3
Server version: 5.5.52-MariaDB MariaDB Server

Copyright (c) 2000, 2016, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)

MariaDB [(none)]> SHOW VARIABLES like "%version%";
+-------------------------+---------------------+
| Variable_name           | Value               |
+-------------------------+---------------------+
| innodb_version          | 5.5.49-MariaDB-38.0 |
| protocol_version        | 10                  |
| slave_type_conversions  |                     |
| version                 | 5.5.52-MariaDB      |
| version_comment         | MariaDB Server      |
| version_compile_machine | x86_64              |
| version_compile_os      | Linux               |
+-------------------------+---------------------+
7 rows in set (0.00 sec)

MariaDB [(none)]> show processlist;
+----+------+-----------+------+---------+------+-------+------------------+----------+
| Id | User | Host      | db   | Command | Time | State | Info             | Progress |
+----+------+-----------+------+---------+------+-------+------------------+----------+
|  3 | root | localhost | NULL | Query   |    0 | NULL  | show processlist |    0.000 |
+----+------+-----------+------+---------+------+-------+------------------+----------+
1 row in set (0.00 sec)

MariaDB [(none)]>
