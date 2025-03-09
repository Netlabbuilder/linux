To list all the network interfaces (like wired, wireless, loopback, etc.), use the following commands:
- `ip add show`
```
[hungtx@linux ~]$ ip add show
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host 
       valid_lft forever preferred_lft forever
2: enp2s0f1: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 40:16:7e:86:aa:c1 brd ff:ff:ff:ff:ff:ff
    inet 192.168.178.59/24 brd 192.168.178.255 scope global dynamic noprefixroute enp2s0f1
       valid_lft 858097sec preferred_lft 858097sec
    inet6 2003:e6:b707:8c00:4216:7eff:fe86:aac1/64 scope global dynamic noprefixroute 
       valid_lft 6921sec preferred_lft 983sec
    inet6 fdd1:1aef:54b9:0:4216:7eff:fe86:aac1/64 scope global dynamic noprefixroute 
       valid_lft 6921sec preferred_lft 3321sec
    inet6 fe80::4216:7eff:fe86:aac1/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever
3: wlp3s0: <BROADCAST,MULTICAST> mtu 1500 qdisc noop state DOWN group default qlen 1000
    link/ether b6:ed:4c:f6:b0:fd brd ff:ff:ff:ff:ff:ff permaddr 54:27:1e:23:94:3b
[hungtx@linux ~]$ 
```
- `ifconfig -a`
```
hungtx@linux ~]$ ifconfig -a
enp2s0f1: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.178.59  netmask 255.255.255.0  broadcast 192.168.178.255
        inet6 fdd1:1aef:54b9:0:4216:7eff:fe86:aac1  prefixlen 64  scopeid 0x0<global>
        inet6 fe80::4216:7eff:fe86:aac1  prefixlen 64  scopeid 0x20<link>
        inet6 2003:e6:b707:8c00:4216:7eff:fe86:aac1  prefixlen 64  scopeid 0x0<global>
        ether 40:16:7e:86:aa:c1  txqueuelen 1000  (Ethernet)
        RX packets 49839  bytes 41203486 (39.2 MiB)
        RX errors 0  dropped 5954  overruns 0  frame 0
        TX packets 12597  bytes 4080417 (3.8 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 144  bytes 12714 (12.4 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 144  bytes 12714 (12.4 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

wlp3s0: flags=4098<BROADCAST,MULTICAST>  mtu 1500
        ether b6:ed:4c:f6:b0:fd  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[hungtx@linux ~]$ 
```
