

ls -lFa /etc/yum.repos.d
total 40
drwxr-xr-x.  2 root root  148 Mar 10 03:02 ./
drwxr-xr-x. 77 root root 8192 Mar 10 04:11 ../
-rw-r--r--   1 root root  195 Nov 15 23:51 cloudera-manager.repo
-rw-r--r--.  1 root root  358 Oct 20 13:01 redhat.repo
-rw-r--r--   1 root root  607 Mar 10 02:34 redhat-rhui-client-config.repo
-rw-r--r--.  1 root root 8679 Mar 10 02:34 redhat-rhui.repo
-rw-r--r--   1 root root   80 Mar 10 02:34 rhui-load-balancers.conf

a/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Unable to login using supplied username/password.
[                          main] DbCommandExecutor              ERROR Error when connecting to database.
java.sql.SQLException: Access denied for user 'root'@'localhost' (using password: YES)
        at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:1084)[mysql-connector-java.jar:]
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:4232)[mysql-connector-java.jar:]
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:4164)[mysql-connector-java.jar:]
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:926)[mysql-connector-java.jar:]
        at com.mysql.jdbc.MysqlIO.proceedHandshakeWithPluggableAuthentication(MysqlIO.java:1748)[mysql-connector-java.jar:]
        at com.mysql.jdbc.MysqlIO.doHandshake(MysqlIO.java:1288)[mysql-connector-java.jar:]
        at com.mysql.jdbc.ConnectionImpl.coreConnect(ConnectionImpl.java:2506)[mysql-connector-java.jar:]
        at com.mysql.jdbc.ConnectionImpl.connectOneTryOnly(ConnectionImpl.java:2539)[mysql-connector-java.jar:]
        at com.mysql.jdbc.ConnectionImpl.createNewIO(ConnectionImpl.java:2321)[mysql-connector-java.jar:]
        at com.mysql.jdbc.ConnectionImpl.<init>(ConnectionImpl.java:832)[mysql-connector-java.jar:]
        at com.mysql.jdbc.JDBC4Connection.<init>(JDBC4Connection.java:46)[mysql-connector-java.jar:]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)[:1.7.0_67]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:57)[:1.7.0_67]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45)[:1.7.0_67]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:526)[:1.7.0_67]
        at com.mysql.jdbc.Util.handleNewInstance(Util.java:409)[mysql-connector-java.jar:]
        at com.mysql.jdbc.ConnectionImpl.getInstance(ConnectionImpl.java:417)[mysql-connector-java.jar:]
        at com.mysql.jdbc.NonRegisteringDriver.connect(NonRegisteringDriver.java:344)[mysql-connector-java.jar:]
        at java.sql.DriverManager.getConnection(DriverManager.java:571)[:1.7.0_67]
        at java.sql.DriverManager.getConnection(DriverManager.java:215)[:1.7.0_67]
        at com.cloudera.enterprise.dbutil.DbCommandExecutor.testDbConnection(DbCommandExecutor.java:253)[db-common-5.10.0.jar:]
        at com.cloudera.enterprise.dbutil.DbCommandExecutor.main(DbCommandExecutor.java:138)[db-common-5.10.0.jar:]
[                          main] DbCommandExecutor              ERROR Exiting with exit code 8
--> Error 8, ignoring (because force flag is set)
