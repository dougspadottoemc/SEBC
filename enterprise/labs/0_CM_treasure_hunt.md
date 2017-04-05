* What is ubertask optimization?
   It's a feature that enables the reuse of a JVM for small tasks (what is a small task can be defined by configuration and can take into consideration input size, number of mappers and number of reducers).

* Where in CM is the Kerberos Security Realm value displayed?
   On Administration > Settings > Kerberos

* Which CDH service(s) host a property for enabling Kerberos authentication?
   On our current Core Hadoop install, Zookeeper, HiveServer2 and HDFS (Authentication for HTTP Web-Consoles)

* How do you upgrade the CM agents?
   After you upgrade the Cloudera Manager Server, you can use an upgrade wizard that is invoked when you connect to the Admin Console or manually install the Cloudera Manager Agent packages.

* Give the tsquery statement used to chart Hue's CPU utilization?
  `select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName="Hue"`

* Name all the roles that make up the Hive service
  HIVESERVER2, HIVEMETASTORE, WEBHCAT, GATEWAY

* What steps must be completed before integrating Cloudera Manager with Kerberos?
   Get or create a Kerberos Principal for the CM server.
