# Running Jupyter on a SLURM Compute Node (via VSCode)

This guide describes how to run a Jupyter notebook on a SLURM-managed compute node while using VSCode to interact with it, avoiding the login node.

---

## 🧠 Overview

- Start an interactive job using `salloc`
- Launch a Jupyter Lab server on the compute node
- Forward the port from your local machine
- Connect to the Jupyter server from a browser or VSCode

---

## 🚀 Step-by-Step Guide

```bash
# 1. Connect via VSCode Remote-SSH to:
# login@hostname.domain

# 2. Check which nodes are available:
sinfo -N -l

# 3. Start an interactive SLURM job on a specific node:
salloc --ntasks=1 --cpus-per-task=20 --mem=128G --time=48:00:00 --nodelist=b33

# OR, let SLURM pick a node:
salloc --ntasks=1 --cpus-per-task=4 --mem=8G --time=4:00:00 --partition=your_partition
```


### 3. On the remote VSCode  

* Click the kernel selector (top right)
* Choose “Existing Jupyter Server”
* Paste the token URL:  
http://localhost:8890/lab?token=xxxxxx
