```bash
;
; BIND data file for robiulhossain.com
;
$TTL    3h
@       IN      SOA     ns1.robiulhossain.com. admin.robiulhossain.com. (
                          1        ; Serial
                          3h       ; Refresh after 3 hours
                          1h       ; Retry after 1 hour
                          1w       ; Expire after 1 week
                          1h )     ; Negative caching TTL of 1 day
;
@       IN      NS      ns1.robiulhossain.com.
@       IN      NS      ns2.robiulhossain.com.


robiulhossain.com.    IN      MX      10      mail.robiulhossain.com.
robiulhossain.com.    IN      A       188.245.99.15
ns1                     IN      A       188.245.99.15
ns2                     IN      A       192.168.0.11
www                     IN      CNAME   robiulhossain.com.
mail                    IN      A       188.245.99.15
ftp                     IN      CNAME   robiulhossain.com.
```

## ADD IT to config file

zone "robiulhossain.com" {
type master;
file "/etc/bind/zones/master/db.robiulhossain.com";
};

db.robiulhossain.com
