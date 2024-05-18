# Setup

## Raspberry Pi

### Install Docker

[Install Docker Engine on Raspberry Pi OS (32-bit)](https://docs.docker.com/engine/install/raspberry-pi-os/)

```
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done
```
