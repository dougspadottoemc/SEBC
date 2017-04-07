* Package info:
```
[root@ip-10-181-102-132 ~]# repoquery -i mariadb-server

Name        : mariadb-server
Version     : 5.5.52
Release     : 1.el7
Architecture: x86_64
Size        : 58203767
Packager    : Red Hat, Inc. <http://bugzilla.redhat.com/bugzilla>
Group       : Applications/Databases
URL         : http://mariadb.org
Repository  : rhui-REGION-rhel-server-releases
Summary     : The MariaDB server and related files
Source      : mariadb-5.5.52-1.el7.src.rpm
Description :
MariaDB is a multi-user, multi-threaded SQL database server. It is a
client/server implementation consisting of a server daemon (mysqld)
and many different client programs and libraries. This package contains
the MariaDB server and some accompanying files and directories.
MariaDB is a community developed branch of MySQL.
```

* Corresponding repo's info
```
[root@ip-10-181-102-132 ~]# cat /etc/yum.repos.d/redhat-rhui.repo
# The amazon ec2 region is now dynamically set via yum.  REGION can be replaced by the amazon ec2 region for debugging
[rhui-REGION-rhel-server-releases]
name=Red Hat Enterprise Linux Server 7 (RPMs)
mirrorlist=https://rhui2-cds01.REGION.aws.ce.redhat.com/pulp/mirror/content/dist/rhel/rhui/server/7/$releasever/$basearch/os
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release
sslverify=1
sslclientkey=/etc/pki/rhui/content-rhel7.key
sslclientcert=/etc/pki/rhui/product/content-rhel7.crt
sslcacert=/etc/pki/rhui/cdn.redhat.com-chain.crt
...
```