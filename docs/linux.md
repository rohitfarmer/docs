---
layout: default
title: Linux
nav_order: 12
description: "Linux"
---

# Linux
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---
# User related
`sudo -u nobody bash` Change the user to a desired name with a desired shell.

# Cron Jobs Log  
`grep CRON /var/log/syslog`

# Monitoring Processes (ps command)
More information at (https://www.tecmint.com/ps-command-examples-for-linux-process-monitoring/)  

`ps -eo user,pid,ppid,cmd,%mem,%cpu --sort=-%mem | head` # Top running processes by highest memory usage.  
`ps -eo user,pid,ppid,cmd,%mem,%cpu --sort=-%cpu | head` # Top running processes by highest cpu usage.  
`kill -9 2583 2584` # Kill a process using its PID.   

# System Update

## Apt
*To update and install packages.*  
`sudo apt-get update`  
`sudo apt-get upgrade`  
`sudo apt-get install`  
`sudo apt-get install vsftpd=2.3.5-3ubuntu1` # Install specific version of the package.  
`sudo apt-get remove vsftpd` # Remove package without removing configuration.  
`sudo apt-get purge vsftpd` # Completely remove package along with its configuration.  
`sudo apt-get remove --purge vsftpd` # Can combine both remove and purge.  
`sudo apt-get clean` # Delete downloaded .deb files.  
`sudo apt-get autoclean` # Delete all .deb files.  
`sudo apt-get check` # Check for broken dependencies.  

## Apt Cache
*To query apt package list.*  
`apt-cache pkgnames` # List all available packages.  
`apt-cache search vsftpd` # Search for a particular package.  
`apt-cache pkgnames vsftpd` # List all the packages starting with a particular name.  
`apt-cache show netcat` # Check package information.  
`apt-cache showpkg vsftpd` # Check dependencies of a particular package.  

## Install Using DPKG
`sudo dpkg -i package_with_unsatisfied_dependencies.deb`  
`sudo apt-get -f install`  

## Unattended Auto Upgrade
`sudo apt-get install unattended-upgrades`  
`sudo dpkg-reconfigure unattended-upgrades`  
https://help.ubuntu.com/lts/serverguide/automatic-updates.html  
