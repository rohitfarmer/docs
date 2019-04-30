---
layout: default
title: Test, Build, and Deploy Singularity using Travis CI.
nav_order: 2
parent: HPC
description: "Test, Build, and Deploy Singularity using Travis CI."
---

# Test, Build, and Deploy Singularity using Travis CI.
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Theory

It is possible to test, build, deploy Singularity containers using [Travis CI](https://travis-ci.org) website. However, the current documentation is only to test the build success of a Singularity definition file. The idea is to spare our local computers from Singularity juicing up all the power during the build. It can also be useful if you don't have admin rights on your computer which is a must to build a container, and also if you are not on a Linux machine. However, having a Linux machine is not an absolute requirement to build a Singularity container.

Travis CI (continuous integration) works by pulling a GitHub repository and executing a build pipeline as laid out in the .travis.yml and associated files (shell scripts maybe) that are included in the GitHub repo. For each GitHub repo, Travis initiates a virtual environment of the OS and distribution selected, installing necessary components required for the build and then carrying out the actual build of the scripts/software required. If the entire run of Travis CI exits with a zero return, then it's said to be a successful build. 

In case of Singularity build a Singularity.def file along with a .travis.yml and any associated shell scripts can be left in a GitHub repo that is linked to Travis CI. Every time there is an update in the Singularity.def file Travis CI will automatically build the container, and if the deployment options are configured correctly, then the container will also be shipped to the desired location. For our use, Google Drive seems to be the right destination among the list of the cloud services supported by Sregistry (the software that deploys Singularity container).

Currently, I have only tested it with my personal [GitHub repo](https://github.com/rohitfarmer/singularity-defs) for Singularity defs. Once I have perfected the protocol I will transfer a set of example scripts to CHI's GitHub. 

## Useful Links  
* [Building Singularity Containers on TravisCI](https://vsoch.github.io/2018/singularity-ci/)
* [Singularity Global Clients](https://singularityhub.github.io/sregistry-cli/clients)
