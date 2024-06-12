## Overview

This simple project is docker based tool, and give you access to 2 dashboards operating system and database metrics. Prometeus container collects metrics from node and mysql exporter containers and transmits them to grafana. Then nginx allows you access to http://metrics.local to watch graphical representation of this metrics.

## System requirements

+ Linux Debian 12 or newer
+ Docker 26.1.4 or newer

## How to install

At first check your system have docker
```
sudo docker info
```
Second - clone git repository
```
git clone git@github.com:time-spacex/project_testing.git
```
After the repository has been downloaded, run add_metrics_local.sh - this script will add an entry to your hosts file so that the metrics.local is available.
```
cd project_testing
sudo ./add_metrics_local.sh
```
Last thing - run docker compose file for deploying containers on a local machine.
```
sudo docker compose up --build
```
