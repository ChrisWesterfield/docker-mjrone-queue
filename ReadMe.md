PHP 7.2.0 RC3
Slim

**default user**: www-data

includes the following extensions:

- pdo
- pdo-mysql
- pcntl
- redis
- opcache
- xdebug
- blackfire

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
