### Hostname
```
MariaDB [(none)]> select @@hostname;
+--------------------------------+
| @@hostname                     |
+--------------------------------+
| ip-10-181-102-132.ec2.internal |
+--------------------------------+
1 row in set (0.00 sec)
```

### Database version
```
MariaDB [(none)]> select @@version;
+----------------+
| @@version      |
+----------------+
| 5.5.52-MariaDB |
+----------------+
1 row in set (0.00 sec)
```

### All Databases
```
MariaDB [(none)]> show databases
    -> ;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hue                |
| metastore          |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)
```