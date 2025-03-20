To get the IPv4 and IPv6 addresses of a public domain name on RHEL, use the following methods:

1. Using `getent`

>This method queries the system's Name Service Switch (NSS) configuration:

```
[hungtx@localhost ~]$ getent ahosts google.com
2a00:1450:4001:828::200e STREAM google.com
2a00:1450:4001:828::200e DGRAM  
2a00:1450:4001:828::200e RAW    
142.250.185.174 STREAM 
142.250.185.174 DGRAM  
142.250.185.174 RAW    
[hungtx@localhost ~]$ getent ahosts google.com | awk '/STREAM/ {print $1}'
2a00:1450:4001:828::200e
142.250.185.174
[hungtx@localhost ~]$
```

To get the IPv6 address of a public domain name on RHEL (Red Hat Enterprise Linux), you can use the following methods:
1. Using getent

This method queries the system's Name Service Switch (NSS) configuration:

getent ahosts example.com | awk '/STREAM/ {print $1}'

This will return both IPv4 and IPv6 addresses. To get only IPv6:

getent ahosts example.com | awk '$1 ~ /:/ {print $1}'

2. Using dig (from bind-utils)

If bind-utils is installed, use dig:

dig AAAA example.com +short

3. Using host

Another way is using host:

host -t AAAA example.com

4. Using nslookup

If nslookup is available:

nslookup -query=AAAA example.com

5. Using ping6

This will try to reach the domain over IPv6 and confirm connectivity:

ping6 example.com

Let me know if you need help installing tools like bind-utils or troubleshooting! 🚀
