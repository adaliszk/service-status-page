_Status page companion for your services utilising Prometheus_

# Service Status Page

Whenever you deploy a service, it is always a good practice to monitor it. There are plenty of robust status page
solutions out there, however, a good deal of them just delivers yet another paid service that you have to manage, and
they seem not to integrate into existing tools all that often such as Prometheus.

This simple tool is aim to be a lightweight companion to display one or many services health or R.E.D. information
using Prometheus. For most sophisticated dashboards you should use tools like Grafana, but if your goal is to expose
a simple and fast status page then this tool might be what you want.

## Features

- integrates with Prometheus for displaying metrics and alerts
- configurable for one or many services to be used as a sidecar or as a standalone status page
- provides a push or pull mechanics for displaying news

# How to use it?

Add the image to your stack or deploy it independently using any of the available image distributions:

- adaliszk/service-status-page
- ghcr.io/adaliszk/service-status-page
- quay.io/adaliszk/service-status-page

You can then follow the instructions on the available page on :8080, or preset values using a config file:
```yaml
prometheus: prometheus-master.monitoring.cluster.local:9090
history: 24h
metrics:
  - name: AVG Response Time
    metric: avg_over_time(gateway_response_seconds[1m])
    position: 1,0
    size: 11,3
  - name: P95 Latency
    metric: gateway_latency
    position: 0,0
    size: 1,1
  - name: 
filters:
  my-label: value
news: rss.app/twitter/handle
maintenance_match:
  title: MAINTENANCE
  begin: "starts at (\w+),"
  duration: "lasts for (\d+) hours"
```

# Contributions

The project is under development right now therefore there are many opportunities to contribute, and it is welcomed!
Please read the [CONTRIBUTING](CONTRIBUTING.md) guide to help you get started.