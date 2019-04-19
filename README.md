# VMWARE ESXi Grafana charts via Prometheus

This Grafana chart is designed for standalone VMWare ESXi.
Test ESXi software levels: 5.0,5.1 and 6.5.


Example charts:

![](_images/79ad77c5.png)

![](_images/75f5db95.png)


Requires to compile GO exported available at:
https://github.com/devinotelecom/prometheus-vmware-exporter

Separate exporter must be run for each of the monitored ESXi hosts. In examples there are two which run on the same machine as Prometheus:
esxexporter01 - scrapes metrics from esx01.mydomain.com and present locally on port 9611
esxexporter02 - scrapes metrics from esx02.mydomain.com and present locally on port 9612

Host names must be resolvable - attached an example /etc/hosts file.

prometheus.yml - Prometheus example configuration to scrape metrics from both exporters.

Grafana dashboard definition: "VMWare ESXi Dashboard.json"
