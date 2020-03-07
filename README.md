## Dependencies
- [Synology Docker](https://www.synology.com/en-global/dsm/packages/Docker) package already installed.
- SSH access to synology.
- Administrator user access.


### Install
```bash
curl -fsSL https://raw.githubusercontent.com/wlbr/synology-prometheus/master/setup | sudo sh
```

#### Endpoints
- Grafana `http://<synology ip/hostname>:3000` (this may take upto 15 seconds to start up.)
- Prometheus `http://<synology ip/hostname>:9090`
- Alertmanager `http://<synology ip/hostname>:9093`
- speedtest_exporter `http://<synology ip/hostname>:9112/metrics`
<!-- - Node-Exporter `http://<synology ip/hostname>:9100/metrics` -->

