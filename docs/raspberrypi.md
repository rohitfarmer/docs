---
layout: default
title: Raspberry Pi
nav_order: 18
description: "Raspberry Pi"
---

# Raspberry Pi/Raspbian
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Enable SSH
[https://www.raspberrypi.org/documentation/remote-access/ssh/](https://www.raspberrypi.org/documentation/remote-access/ssh/)

```
sudo systemctl enable ssh
sudo systemctl start ssh
```

# Apache and PhP
[https://www.raspberrypi.org/documentation/remote-access/web-server/apache.md](https://www.raspberrypi.org/documentation/remote-access/web-server/apache.md)

```
sudo apt-get install apache2 -y

sudo apt-get install php libapache2-mod-php -y
```

# Miniconda3
```
wget http://repo.continuum.io/miniconda/Miniconda3-latest-Linux-armv7l.sh
chmod a+x Miniconda3-latest-Linux-arm7l.sh
./Miniconda3-latest-Linux-arm7l.sh
```

