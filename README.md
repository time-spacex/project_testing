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

![screenshot]([https://s89klg.storage.yandex.net/rdisk/f04a5f12068a8b41d3034397fccd35a8a7ea06efa44f27c84d929202dcaba637/66699db0/IoIOxktzTT0sH_9TxoiNPeFf6-zwEC80jQgOGCbDmiHWLXk85X5yifQJTbJy-490GTqYaS9jMa5lL6M1GNgC_A==?uid=30479285&filename=%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%2012-06-2024%20120318.jpg&disposition=inline&hash=&limit=0&content_type=image%2Fjpeg&owner_uid=30479285&fsize=21567&hid=8aa2fe33bbe9b029550892f8fb39d9ff&media_type=image&tknv=v2&etag=02663076b3bcf16d08599f94c31403da&ts=61ab1125ecc00&s=cbf1894e30499e876720567670c8404708bfda933802e0862eb9f0dd06fd38a2&pb=U2FsdGVkX18BiwJKEEwFO8V7x1IslOMmfdmkkoOSIh57MvCSUm6eBkxdCYKCRcaf-OVViSg9eimRtbATNHEeBOVgdall5e4VWN2ZwDK5pmI](https://s460vlx.storage.yandex.net/rdisk/36fc17d9a872fb64211dd2e65eed9d6872d3b542b4f1a5707e526ffba5511867/6669ec4e/IoIOxktzTT0sH_9TxoiNPY4Q7w1s5D3nD2n2ITKaPDZ58pPkWxfsYSbgFftuG4kdoeaxCENytih6yv--kV7m3g==?uid=30479285&filename=%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%2012-06-2024%20174250.jpg&disposition=inline&hash=&limit=0&content_type=image%2Fjpeg&owner_uid=30479285&fsize=19468&hid=a163d9695175117ece2a400410ccb7c4&media_type=image&tknv=v2&etag=21dd39bd22e2825c3af93754d84801ed&ts=61ab5c1f92f80&s=fd5934f5016541608e6633793bc6ecbf683ac0ad81484a35518cc90f25549116&pb=U2FsdGVkX18B7JVTRKYnqe5pTaMdIqT5NKj8F5RKoI0IqAdDss-2pFKi8lyBw0mNtkXp0R9gS5W0yUA8d6Nxknz5RFVh70fRVlfA3uVq8HM))

![screenshot](https://s526vla.storage.yandex.net/rdisk/fc187fdc5ac1df37b5eaa8daee4fd403f0b124ccf1fb13cdf4fa2f9b8000fa10/66699dfc/IoIOxktzTT0sH_9TxoiNPV1ygLk8N3qDdxW2bkugrvnKJJ5GzjpXiTi_uaouvrZKntunFOiwN2Pi2_uLhN1YbA==?uid=30479285&filename=%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%2012-06-2024%20120414.jpg&disposition=inline&hash=&limit=0&content_type=image%2Fjpeg&owner_uid=30479285&fsize=28446&hid=c6761ada1e9fc3e552373e46d67f0dec&media_type=image&tknv=v2&etag=08364bbeefd52386cc4d02d4e429c832&ts=61ab116e67700&s=b3f7a7b4742884e02c03150badf97a27c3efd72d3046b53332b96983edd1de78&pb=U2FsdGVkX1_J_Td0zv6s8veWmz8VqulkzwOsjvvovnq8J6wR0DEI3pEBOdOhg5Svf-MazI3HzcmxE98AdzMp3NwwgKTZx5Z7drHh_zsOnwE)
