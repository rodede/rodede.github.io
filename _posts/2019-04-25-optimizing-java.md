---
layout: post
title: Optimizing Java
description: Optimizing Java by Ben Evans
categories: java
---

Key aspects
=== 
![JVM subsystems](/assets/images/jvm_subsystem.png)  
- Interpreter : Java Language Specifications + JVM specifications  
- JIT compiler (hotspot) : profile guide optimization (not AOT)   
- Classloading : pinchpoint for Java security model  
- Garbage Collection  

![CPU anatomy](/assets/images/cpu_anatomy.png)  
- Cache L1,L2,L3
- North bridge !

![Unix memory model](/assets/images/unix_memory_model.png)  

JVM Objects at runtime
=====  
Oops: _mark and _klass words  
![Oops](/assets/images/oops_mark_klass.png)  
