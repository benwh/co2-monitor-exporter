# CO2 Monitor Exporter

Prometheus exporter for CO2 concentration and indoor temperature from TFA Dostmann AirCO2NTROL Mini in Node.JS.

Based on [node-co2-monitor](https://github.com/huhamhire/node-co2-monitor).


## Contents

* [Supported Hardware](#supported-hardware)
* [Install](#install)
* [Usage](#usage)
* [Metrics](#metrics)
* [License](#license)


## Supported Hardware

* [TFA Dostmann AirCO2NTROL Mini - Monitor CO2 31.5006](https://www.amazon.de/dp/B00TH3OW4Q)


## Install

```bash
npm install co2-monitor-exporter -g
```


## Usage
```bash
co2-monitor [--port <port>]
```

Or starting with PM2 as a service.
```bash
pm2 start `which co2-monitor` [-- --port <port>]
```


## Metrics

  Name  | Description
--------|-------------
air_temp| Ambient Temperature (Tamb) in ℃.
air_co2 | Relative Concentration of CO2 (CntR) in ppm.


## License

MIT