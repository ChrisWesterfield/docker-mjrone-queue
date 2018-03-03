PHP 7.0.27 Queue Server

**default user**: www-data

includes the following extensions:

- pdo
- pdo-mysql
- pdo-pgsql
- pcntl
- redis
- opcache
- xdebug
- blackfire
- pdo_pgsql
- xhprof/tideways
- gd
- ftp
- fileinfo
- imap
- json
- mbstring
- ldap
- phar
- tidy
- sockets
- xmlrpc
- xsl
- mongodb

also includes the following apt installed packages:

1. supervisor
2. teseract (for OCR)
4. graphviz

#NOTES:
This Container musst be launched under the private IP Iddress 
172.42.X.X to be able to connect to a munin host

example config for cron

```
[program:cron]
command = cron -f -L 15
autostart=true
autorestart=true
```
