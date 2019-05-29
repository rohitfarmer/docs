---
layout: default
title: Running Jupyter on HPC.
nav_order: 10
parent: HPC
description: "Setting up Jupyter Notebook Over Tunneling on HPC."
---

# Running Jupyter on HPC
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Setting up Jupyter Notebook Over Tunneling on HPC.

Below is an example protocol to run Jupyter notebook in an interactive node on a high-performance computer (HPCs). Most of the HPCs have their specialised way of interacting with them. Therefore, you may have to tweak this protocol as per your need. I would be happy to discuss and troubleshoot with you; contact me at [contact@rohitfarmer.dev](mailto:contact@rohitfarmer.dev). Any suggestions to augment this protocol with more advanced features are welcomed.

1. SSH to the HPC.    
2. Claim an interactive node (follow the standard procedure for your HPC, in my case it is `qrsh`).   
3. Note the interactive node name.  
4. Run Jupyter on the claimed interactive node by `jupyter notebook --no-browser --ip='0.0.0.0'` or create an alias in your bashrc for a shortcut. For example `alias jup='jupyter notebook --no-browser --ip='0.0.0.0''`.  
5. On your computer start another SSH session with tunnelling using the interactive node name as noted above `ssh user@host -L8888:nodeName:8888 -N`. *The prompt probably won't return and you may also not see any message in your terminal, but as long as there is no error message, it's probably running fine.*  
6. To avoid re-writing the code in step 5 every time you tunnel you can use the shell script below.  

I named it `jupssh`.  
```
#!/bin/sh

# Check if the arugment is passed.
if [[ $# -eq 0 ]];
then
    echo 'Usage: jupssh <node name>'
    exit 1
fi

ssh user@host -L8888:$1:8888 -N
```

* Copy the URL that the Jupyter daemon has generated in step 4 and paste it in the browser on your computer. URL should look something similar to `http://(nodeName or 127.0.0.1):8888/?token=3f7c3a8949b3fa1961c63653873fea075a93a29bffe373b5`. Choose either nodeName or 127.0.0.1 in the URL.