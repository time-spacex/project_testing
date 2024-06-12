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

![screenshot](https://s89klg.storage.yandex.net/rdisk/f04a5f12068a8b41d3034397fccd35a8a7ea06efa44f27c84d929202dcaba637/66699db0/IoIOxktzTT0sH_9TxoiNPeFf6-zwEC80jQgOGCbDmiHWLXk85X5yifQJTbJy-490GTqYaS9jMa5lL6M1GNgC_A==?uid=30479285&filename=%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%2012-06-2024%20120318.jpg&disposition=inline&hash=&limit=0&content_type=image%2Fjpeg&owner_uid=30479285&fsize=21567&hid=8aa2fe33bbe9b029550892f8fb39d9ff&media_type=image&tknv=v2&etag=02663076b3bcf16d08599f94c31403da&ts=61ab1125ecc00&s=cbf1894e30499e876720567670c8404708bfda933802e0862eb9f0dd06fd38a2&pb=U2FsdGVkX18BiwJKEEwFO8V7x1IslOMmfdmkkoOSIh57MvCSUm6eBkxdCYKCRcaf-OVViSg9eimRtbATNHEeBOVgdall5e4VWN2ZwDK5pmI)

![screenshot](https://disk.yandex.ru/i/RqMQH8nyUyFP7w)
