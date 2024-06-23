# Home Lab Documentation

## Introduction

This section provides an overview of the documentation, the purpose of my home lab, and the goals I aim to achieve.

## Table of Contents

- [Home Lab Documentation](#home-lab-documentation)
  - [Introduction](#introduction)
  - [Table of Contents](#table-of-contents)
  - [Markdown Cheat Sheet](#markdown-cheat-sheet)
  - [Install Portainer CE](#install-portainer-ce)
    - [Portainer Server Deployment](#portainer-server-deployment)
    - [Deployment](#deployment)
  - [Install Docker](#install-docker)
  - [Hardware Notes](#hardware-notes)

<!-- --- -->

## Markdown Cheat Sheet

Looking for a quick reference guide for Markdown syntax? Check out this cheat sheet to help you format your text, add links, insert images, and more. It's a handy resource to have on hand while working with Markdown.

![Markdown Cheat Sheet](images/Markdown_Cheat_Sheet.png)

## Install Portainer CE

### Portainer Server Deployment

* Create Proxmox LXC
* `nano /etc/ssh/sshd_config`
  + PermitRootLogin yes
* VScode SSH

- [Install Docker](#install-docker)

### Deployment

  + [Portainer Documentation](https://docs.portainer.io/start/install-ce/server/docker/linux)
  +  `docker volume create portainer_data`
  +  `docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest`

## Install Docker

  + `apt-get update`
  + `apt-get upgrade -y`
  + `apt install docker.io -y`
  + `systemctl enable docker`
  + `systemctl start docker`
  + `systemctl status docker`
  + `docker -v`

## Hardware Notes

 + Hardware:
   + ASUS Chromebox 3

     + [Spec sheet](https://www.asus.com/us/site/assets/commercial/datasheet/Chromebox_3_Datasheets_Updated.pdf)
     + [SSD](https://www.disctech.com/Western-Digital-SDAPTUW-512G-1012-512GB-NVMe-Solid-State-Drive)
     + [Intel® Dual Band Wireless-AC 7265 ](https://www.amazon.com/Intel-Wireless-AC-802-11ac-Wi-Fi-Bluetooth/dp/B00STV5UKW)
     + USB 3.1 Gen 1 supports speeds of up to 5Gbit/s 
