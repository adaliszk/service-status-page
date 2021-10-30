_An open-source status page companion for your services_

# Service Status Page
Whenever you deploy a service, it is always a good practice to monitor it. There are plenty of robust status page 
solutions out there, however, a good deal of them just delivers yet another paid service that you have to manage. 
Many often don't even integrate into existing infrastructure tools like Prometheus or Elasticsearch and try to replace 
otherwise simple and capable stacks.

While some of them are definitely a great option, like [Cachet](https://github.com/CachetHQ/Cachet), this project goal
is to focus on the absolute minimum and ship a flexible, slim solution that integrates into other tools first.

## Features
- integrates with existing tools or works as a standalone
- re-usable web components; customise to your leisure
- pluggable; only run what you actually need


## Roadmap
- [ ]  setup developer environment and project structure
- [ ]  add backend that stores URL pings either in memory or using Prometheus
- [ ]  add Prometheus data-source and metric configuration
- [ ]  setup build and publish pipeline for docker
- [ ]  add frontend that builds and bundles lit components
- [ ]  add `service-status-page` application component
- [ ]  add `ssp-metric-widget` component to show mean ping
- [ ]  add `ssp-graph-widget` component to show over-time health
- [ ]  add `ssp-uptime-widget` component to show liveliness history
- [ ]  add `ssp-ping-source` to fetch data locally without the backend
- [ ]  setup build and publish pipeline for web-components
- [ ]  add Helm chart for standalone mode