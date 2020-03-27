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
2. got to Grafana at `http://<synology ip/hostname>:3000` (initial login ins admin/admin) and add a promethous datasource, add a dashboard.
3. add a graph for the measument labs (mlab) speed test (download & upload)
4. add a gaph for the mlab ping
5. add a graph for the fritzbox speed sync
6. add a graph for the fritzbox connection uptime



#### Endpoints
- Grafana `http://<synology ip/hostname>:3000` (this may take upto 15 seconds to start up.)
- Prometheus `http://<synology ip/hostname>:9090`
- Alertmanager `http://<synology ip/hostname>:9093`
- fritzox_exporter `http://<synology ip/hostname>:9122/metrics`
- mlapb_exporter `http://<synology ip/hostname>:9133/metrics`
<!-- - speedtest_exporter `http://<synology ip/hostname>:9112/metrics`->
<!-- - Node-Exporter `http://<synology ip/hostname>:9100/metrics` -->

