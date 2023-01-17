---
layout: post
title: "Solve memory problem of Netlogo big model running"
categories:
 - IT tips
tags: [Netlogo]
---

Mac OS X: The file for NetLogo will be located at:  
```/Applications/NetLogo 6.3.0/NetLogo 6.3.0.app/Contents/app/NetLogo 6.3.0.cfg```

Change ```-Xmx1024m``` to  ```-Xmx4096m``` in ```[JavaOptions]```.

<!--more-->

> Your model is too large to run in the amount of memory available to NetLogo!
For more information consult the "How big can my model be?" section of the FAQ in the user manual.  
Warning: you may see strange results if you continue running the current model without restarting NetLogo.

Ref: [Solution in the offficial site FAQ](http://ccl.northwestern.edu/netlogo/docs/faq.html#how-big-can-my-model-be-how-many-turtles-patches-procedures-buttons-and-so-on-can-my-model-contain){:target="_blank"}
