# Prometheus-Operator-Thanos

[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/Yuri-NagaSaki/Prometheus-Operator-Thanos)

> Note that everything is experimental and may change significantly at any time.

This repository is developed based on the [kube-prometheus](https://github.com/prometheus-operator/kube-prometheus) project. It extends the original model by adding NodeExporter and Kubernetes Pod Prometheus rules. 
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
