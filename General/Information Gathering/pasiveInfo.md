
Obtain Ip adress:
```
$ host web.org
```
--------------------------------------------------------------------

> [!IMPORTANT]
> Search for Names, e-mails adresses...


/robots.txt —> important, first search

    disallow/allow 

    normally disallow /wp-admin/


/sitemap_index.xml —> important

```
$ whatweb web.org
```

Copy web —> HTTrack (Website Copier)

> who.is

```
$ whois web.org
```

> https://sitereport.netcraft.com/

```
$ dnsrecon web.org
```

```
$ wafw00f web.org

$ wafw00f web.org -a (for checking all types)
```

Use sublist3r for passive enumeration of directories etc.
```
$ sublist3r -d web.org -e google,yahoo

$ sublist3r -d web.org
```

Old versions of websites: waybackmachine

Google Dorks:

site:ine.com 

inurl:admin

site:*.ine.com 

intitle:index of

cache:ine.com

inurl:auth_user_file.txt

inurl_passwd.txt

> https://www.exploit-db.com/google-hacking-database

Email,users,ips,hosts harvesting:
```
$ theHarvester -d web.org -b google,linkedin
```