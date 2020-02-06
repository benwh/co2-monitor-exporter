# CO2 Monitor Exporter

Prometheus exporter for CO2 concentration and indoor temperature from TFA Dostmann AirCO2NTROL Coach in Node.JS.

Uses [jaller94's fork][ncm-fork] of [node-co2-monitor][ncm].

[ncm-fork]: https://gitlab.com/jaller94/node-co2-monitor
[ncm]: https://github.com/huhamhire/node-co2-monitor

## Contents

* [Supported Hardware](#supported-hardware)
* [Install](#install)
* [Usage](#usage)
* [Metrics](#metrics)
* [License](#license)

## Supported Hardware

* [TFA Dostmann AirCO2NTROL Coach - Monitor CO2 31.5009](https://www.tfa-dostmann.de/en/produkt/co2-monitor-airco2ntrol-coach-31-5009/)

## Install

Currently this isn't published anywhere, so to install:

```bash
git clone https://github.com/benwh/co2-monitor-exporter
npm install -g .
```

## Usage

```bash
co2-exporter [--port <port> --host <host>]
```

Or starting with PM2 as a service.
```bash
pm2 start `which co2-exporter` [-- --port <port> --host <host>]
```

By default the exporter will accept connections on `127.0.0.1:9091`.

![Grafana](https://huhamhire.github.io/co2-monitor-exporter/images/grafana.png)

## Metrics

  Name                  | Description
------------------------|-------------
air_temperature_celsius | Ambient Temperature (Tamb) in ℃.
air_co2_ppm             | Relative concentration of CO2 (CntR) in ppm.
air_humidity_ratio      | Relative humidity percentage.

## License

MIT
