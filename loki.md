

## What is loki?

- Loki is a horizontally-scalable, highly-available, multi-tenant log aggregation system inspired by Prometheus.
- Compared to other log aggregation systems, Loki:
   - does not do full text indexing on logs. By storing compressed, unstructured logs and only indexing metadata, Loki is     simpler to operate and cheaper to run.
  - indexes and groups log streams using the same labels you’re already using with Prometheus, enabling you to seamlessly switch between metrics and logs using the same labels that you’re already using with Prometheus.
  - is an especially good fit for storing Kubernetes Pod logs. Metadata such as Pod labels is automatically scraped and indexed.
  - has native support in Grafana (needs Grafana v6.0).

### A Loki-based logging stack consists of 3 components:

- ``` promtail ``` is the agent, responsible for gathering logs and sending them to Loki.
- ``` loki ``` is the main server, responsible for storing logs and processing queries.
- ``` Grafana ``` for querying and displaying the logs.
``` Promtail``` can be deployed as a ``` sidecar ``` or a ``` daemonSet ``` . ``` DaemonSet``` the best solution for a single-tenant model but In a multi-tenant environment, ``` sidecar ``` enables teams to aggregate logs for specific pods and deployments.

### Loki Architecture: [see more](https://github.com/grafana/loki/blob/v1.3.0/docs/architecture.md#components)

### Loki Api: https://github.com/grafana/loki/blob/master/docs/logql.md

