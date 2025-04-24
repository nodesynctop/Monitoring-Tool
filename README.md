# Monitoring-Tool
An easy setup to instantly get a powerful monitoring tool for all your validation nodes.
## I. Install Docker
```
command -v docker >/dev/null || (curl -fsSL https://get.docker.com | sudo sh)
```
## II. Install Tool

#### 1. Clone the repo
```
cd $HOME && git clone https://github.com/nodesynctop/Monitoring-Tool.git
```
#### 2. Configuration files
```
cd Monitoring-Tool && sudo nano prometheus/prometheus.yml
```
`your_ip:port` # Replace with the IP address and port of your Tendermint node

#### 3. Start 
```
sudo docker compose up -d
```

#### 4. Open in browser http://<your_server_ip>:3000

default user: `admin`

default password: `admin`

You can change the password after your first login.

Use `http://prometheus:9090` as the Prometheus server URL for your setup. This is the default URL to access the Prometheus web interface, which is running within Docker.
#### 5. How to Add Multiple Tendermint Nodes to Prometheus (Skip if You Have Only One Node)
Open the Prometheus Configuration File
```
cd $HOME/Monitoring-Tool && sudo nano prometheus/prometheus.yml
```
Add Multiple Nodes
```
scrape_configs:
  - job_name: 'tendermint'
    static_configs:
      - targets:
          - 'your_ip1:port'  # Replace with the IP address and port of the first Tendermint node
          - 'your_ip2:port'  # Replace with the IP address and port of the second Tendermint node
          - 'your_ip3:port'  # Replace with the IP address and port of the third Tendermint node
```
Save and Restart Prometheus
```
docker compose restart prometheus
```
#### 6.  Stop the Containers 
```
docker stop grafana prometheus node_exporter
```
#### 7. Remove the Containers
```
docker rm grafana prometheus node_exporter
```
