# Setup

## QNAP

### Create share

![Setup Shared Folder](/setup/QNAP_set_share_permissions.png)

### Create folder structure



## Raspberry Pi

### Install Docker

Add mount to /etc/fstab

```
<NAS IP>:/teslamate	/mnt/teslamate/	nfs	rw	0	0
```

### Install Docker

[Install Docker Engine on Raspberry Pi OS (32-bit)](https://docs.docker.com/engine/install/raspberry-pi-os/)

```
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done
```

Install using the apt repository

### Create docker-compose.yml file

Create docker-compose.yml file (from this repo) then follow the instructions:

[Teslamate docker install docs](https://docs.teslamate.org/docs/installation/docker)

