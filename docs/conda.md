---
layout: default
title: Conda
nav_order: 3
description: "Conda commands."
---

# Conda
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Create and Update Conda Environments

**Example yaml file.**
```
 name: h5n1day100
 channels:
   - bioconda
   - conda-forge
 dependencies:
   - r=3.5.1
   - snakemake=5.4.5
   - r-tidyverse=1.2.1
   - r-feather=0.3.2
   - r-venndiagram=1.6.20
   - r-tmod=0.40
   - r-biocmanager=1.30
   - bioconductor-biobase=2.42
   - r-logging=0.9_107
```

`conda env create --file=environment.yaml`

`conda env update --file=environment.yaml`

**To activate conda environment** `conda activate h5n1day100`

**To deactivate conda environment** `conda deactivate`

**To remove conda environment** `conda env remove --name=<env name>`

# To Completely remove Anaconda from your Computer

To remove the configs:  
```
conda install anaconda-clean
anaconda-clean --yes
```

Once the configs are removed you can delete the anaconda install folder, which is usually under your home dir:   
`rm -rf ~/anaconda3`

Also, the `anaconda-clean --yes` command creates a backup in your home directory of the format `~/.anaconda_backup/<timestamp>`. Make sure to delete that one also.

Now if you want to clean all, you will also have to delete the two last lines added to your .bash_profile. They look like:
```
# added by Anaconda3 5.2.0 installer
export PATH="/Users/ody/anaconda3/bin:$PATH"
```
