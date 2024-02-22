# Grafana_Loki_Promtail
Grafana Installation


echo "deb [signed-by=/usr/share/keyrings/grafana.key]
https://apt.grafana.com beta main" | sudo tee -a /etc/apt/sources.list.d/grafana.list

# Update the list of available packages
sudo apt-get update
# Install the latest OSS release:
sudo apt-get install grafana
#To start Grafana Server
sudo /bin/systemctl status grafana-server

Download Promtail Config

wget https://raw.githubusercontent.com/grafana/loki/v2.8.0/clients/cmd/promtail
/promtail-docker-config.yaml -0 promtail-config.yaml


Run Promtail Docker container

docker run -d --name promtail -v $ (pwd):/mnt/config -v /var/log:/var/10g
--link loki grafana/promtail:2.8.0
--config. file=/mnt/config/promtail-config.yaml

Install Loki and Promtail using Docker

Download Loki Config

wget https://raw.githubusercontent.com/grafana/loki/v2.8.0/cmd/loki/loki-local-
config. yaml -0 loki-config. yaml

Run Loki Docker container

docker run -d --name loki -v $(pwd):/mnt/config -p 3100:3100 grafana/loki:2.8,0 --config. file=/mnt/config/loki-config-yaml

Download Promtail Config

wget
https://raw.githubusercontent.com/grafana/loki/v2.8.0/clients/cmd/promtail
/promtail-docker-config.yaml -0 promtail-config.yaml

