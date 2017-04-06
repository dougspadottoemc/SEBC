```
[libdefaults]
default_realm = CLOUDERA.BOOTCAMP
dns_lookup_kdc = false
dns_lookup_realm = false
ticket_lifetime = 86400
renew_lifetime = 604800
forwardable = true
default_tgs_enctypes = rc4-hmac
default_tkt_enctypes = rc4-hmac
permitted_enctypes = rc4-hmac
udp_preference_limit = 1
kdc_timeout = 3000
[realms]
CLOUDERA.BOOTCAMP = {
kdc = ip-10-179-156-49.ec2.internal
admin_server = ip-10-179-156-49.ec2.internal
}
```