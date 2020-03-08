## Dependencies
- [Synology Docker](https://www.synology.com/en-global/dsm/packages/Docker) package already installed.
- SSH access to synology.
- Administrator user access.


### Install
```bash
curl -fsSL https://raw.githubusercontent.com/wlbr/synology-prometheus/master/setup | sudo sh
```
#### To monitor your broadband connection automatically:
1. go to Prometheus at `http://<synology ip/hostname>:9090/graph` and add a speedtest metric to the graph (download, upload or ping)
2. got to Grafana at `http://<synology ip/hostname>:3000` (initial login ins admin/admin) and add a promethous datasource, add a dahboard and a graph. Copy your Prometheus query from the Prometheus graph console view to your new Grafana panel 


#### Endpoints
- Grafana `http://<synology ip/hostname>:3000` (this may take upto 15 seconds to start up.)
- Prometheus `http://<synology ip/hostname>:9090`
- Alertmanager `http://<synology ip/hostname>:9093`
- speedtest_exporter `http://<synology ip/hostname>:9112/metrics`
<!-- - Node-Exporter `http://<synology ip/hostname>:9100/metrics` -->

