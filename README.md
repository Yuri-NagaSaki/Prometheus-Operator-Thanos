# Prometheus-Operator-Thanos

[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/Yuri-NagaSaki/Prometheus-Operator-Thanos)

> Note that everything is experimental and may change significantly at any time.

This repository is developed based on the [kube-prometheus](https://github.com/prometheus-operator/kube-prometheus) project. It extends the original project by adding NodeExporter and Kubernetes Pod Prometheus rules. 
Additionally, it introduces two Thanos architecture modes, thanos-sidecar and thanos-receive, to enhance Prometheus high availability.

The content of this project is written in [Yuri-NagaSaki](https://github.com/Yuri-NagaSaki). This project could both be described as a package as well as a library.

Components included in this package:

* The [Prometheus Operator](https://github.com/prometheus-operator/prometheus-operator)
* Highly available [Prometheus](https://prometheus.io/)
* Highly available [Alertmanager](https://github.com/prometheus/alertmanager)
* [Prometheus node-exporter](https://github.com/prometheus/node_exporter)
* [Prometheus blackbox-exporter](https://github.com/prometheus/blackbox_exporter)
* [Prometheus Adapter for Kubernetes Metrics APIs](https://github.com/kubernetes-sigs/prometheus-adapter)
* [kube-state-metrics](https://github.com/kubernetes/kube-state-metrics)
* [Grafana](https://grafana.com/)
* [Thanos](https://github.com/thanos-io/thanos)
* [PrometheusAlert](https://github.com/feiyu563/PrometheusAlert)


This stack is meant for cluster monitoring, so it is pre-configured to collect metrics from all Kubernetes components. In addition to that, it delivers a default set of dashboards and alerting rules. The newly added Thanos provides high availability for Prometheus, ensuring robust and reliable monitoring. In multi-Kubernetes cluster setups, Prometheus writes monitoring data to the Thanos store gateway, while the Thanos query gateway allows reading and querying data from the Thanos store gateway. This integration provides Prometheus with scalability and resilience in terms of persistent storage and cross-cluster querying.

## Thanos Basic Components Introduction

- **Query**: Implements the Prometheus API, providing a consistent query interface with Prometheus.
- **Sidecar**: Connects to Prometheus, provides a query interface, and can also report data.
- **Store Gateway**: Accesses metric data stored in object storage.
- **Compact**: Compresses samples and cleans up data in object storage.
- **Receive**: Receives data from Prometheus Remote Write.
- **Ruler**: Configures and manages alerting rules.
