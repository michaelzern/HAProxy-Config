# HAProxy-Config
Layer 7 Load Balancer config file for JAMF Pro

located in /etc/haproxy/haproxy.cfg

# Check stats with HATOP
Install guide https://www.serverlab.ca/tutorials/linux/network-services/monitoring-haproxy-using-hatop/

```
hatop -s /var/run/haproxy.sock
```

```
NAME    name of the proxy and his services\
W       configured weight of the service
STATUS  service status (UP/DOWN/NOLB/MAINT/MAINT(via)...)
CHECK   status of last health check (see status reference below)
ACT     server is active (server), number of active servers (backend)
BCK     server is backup (server), number of backup servers (backend)
QCUR    current queued requests
QMAX    max queued requests
SCUR    current sessions
SMAX    max sessions # max concurrent sessions
SLIM    sessions limit
STOT    total sessions # total number of sessions since haproxy was restarted
```

# Securing haproxy or nginx via HTTP Headers

https://blog.devcloud.hosting/securing-haproxy-and-nginx-via-http-headers-54020d460283
