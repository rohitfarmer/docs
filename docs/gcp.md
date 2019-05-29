---
layout: default
title: GCP
nav_order: 7
description: "Google cloud platform."
---

# Google Cloud Platform (GCP)
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---
# To ssh to Google Compute Engine Instance

First generate a ssh key pair on your local machine; use the username on the instance else it will create the user
same as user on the local machine.

`ssh-keygen -t rsa -f ~/.ssh/name -C username`

`chmod 400 ~/.ssh/name`

Then login to your compute engine dashboard and click on metadata tab on the left. Go to ssh keys section and click edit,
create a new entry and past the name.pub contents there. 

`ssh -i ~/.ssh/name username@external ip address`  
`sftp -i ~/.ssh/name username@external ip addresss`  