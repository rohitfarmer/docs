---
layout: default
title: Docker
nav_order: 4
parent: HPC
description: "Docker"
---

# Docker
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---
# Install Docker

`sudo apt-get install docker.io`

## Add Current User to Docker Group to Solve sudo Problem

`sudo usermod -a -G docker $USER`

# Checking Docker Status
```
docker ps # to check for current running instances

docker ps -a # to check for all the docker runs ever ran

docker ps --filter status=running # check for the dockers that are running

docker kill container # to kill a running container

docker rm container # remove a specific stopped container

docker rm $(docker ps -a -q) # to remove all the stopped containers
```

# Execute Docker
```
docker exec container command
```
