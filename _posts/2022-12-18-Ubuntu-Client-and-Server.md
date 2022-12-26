---
layout: post
title: "Ubuntu 22.04 on both client PC and remote server"
categories:
 - IT tips
 - NIS
tags: [Ubuntu 22.04, Linux, Remote access]
---

Due to promoting research, I decided to build a home Ubuntu environment accessing the NIS remote GPU server, which runs on Ubuntu 22.04.

<!--more-->

### Main functions in the Ubuntu local PC:
- Anaconda for python programming
- Dropbox files syncing
- Internet browsing, etc

### Main functions in the Ubuntu remote server:
- ssh connecting
- Python computing
- Remote desktop for Netlogo, etc

## The installation details are as follows.

### Anaconda installed in local PC
It is easy to do. So only the confirmed screenshot is here.  
![Locval anaconda](/assets/images/20221218_1_conda_info.png)

### Now, start to build the JupyterLab server. At first, access it via ssh.  
![ssh to GPU](/assets/images/20221218_2_ssh_GPU_server.png)

### sudo apt upgrade
![sudo apt upgrade](/assets/images/20221218_3_sudo_apt_upgrade.png)

### sudo apt install curl -y
![curl](/assets/images/20221218_4_sudo_apt_install_curl.png)

### Download anaconda install package and sha256sum it to confirm.
![download](/assets/images/20221218_5_download_anacondaPKG.png)  
![sha256sum](/assets/images/20221218_6_sha256sum_anacondaPKG.png)

### Anaconda installation
![inst_7](/assets/images/20221218_7_install_anaconda.png)  
![inst_8](/assets/images/20221218_8_install_anaconda.png)  
![inst_9](/assets/images/20221218_9_install_anaconda.png)  
![inst_10](/assets/images/20221218_10_install_anaconda.png)  
![inst_11](/assets/images/20221218_11_install_anaconda.png)

### Generate JupyterLab server config file
![config](/assets/images/20221218_12_generate_jupyterlab_config.png)

### Modify config file via vim
![vim](/assets/images/20221218_13_vim_config.png)

### Access to the built JupyterLab server and start it via ssh
![start remote JupyterLab server](/assets/images/20221218_14_ssh_to_remote_jupyterlab.png)

### Input the key for the first access
![first access](/assets/images/20221218_15_fist_access.png)

### Successful access
![successful access](/assets/images/20221218_16_success_access.png)

### （Option） tmux installation for terminal connection
![tmux](/assets/images/20221218_17_tmux_inst.png)











