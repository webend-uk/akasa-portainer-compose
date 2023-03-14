# akasa-portainer-compose

## networks
https://www.adminsub.net/ipv4-subnet-calculator/172.17.1.0/28
| Docker Network     |      CIDR        | HOST IP      | FIRST IP      | LAST IP       |
|--------------------|------------------|--------------|---------------|---------------|
| infra-net          | 172.17.1.0/28    | 172.17.1.1   | 172.17.1.2    | 172.17.1.14   |
| metrics-net        | 172.17.1.16/28   | 172.17.1.17  | 172.17.1.18   | 172.17.1.30   |
| backup-net         | 172.17.1.32/28   | 172.17.1.33  | 172.17.1.34   | 172.17.1.46   |
| media-net          | 172.17.1.48/28   | 172.17.1.49  | 172.17.1.50   | 172.17.1.62   |
| scrappers-net      | 172.17.1.64/28   | 172.17.1.65  | 172.17.1.66   | 172.17.1.78   |
| monitoring-net     | 172.17.1.80/28   | 172.17.1.81  | 172.17.1.82   | 172.17.1.94   |


## ports
| Stack       | Container          | Port        | Description           |
|-------------|--------------------|-------------|-----------------------|
| metrics     | node-exporter      |  9101:9100  | node-exporter metrics |
| metrics     | cadvisor-exporter  |  9102:8080  | node-exporter metrics |
| metrics     | deluge-exporter    |  9103:9354  | node-exporter metrics |
| media       | gluetun            |  8081:8112  | Deluge UI             |
| media       | gluetun            |  8082:8989  | Sonarr UI             |
| media       | gluetun            |  8083:7878  | Radarr UI             |
| media       | gluetun            |  8084:80    | lxde UI               |
| media       | gluetun            | 58846:58846 | Deluge Remote         |
| media       | gluetun            |  5900:5900  | lxde VNC              |
| media       | gluetun            |  6789:6789  | nzbget UI             |
| media       | gluetun            |  8085:8080  | sabnzbd UI            |
| scrappers   | tautulli           |  8090:8181  | Tautulli UI           |
| monitoring  | prometheus         |  9090:9090  | Prometheus UI         |
| monitoring  | grafana            |  3000:3000  | Grafana UI            |
