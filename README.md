# Monitoring-Tool
An easy setup to instantly get a powerful monitoring tool for all your validation nodes.
## 1. Install Docker
```
command -v docker >/dev/null || (curl -fsSL https://get.docker.com | sudo sh)
```
## 2. Install Tool

 1. Clone the repo
```
cd $HOME && git clone https://github.com/nodesynctop/Monitoring-Tool.git
```
2. Configuration files
```
cd Monitoring-Tool && sudo nano prometheus/prometheus.yml
```
`your_ip:26660` # Replace with the IP address and port of your Tendermint node

3. Start 
```
sudo docker compose up -d
```

4. Open in browser http://<your_server_ip>:3000

default user: `admin`

default password: `admin`

You can change the password after your first login.

Use `http://prometheus:9090` as the Prometheus server URL for your setup. This is the default URL to access the Prometheus web interface, which is running within Docker.
