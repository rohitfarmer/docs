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

`conda env create --name=h5n1day100 -file=environment.yaml`

`conda env update --name=h5n1day100 --file=environment.yaml`

**To activate conda environment** `conda activate h5n1day100`

**To deactivate conda environment** `conda deactivate`