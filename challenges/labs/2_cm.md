### Repos

```
[root@ip-10-181-102-132 ~]# ls -la ls /etc/yum.repos.d
ls: cannot access ls: No such file or directory
/etc/yum.repos.d:
total 36
drwxr-xr-x.  2 root root  119 Apr  7 09:29 .
drwxr-xr-x. 77 root root 8192 Apr  7 10:18 ..
-rw-r--r--.  1 root root  358 Oct 20 13:01 redhat.repo
-rw-r--r--.  1 root root  607 Apr  7 09:29 redhat-rhui-client-config.repo
-rw-r--r--.  1 root root 8679 Apr  7 09:29 redhat-rhui.repo
-rw-r--r--.  1 root root   80 Apr  7 09:29 rhui-load-balancers.conf
```

### SCM database setup (from node2 to node1 where the DB is)
```
[root@ip-10-146-51-155 ~]# /usr/share/cmf/schema/scm_prepare_database.sh mysql scm root admin -h ip-10-181-102-132.ec2.internal --scm-host ip-10-146-51-155.ec2.internal -utemp -ptemp
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
```