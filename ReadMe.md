PHP 7.1.8

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
3. Monit
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

Munin Config

```
[program:munin]
command=/usr/bin/sudo /usr/sbin/munin-node --config /etc/munin/munin-node.conf
autostart=true
autorestart=false
priority=5
stdout_events_enabled=true
stderr_events_enabled=true
stdout_logfile=/dev/stdout
stdout_logfile_maxbytes=0
stderr_logfile=/dev/stderr
stderr_logfile_maxbytes=0
```