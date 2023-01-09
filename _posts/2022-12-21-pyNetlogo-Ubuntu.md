---
layout: post
title: "Multi-agent Reinforcement Learning Environment by Python and Netlogo in Ubuntu"
categories:
 - Python
 - Game theory
 - Reinforcement learning
 - Research PJ
 - IT tips
 
tags: [Multi-agent, Reinforcement Learning, Python, Game theory, Netlogo, Ubuntu]
---

It is done to control Netlogo from python on the Ubuntu system.
Netlogo is a helpful visual tool for multi-agent simulation.
However, it is challenging to analyze further the agent behaviors and action policies.
Python is a better choice to cover Netlogo. Furthermore,
it can easily construct a reinforcement learning mechanism for policy enhancement.
The point is to build an efficient shared environment for these two.  
After many trials, I used Jpype and pyNetlogo in the latest Ubuntu system.

<!--more-->

# How to build pyNetlogo environment in Ubuntu

## Install anaconda 
To download the latest anaconda installation package.  
[https://www.anaconda.com/products/distribution#linux](https://www.anaconda.com/products/distribution#linux){:target="_blank"}

ref: [https://blog.eldernode.com/setup-anaconda-on-ubuntu-22-04/](https://blog.eldernode.com/setup-anaconda-on-ubuntu-22-04/){:target="_blank"}

```
$ cd Downloads
(change downloaded file name to a simple one.)
$ bash Anaconda3.sh 
```

To create a desktop shortcut for Anaconda Navigator  
ref: [https://www.how2shout.com/linux/create-anaconda-navigator-desktop-shortcut-ubuntu-20-04-18-04/](https://www.how2shout.com/linux/create-anaconda-navigator-desktop-shortcut-ubuntu-20-04-18-04/){:target="_blank"}

## Generate pyNetlogo env in anaconda

### Intsall numpy, scipy, pandas

In terminal, ```$ conda activate pyNetlogo```

### Install JPype
Because JPype is not in conda list, confirm it in [the official site](https://jpype.readthedocs.io/en/latest/install.html#binary-install){:target="_blank"}.  
```
$ conda install -c conda-forge jpype1
```
note: JPype can not work in Python 3.9, but fine in 3.8.

### Install pyNetlogo
ref: [https://pynetlogo.readthedocs.io/en/latest/install.html](https://pynetlogo.readthedocs.io/en/latest/install.html){:target="_blank"}

note: pyNetLogo requires NumPy, SciPy, Pandas and JPype packages.

```
$ pip install pynetlogo
Conda installs matplotlib and seaborn
```
note: do it later.change in core.py of pyNetlogo

### Install Java JDK
ref: [here](https://self-development.info/ubuntu-22-04-lts%E3%81%B8%E3%81%AEjava%EF%BC%88openjdk%EF%BC%89%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB/){:target="_blank"}

```
$ sudo apt update  
$ sudo apt install -y openjdk-17-jdk
```

Choose JDK17 to install.  
The Java installation costs time.  
After installation, check the Java version: $ java --version 

End processes while error.
```$ gnome-system-monitor```

## Summary

Key steps of installation:  
```
$ conda install -c conda-forge jpype1
$ pip install pynetlogo
$ sudo apt install -y openjdk-17-jdk
```

Notes:  
(1) JPype does not work on Python 3.9, but fine on 3.8.  
(2) Skip JDK19 trial while JDK17 works. 

![pyNetlogo methodological structure](/assets/images/20221222_pyNetlogo_methodological_structure.png)

![pyNetlogo implememtation structure](/assets/images/20221222_pyNetlogo_implememtation_structure.png)

![pyNetlogo demo](/assets/images/20221222_pyNetlogo_demo.png)




