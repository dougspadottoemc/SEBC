### ls /user
```
[ec2-user@ip-10-181-102-132 ~]$ hdfs dfs -ls /user
Found 6 items
drwxrwxrwx   - mapred  hadoop             0 2017-04-07 11:58 /user/history
drwxrwxr-t   - hive    hive               0 2017-04-07 11:58 /user/hive
drwxrwxr-x   - hue     hue                0 2017-04-07 11:59 /user/hue
drwxr-xr-x   - neymar  merengues          0 2017-04-07 12:01 /user/neymar
drwxrwxr-x   - oozie   oozie              0 2017-04-07 11:59 /user/oozie
drwxr-xr-x   - ronaldo barca              0 2017-04-07 12:02 /user/ronaldo
```

### CM API call
```
[ec2-user@ip-10-181-102-132 ~]$ curl -X GET -u "admin:admin" -i http://ec2-54-147-51-236.compute-1.amazonaws.com:7180/api/v14/hosts                                                          HTTP/1.1 200 OKc2-54-147-51-236.compute-1.amazonaws.com:7180/api/v14/h                                                                                                                       Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=1ucms5idxwb6nbyfyc0hxfsnv;Path=/;HttpOnly
Content-Type: application/json
Date: Fri, 07 Apr 2017 16:06:34 GMT
Transfer-Encoding: chunked
Server: Jetty(6.1.26.cloudera.4)

{
  "items" : [ {
    "hostId" : "ca680478-f1f4-4808-b13c-0601d58e71ff",
    "ipAddress" : "10.146.51.155",
    "hostname" : "ip-10-146-51-155.ec2.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-146-51-155.ec2.internal:7180/cmf/hostRedirect/ca680478-f1f4-4808-b13c-0601d58e71ff",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15331930112
  }, {
    "hostId" : "cfe6dd9b-12f4-4458-a3c8-b29fafaaf5e8",
    "ipAddress" : "10.156.39.216",
    "hostname" : "ip-10-156-39-216.ec2.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-146-51-155.ec2.internal:7180/cmf/hostRedirect/cfe6dd9b-12f4-4458-a3c8-b29fafaaf5e8",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15331930112
  }, {
    "hostId" : "1469aba5-824c-4bf6-9f81-7adf43f4a815",
    "ipAddress" : "10.167.0.133",
    "hostname" : "ip-10-167-0-133.ec2.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-146-51-155.ec2.internal:7180/cmf/hostRedirect/1469aba5-824c-4bf6-9f81-7adf43f4a815",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15331930112
  }, {
    "hostId" : "3eb2dfd3-d610-44e2-a331-1a8d76334c77",
    "ipAddress" : "10.181.102.132",
    "hostname" : "ip-10-181-102-132.ec2.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-146-51-155.ec2.internal:7180/cmf/hostRedirect/3eb2dfd3-d610-44e2-a331-1a8d76334c77",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15331930112
  }, {
    "hostId" : "f2bfcfcc-72d8-40ab-b38c-da2f04e4fa9b",
    "ipAddress" : "10.229.31.57",
    "hostname" : "ip-10-229-31-57.ec2.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-146-51-155.ec2.internal:7180/cmf/hostRedirect/f2bfcfcc-72d8-40ab-b38c-da2f04e4fa9b",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15331930112
  } ]
```