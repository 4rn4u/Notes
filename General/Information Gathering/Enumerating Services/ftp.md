# **FTP**

## **File Transfer Protocol 21**


--------------------------------------------------------------------

### Some Nmap Scans

```
$ nmap 0.0.0.0 -p -sV -0

$ nmap 0.0.0.0 -p 21 -sV -0
```

--------------------------------------------------------------------

### Nmap Scripts

```
$ nmap 0.0.0.0 —script ftp-brute —script-args userdb=/root/users -p 21

$ nmap 0.0.0.0 —script ftp-anon

$ ls -la /usr/share/nmap/scripts/ | grep ftp-*
```

--------------------------------------------------------------------

### BRUTEFORCE

```
$ hydra -L /usr/share/metasploit-framework/data/wordlists/common_users.txt -P /usr/share/metasploit/data/wordlists/unix_passwords ftp
```

--------------------------------------------------------------------

### Trying anonymous login

```
$ ftp 0.0.0.0
> anonymous and “” (enter)
```

--------------------------------------------------------------------

```
> **ProFTP metasploit module** for analysing ftp
> search proftp
```

--------------------------------------------------------------------