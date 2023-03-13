# akasa-portainer-compose

## networks
https://www.adminsub.net/ipv4-subnet-calculator/172.17.1.0/28
| Docker Network     |      CIDR        | HOST IP      | FIRST IP      | LAST IP       |
|--------------------|------------------|--------------|---------------|---------------|
| backup-net         | 172.17.1.0/28    | 172.17.1.1   | 172.17.1.2    | 172.17.1.14   |
| metrics-net        | 172.17.1.16/28   | 172.17.1.17  | 172.17.1.18   | 172.17.1.30   |
| media-net          | 172.17.1.32/28   | 172.17.1.33  | 172.17.1.34   | 172.17.1.46   |
| scrappers-net      | 172.17.1.48/28   | 172.17.1.49  | 172.17.1.50   | 172.17.1.62   |
| monitoring-net     | 172.17.1.64/28   | 172.17.1.65  | 172.17.1.66   | 172.17.1.78   |

## ports
| Stack       | Container          | Port        | Description           |
|-------------|--------------------|-------------|-----------------------|
| metrics     | node-exporter      |  9101:9100  | node-exporter metrics |
| metrics     | cadvisor-exporter  |  9102:8080  | node-exporter metrics |
| metrics     | deluge-exporter    |  9103:9354  | node-exporter metrics |
| monitoring  | prometheus         |  9090:9090  | Prometheus UI         |
| monitoring  | grafana            |  3000:3000  | Grafana UI            |
