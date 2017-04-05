### Stop Hive

``` [ec2-user@ip-10-179-156-49 ~]$ curl -X POST -u "dougspadottoemc:cloudera" -i http://ec2-23-22-152-100.compute-1.amazonaws.com:7180/api/v2/clusters/dougspadottoemc/services/hive/commands/stop
HTTP/1.1 200 OK
Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=1b0bqgbtqpxumx3zih8zg523h;Path=/;HttpOnly
Content-Type: application/json
Date: Wed, 05 Apr 2017 13:20:37 GMT
Transfer-Encoding: chunked
Server: Jetty(6.1.26.cloudera.4)

{
  "id" : 1243,
  "name" : "Stop",
  "startTime" : "2017-04-05T13:20:37.183Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
  ```

### Checking if command ran ok

``` [ec2-user@ip-10-179-156-49 ~]$ curl -X GET -u "dougspadottoemc:cloudera" -i http://ec2-23-22-152-100.compute-1.amazonaws.com:7180/api/v2/commands/1243                                       HTTP/1.1 200 OK
Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=ymcs138gknkv1fdkk1yq6t2we;Path=/;HttpOnly
Content-Type: application/json
Date: Wed, 05 Apr 2017 13:21:26 GMT
Transfer-Encoding: chunked
Server: Jetty(6.1.26.cloudera.4)

{
  "id" : 1243,
  "name" : "Stop",
  "startTime" : "2017-04-05T13:20:37.183Z",
  "endTime" : "2017-04-05T13:20:39.171Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully stopped service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 1244,
      "name" : "Stop",
      "startTime" : "2017-04-05T13:20:37.185Z",
      "endTime" : "2017-04-05T13:20:39.170Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-a89c5c6d0abf925e2a0511b2019dba01"
      }
    }, {
      "id" : 1245,
      "name" : "Stop",
      "startTime" : "2017-04-05T13:20:37.187Z",
      "endTime" : "2017-04-05T13:20:39.170Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-WEBHCAT-a89c5c6d0abf925e2a0511b2019dba01"
      }
    }, {
      "id" : 1246,
      "name" : "Stop",
      "startTime" : "2017-04-05T13:20:37.188Z",
      "endTime" : "2017-04-05T13:20:39.162Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-a89c5c6d0abf925e2a0511b2019dba01"
      }
    } ]
  } ```


### Start Hive

``` [ec2-user@ip-10-179-156-49 ~]$ curl -X POST -u "dougspadottoemc:cloudera" -i http://ec2-23-22-152-100.compute-1.amazonaws.com:7180/api/v2/clusters/dougspadottoemc/services/hive/commands/start
HTTP/1.1 200 OK
Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=m0i7fiwzjwka139dbnr72fbq5;Path=/;HttpOnly
Content-Type: application/json
Date: Wed, 05 Apr 2017 13:24:47 GMT
Transfer-Encoding: chunked
Server: Jetty(6.1.26.cloudera.4)

{
  "id" : 1248,
  "name" : "Start",
  "startTime" : "2017-04-05T13:24:47.066Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
```

### Checking if command ran ok
``` [ec2-user@ip-10-179-156-49 ~]$ curl -X GET -u "dougspadottoemc:cloudera" -i http://ec2-23-22-152-100.compute-1.amazonaws.com:7180/api/v2/commands/1248                                       HTTP/1.1 200 OK
Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=b53q59re31oaxu7jm6hqt6df;Path=/;HttpOnly
Content-Type: application/json
Date: Wed, 05 Apr 2017 13:26:28 GMT
Transfer-Encoding: chunked
Server: Jetty(6.1.26.cloudera.4)

{
  "id" : 1248,
  "name" : "Start",
  "startTime" : "2017-04-05T13:24:47.066Z",
  "endTime" : "2017-04-05T13:25:09.476Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully started service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 1249,
      "name" : "Start",
      "startTime" : "2017-04-05T13:24:47.092Z",
      "endTime" : "2017-04-05T13:25:09.469Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-a89c5c6d0abf925e2a0511b2019dba01"
      }
    }, {
      "id" : 1251,
      "name" : "Start",
      "startTime" : "2017-04-05T13:24:47.208Z",
      "endTime" : "2017-04-05T13:25:09.469Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-a89c5c6d0abf925e2a0511b2019dba01"
      }
    }, {
      "id" : 1250,
      "name" : "Start",
      "startTime" : "2017-04-05T13:24:47.168Z",
      "endTime" : "2017-04-05T13:25:09.462Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-WEBHCAT-a89c5c6d0abf925e2a0511b2019dba01"
      }
    } ]
  } ```

### Checking Hive status

For that, I checked the role, and within it I can see the status (I removed spurious output):

``` [ec2-user@ip-10-179-156-49 ~]$ curl -X GET -u "dougspadottoemc:cloudera" -i http://ec2-23-22-152-100.compute-1.amazonaws.com:7180/api/v2/clusters/dougspadottoemc/services/hive/roles
HTTP/1.1 200 OK
Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=10zwfr59qd399qni4t6vo6vo6;Path=/;HttpOnly
Content-Type: application/json
Date: Wed, 05 Apr 2017 13:31:37 GMT
Transfer-Encoding: chunked
Server: Jetty(6.1.26.cloudera.4)

{
  "items" : [ {
    "name" : "hive-GATEWAY-b703c02679ba9f49263df0978c692d9b",
    "type" : "GATEWAY",
    "serviceRef" : {
      "clusterName" : "cluster",
      "serviceName" : "hive"
    },
    "hostRef" : {
      "hostId" : "8743d4e1-4bb6-4bb1-a48f-95f3d1e80ed5"
    },
    "roleUrl" : "http://ip-10-179-156-49.ec2.internal:7180/cmf/roleRedirect/hive-GATEWAY-b703c02679ba9f49263df0978c692d9b",
    "roleState" : "NA",
    "healthSummary" : "GOOD",
    "healthChecks" : [ ],
    "configStale" : false,
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED"
  }, {
    "name" : "hive-HIVEMETASTORE-a89c5c6d0abf925e2a0511b2019dba01",
    "type" : "HIVEMETASTORE",
    "serviceRef" : {
      "clusterName" : "cluster",
      "serviceName" : "hive"
    },
    "hostRef" : {
      "hostId" : "3fe4afa7-95b4-4b6f-b816-c015b80bb579"
    },
    "roleUrl" : "http://ip-10-179-156-49.ec2.internal:7180/cmf/roleRedirect/hive-HIVEMETASTORE-a89c5c6d0abf925e2a0511b2019dba01",
    "roleState" : "STARTED",
  ...
  }, {
    "name" : "hive-WEBHCAT-a89c5c6d0abf925e2a0511b2019dba01",
    "type" : "WEBHCAT",
  ...
    "roleState" : "STARTED",
    "healthSummary" : "GOOD",
 ...
  }, {
    "name" : "hive-GATEWAY-3c5aebf5cb1306e9b452b69e6a63b84f",
    "type" : "GATEWAY",
   ...
    "roleState" : "NA",... // which is ok as it's a gateway

  }, {
    "name" : "hive-GATEWAY-ce7bbe6ba0ba658228d1d7799ae519ee",
    "type" : "GATEWAY",
    ...
    "roleState" : "NA",
    ...
  }, {
    "name" : "hive-GATEWAY-d45096e224585b1232c846bccaeb6f47",
    "type" : "GATEWAY",
  ...
    "roleState" : "NA",
  }, {
    "name" : "hive-GATEWAY-a89c5c6d0abf925e2a0511b2019dba01",
    "type" : "GATEWAY",
   ...
    "roleState" : "NA",
   ...
  }, {
    "name" : "hive-HIVESERVER2-a89c5c6d0abf925e2a0511b2019dba01",
    "type" : "HIVESERVER2",
    ...
    "roleState" : "STARTED",
    "healthSummary" : "GOOD",
   ...
  } ] ```
