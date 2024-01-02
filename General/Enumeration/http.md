# **HTTP**

## **Web Server 80**

--------------------------------------------------------------------

### Nmap Scripts

```
> windows:

$ nmap 0.0.0.0 -sV -p 80 —script http-enum

$ nmap 0.0.0.0 -sV -p 80 —script http-headers

$ nmap 0.0.0.0 -sV -p 80 —script http-methods —script-args hhtp-methods.url-pah=/webdav/

$ nmap 0.0.0.0 -sV -p 80 —script http-webdav-scan —script-args hhtp-methods.url-pah=/webdav/


> linux:

$ nmap 0.0.0.0 -sV -p 80 —script banner
```

--------------------------------------------------------------------

### Useful Commands

```
$ whatweb 0.0.0.0

$ http 0.0.0.0

$ dirb http://0.0.0.0
$ dirb http://0.0.0.0 /usr/share/metasploit_framework/data/wordlists/directory.txt

$ browsh —startup-url http://0.0.0.0

$ curl 0.0.0.0 | more
> curl what is recieved in robots.txt

$ wget “http://0.0.0.0/index”

$ browsh —startup-url http://0.0.0.0

$ lynx http://0.0.0.0
```
