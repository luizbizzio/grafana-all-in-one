# Grafana for All
Grafana Dashboard using metrics from Prometheus, Infinity, Tuya Exporter, Promdapter, Windows Exporter, Solis Inverter Exporter, Node Exporter, Open Meteo API

![image](https://github.com/luizbizzio/Grafana-for-all/assets/73234672/ff767a86-b51c-4cbd-a68c-649ed24c0572)

## Setup

### Grafana
* [Download page](https://grafana.com/grafana/download) (Used 9.5.2)
* [Docs](https://grafana.com/docs/grafana/latest/setup-grafana/installation/)

### Prometheus
* [Download page](https://prometheus.io/download/) (Used 2.44.0)
* [Docs](https://prometheus.io/docs/prometheus/latest/getting_started/)

### GO
* [Download page](https://go.dev/dl/) (Used 1.20.4)\
Note: _Only to build exporters, then can you uninstall_

### HWiNFO
* [Download page](https://www.hwinfo.com/download/) \
**You will need to enable:** \
"Show Sensors on Startup" \ 
"Minimize Main Window on Startup" \
"Minimize Sensors on Startup" \ 
"Minimize Sensors Instead of Closing" \ 
"Auto Start"

### Tuya Exporter
[here is excellent guide](https://github.com/codetheweb/tuyapi/blob/master/docs/SETUP.md) by @codetheweb
```
git clone https://github.com/rkosegi/tuya-smartplug-exporter
cd tuya-smartplug-exporter
```
add your device info in ./config.yaml
```
go build
```
Tutorial to get device info: https://github.com/iRayanKhan/homebridge-tuya/wiki/Get-Local-Keys-for-your-devices \
localhost:9999/metrics

### PromDapter
* Repository: https://github.com/kallex/PromDapter \
Default Port: 10445 

### Windows Exporter
### Solis Inverter JSON API
### Node Exporter



## Docs
You can find useful information about several components and answers to frequently asked questions in each repository. If you think that there is something missing, you are invited to submit a pull request to the grafana-for-all repository.

## Repositories

* Prometheus:
https://github.com/prometheus/prometheus

* Inifinity:
https://github.com/yesoreyeram/grafana-infinity-datasource

* Tuya Exporter: (Smart Plug)
https://github.com/rkosegi/tuya-smartplug-exporter
  
* PromDapter: (HWiNFO)
https://github.com/kallex/PromDapter
  
* Windows Exporter: (Windows Info)
https://github.com/prometheus-community/windows_exporter
  
* Solis inverter JSON API: (Photovoltaic system with Solis inverter)
https://github.com/fss/solis-inverter
  
* Node Exporter: (Used on PiKVM - IP-KVM on Raspberry Pi)
https://github.com/prometheus/node_exporter
  
* Open Meteo JSON API: (Weather)
https://github.com/open-meteo/open-meteo
