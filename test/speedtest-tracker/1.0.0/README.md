# Introduction

This program runs a speedtest check every hour and graphs the results. The back-end is written in [Laravel](https://laravel.com/) and the front-end uses [React](https://reactjs.org/). It uses the [Ookla's speedtest cli](https://www.speedtest.net/apps/cli) package to get the data and uses [Chart.js](https://www.chartjs.org/) to plot the results.

A demo can be found [here](https://speedtest.henrywhitaker.com)

**Disclaimer:**<br>
**You will need to accept Ookla's EULA and privacy agreements in order to use this container.**<br>
**This chart is not maintained by the upstream project**

## Source Code

* <https://github.com/henrywhitaker3/Speedtest-Tracker>

![speedtest](https://user-images.githubusercontent.com/36062479/78822484-a82b8300-79ca-11ea-8525-fdeae496a0bd.gif)

## Requirements

Kubernetes: `>=1.16.0-0`

## Dependencies

| Repository | Name | Version |
|------------|------|---------|
| https://library-charts.truecharts.org | common | 10.2.0 |

## Installing the Chart

To install this App on TrueNAS SCALE check TrueCharts [Quick-Start Guide](https://truecharts.org/manual/Quick-Start%20Guides/02-Installing-an-App/).

## Manual setup required after deployment of app

This chart uses the GeoIP City database. This needs to be added into the chart after deployment.
Connect into the shell of the chart and install GeoIP2 city db into /config/geoip2db/GeoLite2-City.mmdb from [MaxMind](https://dev.maxmind.com/geoip/updating-databases?lang=en#directly-downloading-databases). You will need to extract the specific file GeoLite2-City.mmdb from the tar.gz.

## Upgrading, Rolling Back and Uninstalling the Chart

To upgrade, rollback or delete this App from TrueNAS SCALE check our [Quick-Start Guide](https://truecharts.org/manual/Quick-Start%20Guides/04-Upgrade-rollback-delete-an-App/).

## Support

- Please check TrueCharts [quick-start guides](https://truecharts.org/manual/Quick-Start%20Guides/01-Adding-TrueCharts/) first.

---
All Rights Reserved - Mr_Dan
