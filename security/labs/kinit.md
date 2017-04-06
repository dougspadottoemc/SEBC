### kinit my test user

```
[root@ip-10-179-156-49 krb5kdc]# kinit dougspadottoemc
Password for dougspadottoemc@CLOUDERA.BOOTCAMP:
You have new mail in /var/spool/mail/root
[root@ip-10-179-156-49 krb5kdc]# klist dougspadottoemc@CLOUDERA.BOOTCAMP
```

### List its credentials
```
[root@ip-10-179-156-49 krb5kdc]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: dougspadottoemc@CLOUDERA.BOOTCAMP

Valid starting       Expires              Service principal
04/05/2017 21:19:15  04/06/2017 21:19:15  krbtgt/CLOUDERA.BOOTCAMP@CLOUDERA.BOOTCAMP
        renew until 04/12/2017 21:19:15
```
