# SrvID-Beacon
Pingable http endpoint for monitoring server uptime



## Setup Instructions
Install python3:
```console
# apt update
# apt install python3
```

Clone git repository:
```console
# cd /opt
# git clone https://git.tjdev.de/tjdev/srvid-beacon
# cd srvid-beacon
```

Create srvid-beacon user:
```console
# useradd -s /bin/bash srvid-beacon
```

Set permissions on daemon file:
```console
# chown :srvid-beacon srvid-beacond
# chmod 654 srvid-beacond
```

Install as systemd service:
```console
# ln -s /opt/srvid-beacon/srvid-beacon.service /etc/systemd/system/srvid-beacon.service
# systemctl daemon-reload
# systemctl enable srvid-beacon.service
# systemctl start srvid-beacon.service
# systemctl status srvid-beacon.service
```
