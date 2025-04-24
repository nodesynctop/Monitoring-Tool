# Monitoring-Tool
An easy setup to instantly get a powerful monitoring tool for all your validation nodes.
## Install Docker
```
command -v docker >/dev/null || (curl -fsSL https://get.docker.com | sudo sh)
```
## Install Tool

### Clone the repo
```
cd $HOME && git clone https://github.com/nodesynctop/Monitoring-Tool.git
```
## Configuration files
```
cd Monitoring-Tool && sudo nano prometheus/prometheus.yml
```
**your_ip:26660** # Replace with the IP address and port of your Tendermint node

## Start 
```
sudo docker compose up -d
```
