# Setup

## QNAP

### Create share

![Setup Shared Folder](/setup/QNAP_set_share_permissions.png)

## Raspberry Pi

### Install Docker

Add mount to /etc/fstab

```
192.168.1.99:/teslamate	/mnt/teslamate/	nfs	rw	0	0
```

### Install Docker

[Install Docker Engine on Raspberry Pi OS (32-bit)](https://docs.docker.com/engine/install/raspberry-pi-os/)

```
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done
```
