# Monitoring-Tool
An easy setup to instantly get a powerful monitoring tool for all your validation nodes.
## Install Docker
```
if ! command -v docker &> /dev/null; then
  echo "Installing Docker..."
  curl -fsSL https://get.docker.com -o get-docker.sh && sudo sh get-docker.sh
else
  echo "Docker is already installed: $(docker --version)"
fi
```
