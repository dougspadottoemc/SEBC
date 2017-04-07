* List the cloud provider you are using (AWS, GCE, Azure, other): AWS
 
*List the nodes you are using by IP address and name
```
10.156.39.216   ip-10-156-39-216.ec2.internal cb5
10.229.31.57    ip-10-229-31-57.ec2.internal cb4
10.167.0.133    ip-10-167-0-133.ec2.internal cb3
10.146.51.155   ip-10-146-51-155.ec2.internal cb2
10.181.102.132  ip-10-181-102-132.ec2.internal cb1
```

 * List the Linux release you are using
```
[ec2-user@ip-10-181-102-132 ~]$ cat /etc/redhat-release
Red Hat Enterprise Linux Server release 7.3 (Maipo)
```

* Demonstrate the disk capacity available on each node is >= 30 GB
```
[ec2-user@ip-10-181-102-132 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda2       80G  1.2G   79G   2% /
...
```

* List the command and output for yum repolist enabled
```
[root@ip-10-181-102-132 ~]# yum repolist
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
repo id                                                                             repo name                                                                                          status
rhui-REGION-client-config-server-7/x86_64                                           Red Hat Update Infrastructure 2.0 Client Configuration Server 7                                         6
rhui-REGION-rhel-server-releases/7Server/x86_64                                     Red Hat Enterprise Linux Server 7 (RPMs)                                                           14,050
rhui-REGION-rhel-server-rh-common/7Server/x86_64                                    Red Hat Enterprise Linux Server 7 RH Common (RPMs)                                                    225
repolist: 14,281
```

* Add users neymar and ronaldo and groups barca and merengues
```
[root@ip-10-181-102-132 ~]# useradd -u 2010 neymar
[root@ip-10-181-102-132 ~]# useradd -u 2016 ronaldo
[root@ip-10-181-102-132 ~]# groupadd barca
[root@ip-10-181-102-132 ~]# groupadd merengues
[root@ip-10-181-102-132 ~]# usermod -a -G barca ronaldo
[root@ip-10-181-102-132 ~]# usermod -a -G merengues neymar
[root@ip-10-181-102-132 ~]# cat /etc/passwd | grep neymar
neymar:x:2010:2010::/home/neymar:/bin/bash
[root@ip-10-181-102-132 ~]# cat /etc/passwd | grep ronaldo
ronaldo:x:2016:2016::/home/ronaldo:/bin/bash
[root@ip-10-181-102-132 ~]# cat /etc/group | grep barca
barca:x:2017:ronaldo
[root@ip-10-181-102-132 ~]# cat /etc/group | grep merengues
merengues:x:2018:neymar
```
_reproduced the above on all nodes_
