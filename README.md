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


## What is loki?

- Loki is a horizontally-scalable, highly-available, multi-tenant log aggregation system inspired by Prometheus.
- Compared to other log aggregation systems, Loki:
   - does not do full text indexing on logs. By storing compressed, unstructured logs and only indexing metadata, Loki is     simpler to operate and cheaper to run.
  - indexes and groups log streams using the same labels you’re already using with Prometheus, enabling you to seamlessly switch between metrics and logs using the same labels that you’re already using with Prometheus.
  - is an especially good fit for storing Kubernetes Pod logs. Metadata such as Pod labels is automatically scraped and indexed.
  - has native support in Grafana (needs Grafana v6.0).

### A Loki-based logging stack consists of 3 components:

- promtail is the agent, responsible for gathering logs and sending them to Loki.
- loki is the main server, responsible for storing logs and processing queries.
- Grafana for querying and displaying the logs.
