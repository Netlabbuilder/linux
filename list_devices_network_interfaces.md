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
- `ip -br add show`
```
[hungtx@linux ~]$ ip -br add show
lo               UNKNOWN        127.0.0.1/8 ::1/128 
enp2s0f1         UP             192.168.178.59/24 2003:e6:b707:8c00:4216:7eff:fe86:aac1/64 fdd1:1aef:54b9:0:4216:7eff:fe86:aac1/64 fe80::4216:7eff:fe86:aac1/64 
wlp3s0           DOWN 
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
- `nmcli device status`
```
[hungtx@linux ~]$ nmcli device status
DEVICE          TYPE      STATE                   CONNECTION 
enp2s0f1        ethernet  connected               enp2s0f1   
lo              loopback  connected (externally)  lo         
wlp3s0          wifi      unavailable             --         
p2p-dev-wlp3s0  wifi-p2p  unavailable             --         
[hungtx@linux ~]$ 
```
- `nmcli device show enp2s0f1`
```
[hungtx@linux ~]$ nmcli device show enp2s0f1
GENERAL.DEVICE:                         enp2s0f1
GENERAL.TYPE:                           ethernet
GENERAL.HWADDR:                         40:16:7E:86:AA:C1
GENERAL.MTU:                            1500
GENERAL.STATE:                          100 (connected)
GENERAL.CONNECTION:                     enp2s0f1
GENERAL.CON-PATH:                       /org/freedesktop/NetworkManager/ActiveConnection/3
WIRED-PROPERTIES.CARRIER:               on
IP4.ADDRESS[1]:                         192.168.178.59/24
IP4.GATEWAY:                            192.168.178.1
IP4.ROUTE[1]:                           dst = 192.168.178.0/24, nh = 0.0.0.0, mt = 100
IP4.ROUTE[2]:                           dst = 0.0.0.0/0, nh = 192.168.178.1, mt = 100
IP4.DNS[1]:                             192.168.178.1
IP4.DOMAIN[1]:                          fritz.box
IP6.ADDRESS[1]:                         2003:e6:b707:8c00:4216:7eff:fe86:aac1/64
IP6.ADDRESS[2]:                         fdd1:1aef:54b9:0:4216:7eff:fe86:aac1/64
IP6.ADDRESS[3]:                         fe80::4216:7eff:fe86:aac1/64
IP6.GATEWAY:                            fe80::1eed:6fff:fe53:302c
IP6.ROUTE[1]:                           dst = fe80::/64, nh = ::, mt = 1024
IP6.ROUTE[2]:                           dst = fdd1:1aef:54b9::/64, nh = ::, mt = 100
IP6.ROUTE[3]:                           dst = 2003:e6:b707:8c00::/64, nh = ::, mt = 100
IP6.ROUTE[4]:                           dst = fdd1:1aef:54b9::/64, nh = fe80::1eed:6fff:fe53:302c, mt = 105
IP6.ROUTE[5]:                           dst = 2003:e6:b707:8c00::/56, nh = fe80::1eed:6fff:fe53:302c, mt = 100
IP6.ROUTE[6]:                           dst = ::/0, nh = fe80::1eed:6fff:fe53:302c, mt = 100
IP6.DNS[1]:                             fdd1:1aef:54b9:0:1eed:6fff:fe53:302c
IP6.DNS[2]:                             2003:e6:b707:8c00:1eed:6fff:fe53:302c
[hungtx@linux ~]$
```
- `nmcli connection show `
```
[hungtx@linux ~]$ nmcli connection show 
NAME        UUID                                  TYPE      DEVICE   
enp2s0f1    f355eadc-f77b-427d-877d-86ba78b0bb33  ethernet  enp2s0f1 
lo          9f2d20a6-6dd0-4ec1-8791-119f9bae3753  loopback  lo      
```
