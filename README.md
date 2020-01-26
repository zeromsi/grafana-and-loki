# grafana-and-loki

## Wy grafana over kibana

- Kibana supports only elasticsearch as data source but using grafana we can source data from various sources like, 
```
AWS CloudWatch
Azure Monitor
Elasticsearch
Google Stackdriver
Graphite
InfluxDB
Loki
Microsoft SQL Server (MSSQL)
Mixed
MySQL
OpenTSDB
PostgreSQL
Prometheus
Testdata
```
- Grafana is designed for analyzing and visualizing metrics such as system CPU, memory, disk and I/O utilization. Grafana does not allow full-text data querying.

- Kibana runs on top of Elasticsearch and is used primarily for analyzing log messages.

- Grafana doesn't support text based querying and visualization, kibana does.

- Kibana by default doesn't support alerting service (Integration wil slack and others) but Grafana does.
- By default kibana dashboard is public. If we want RBAC, we need to purchage ``` Elastic Stack security features ```. On the other hand grafana provides RBAC by default.


## Intall Grafana and map prometheus

[Link](https://devopscube.com/setup-grafana-kubernetes/)
