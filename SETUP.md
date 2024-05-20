# Setup

## QNAP

### Create share

![Setup Shared Folder](/setup/QNAP_set_share_permissions.png)

### Create folder structure

Create folders following this structure:

- docker-volumes
  - db
  - grafana-data
  - mosquitto-conf
  - mosquitto-data
 
![Folder Structure](/setup/QNAP_folder_structure.png)

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

Create docker-compose.yml file (from the template in this repo) in /mnt/teslamate/ then follow the instructions:

[Teslamate docker install docs](https://docs.teslamate.org/docs/installation/docker)

The encryption key can be generated [here](https://acte.ltd/utils/randomkeygen).

## Teslamate UI

Start Teslamate at http://<Raspberry Pi IP>:4000
Set the access token and refresh token (Use 3rd party app like Auth for Tesla).
In the Teslamate UI, in the settings, set Dashboards URL to http://<Raspberry Pi IP>:3000
