# HELP
1. The ip address of each container change every time i reboot my server. How to stop that ?

### Basic server config before starting
* OS : Ubuntu Server 24.04.2 LTS
* HDD : 2to
* CasaOS : curl -fsSL https://get.casaos.io | sudo bash
* Tailscale : curl -fsSL https://tailscale.com/install.sh | sh

### Set-up folders
```
sudo mkdir /data
sudo chown -R $USER /data
sudo chgrp -R $USER /data
sudo mkdir /config
sudo chown -R $USER /config
sudo chgrp -R $USER /config
sudo mkdir /docker
sudo chown -R $USER /docker
sudo chgrp -R $USER /docker
sudo mkdir /docker/homelab
cd /data
mkdir -p downloads/qbittorrent/{completed,incomplete,torrents} && mkdir -p downloads/nzbget/{completed,intermediate,nzb,queue,tmp} && mkdir -p /data/{movies,show}
```
### Getting the docker compose
```
cd /docker/homelab
wget https://raw.githubusercontent.com/OwNuT/HomeLab/refs/heads/main/compose.yaml
docker compose up -d
```
