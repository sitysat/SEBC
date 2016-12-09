List the command and output of ls /etc/yum.repos.d in challenges/labs/2_cm.md
```
[root@ip-172-31-3-217 ~]# ls /etc/yum.repos.d/
cloudera-manager.repo  redhat.repo                     redhat-rhui.repo  rhui-load-balancers.conf
mysql-community.repo   redhat-rhui-client-config.repo  rhel-source.repo
```

Use the scm_prepare_database.sh script to write your db.properties file and list the full cmd
```
[root@ip-172-31-3-217 ~]# /usr/share/cmf/schema/scm_prepare_database.sh -h ip-172-31-3-218.ap-southeast-1.compute.internal -u root -p --scm-host ip-172-31-3-217.ap-southeast-1.compute.internal mysql scm scm -f
Enter database password:
Enter SCM password:
JAVA_HOME=/usr/java/jdk1.7.0_75
Verifying that we can write to /etc/cloudera-scm-server
log4j:ERROR Could not find value for key log4j.appender.A
log4j:ERROR Could not instantiate appender named "A".
[2016-12-08 20:43:50,309]ERROR     1[main] - com.cloudera.enterprise.dbutil.DbProvisioner.executeSql(DbProvisioner.java) - Exception when creating/dropping database with user 'root' and jdbc url 'jdbc:mysql://ip-172-31-3-218.ap-southeast-1.compute.internal/?useUnicode=true&characterEncoding=UTF-8'
java.sql.SQLException: Can't create database 'scm'; database exists
        at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:964)
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3970)
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3906)
        at com.mysql.jdbc.MysqlIO.sendCommand(MysqlIO.java:2524)
        at com.mysql.jdbc.MysqlIO.sqlQueryDirect(MysqlIO.java:2677)
        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2545)
        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2503)
        at com.mysql.jdbc.StatementImpl.executeInternal(StatementImpl.java:839)
        at com.mysql.jdbc.StatementImpl.execute(StatementImpl.java:739)
        at com.cloudera.enterprise.dbutil.DbProvisioner.executeSql(DbProvisioner.java:286)
        at com.cloudera.enterprise.dbutil.DbProvisioner.doMain(DbProvisioner.java:95)
        at com.cloudera.enterprise.dbutil.DbProvisioner.main(DbProvisioner.java:110)
[2016-12-08 20:43:50,317]ERROR     9[main] - com.cloudera.enterprise.dbutil.DbProvisioner.main(DbProvisioner.java) - Stack Trace:
java.sql.SQLException: Can't create database 'scm'; database exists
        at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:964)
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3970)
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3906)
        at com.mysql.jdbc.MysqlIO.sendCommand(MysqlIO.java:2524)
        at com.mysql.jdbc.MysqlIO.sqlQueryDirect(MysqlIO.java:2677)
        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2545)
        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2503)
        at com.mysql.jdbc.StatementImpl.executeInternal(StatementImpl.java:839)
        at com.mysql.jdbc.StatementImpl.execute(StatementImpl.java:739)
        at com.cloudera.enterprise.dbutil.DbProvisioner.executeSql(DbProvisioner.java:286)
        at com.cloudera.enterprise.dbutil.DbProvisioner.doMain(DbProvisioner.java:95)
        at com.cloudera.enterprise.dbutil.DbProvisioner.main(DbProvisioner.java:110)
--> Error 1, ignoring (because force flag is set)
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_75/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
log4j:ERROR Could not find value for key log4j.appender.A
log4j:ERROR Could not instantiate appender named "A".
[2016-12-08 20:43:50,942] INFO     1[main] - com.cloudera.enterprise.dbutil.DbCommandExecutor.parseSqlState(DbCommandExecutor.java) - Unable to login using supplied username/password.
[2016-12-08 20:43:50,947]ERROR     6[main] - com.cloudera.enterprise.dbutil.DbCommandExecutor$DbConnectionTestException.logError(DbCommandExecutor.java) - Error when connecting to database.
java.sql.SQLException: Access denied for user 'scm'@'ip-172-31-3-217.ap-southeast-1.compute.internal' (using password: YES)
        at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:964)
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3970)
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3906)
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:873)
        at com.mysql.jdbc.MysqlIO.proceedHandshakeWithPluggableAuthentication(MysqlIO.java:1710)
        at com.mysql.jdbc.MysqlIO.doHandshake(MysqlIO.java:1226)
        at com.mysql.jdbc.ConnectionImpl.coreConnect(ConnectionImpl.java:2253)
        at com.mysql.jdbc.ConnectionImpl.connectOneTryOnly(ConnectionImpl.java:2284)
        at com.mysql.jdbc.ConnectionImpl.createNewIO(ConnectionImpl.java:2083)
        at com.mysql.jdbc.ConnectionImpl.<init>(ConnectionImpl.java:806)
        at com.mysql.jdbc.JDBC4Connection.<init>(JDBC4Connection.java:47)
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:57)
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45)
        at java.lang.reflect.Constructor.newInstance(Constructor.java:526)
        at com.mysql.jdbc.Util.handleNewInstance(Util.java:425)
        at com.mysql.jdbc.ConnectionImpl.getInstance(ConnectionImpl.java:410)
        at com.mysql.jdbc.NonRegisteringDriver.connect(NonRegisteringDriver.java:328)
        at java.sql.DriverManager.getConnection(DriverManager.java:571)
        at java.sql.DriverManager.getConnection(DriverManager.java:215)
        at com.cloudera.enterprise.dbutil.DbCommandExecutor.testDbConnection(DbCommandExecutor.java:243)
        at com.cloudera.enterprise.dbutil.DbCommandExecutor.main(DbCommandExecutor.java:137)
[2016-12-08 20:43:50,951]ERROR    10[main] - com.cloudera.enterprise.dbutil.DbCommandExecutor$DbConnectionTestException.logError(DbCommandExecutor.java) - Exiting with exit code 8
--> Error 8, ignoring (because force flag is set)
All done, your SCM database is configured correctly!

[root@ip-172-31-3-217 ~]# cat /etc/cloudera-scm-server/db.properties
# Auto-generated by scm_prepare_database.sh on Thu Dec  8 20:43:50 EST 2016
#
# For information describing how to configure the Cloudera Manager Server
# to connect to databases, see the "Cloudera Manager Installation Guide."
#
com.cloudera.cmf.db.type=mysql
com.cloudera.cmf.db.host=ip-172-31-3-218.ap-southeast-1.compute.internal
com.cloudera.cmf.db.name=scm
com.cloudera.cmf.db.user=scm
com.cloudera.cmf.db.password=password
com.cloudera.cmf.db.setupType=EXTERNAL

```