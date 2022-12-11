---
layout: post
title: "Fixed Lenovo P920 Nivdia driver installtion in Ubuntu 22.04"
categories:
 - IT Tips
tags: [Mouse scroll direction, Natual]
---
The recent Ubuntu 22.04 upgrade auto installation caused display problem in our GPU server, the Lenovo P920 workstation. 
After surveying, I found the best solution and solved the problem by a few command lines.

<!--more-->


```
sudo apt-get purge nvidia *
sudo apt-get update
sudo apt-get autoremove
```
