# Mapping a Network

> With acces to the network we use sniffing —> passive reconnaissance, watch network traffic

ARP —> Addres Resolution Protocol (Resolve Ip to MAC)
    - 10.10.1.5 is at 00:0c:29:af:ea:d2

ICMP —> Internet Control Message Protocol
    - Traceroute
    - Ping
        - Type 8 - echo request

**MAP HOSTS:**
```
$ sudo nmap -sn (ip)
```
> -sn means not to port scan

```
$ sudo nmap -sn (ip)/(subnet)
```

```
$ netdiscover -i eth0 -r ip/subnet
```

```
$ sudo arp-scan -I eth0 -g 10.10.10.10/24

> whireshark —> endpoints
```

```
$ fping -I eth0 -g 10.10.10.10/24 -a 2>/dev/null (-a —> active)
```