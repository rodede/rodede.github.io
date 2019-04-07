---
layout: post
title: Spring devtools usage
description: Spring devtools - How to make it work
categories: spring
---

Normally, the Spring boot devtools should add the below features:
- Automatic application restart when code changes  
- Automatic browser refresh when browser-destined resources (such as templates, JavaScript, stylesheets, and so on) change  
- Automatic disable of template caches  
- Built in H2 Console if the H2 database is in use  
~~~ bash
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-devtools</artifactId>
	<scope>runtime</scope>
</dependency>
~~~      

To make it work while editing in IntelliJ, there are couple of things to be also changed:
1. Add LiveReload extension in your browser. Apparently, this cannot be installed anymore with the package provided from the [site](http://livereload.com/extensions/), but obly through Apple Appstore  
After install, there should be a new icon on the browser
![Liveramp](/assets/images/liveramp.jpg)

2. In your IntelliJ IDEA go to: file->settings->build,execution,deployment. Fill ->compiler->build project automatically checkbox
![IntelliJ](/assets/images/intellij-build-auto.jpg)

3. In your intellij IDEA: SHIFT+Cmd+A ->registry-> compiler.automake.allow.when.app.running

From [here](https://stackoverflow.com/questions/33869606/intellij-15-springboot-devtools-livereload-not-working)
