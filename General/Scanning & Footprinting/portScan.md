# Port Scanning

> ping <ip>

**NMAP PORTS:**
```
$ nmap -Pn (ip)

$ nmap -Pn -sCV -0 -v ()

$ nmap -iL ips

$ nmap -iL ips -sV -0

$ nmap -T4 -PA -sC -sV -p 1-10000 0.0.0.0

$ nmap -sV -sC -p 445 0.0.0.0
```

--------------------------------------------------------------------

> Agressive scan: nmap -A

> output normal: -oN test.txt

> excel format: -oX test.xml

--------------------------------------------------------------------