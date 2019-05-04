---
layout: post
title: Druid development
description: Starting druid 
categories: programming
---

Links
=====  

[Community](http://druid.io/community/) general guideliness  

[Github](https://github.com/apache/incubator-druid/blob/master/CONTRIBUTING.md) - project and issues list

[Druid CLA](http://druid.io/community/cla.html)

[DEV overview](http://druid.io/docs/latest/development/overview.html)


Dev
===
[How to contribute](https://github.com/apache/incubator-druid/blob/master/CONTRIBUTING.md)  
[Build](https://github.com/apache/incubator-druid/blob/master/docs/content/development/build.md)  
[IntelliJ setup](https://github.com/apache/incubator-druid/blob/master/INTELLIJ_SETUP.md)  
[MySQL setup](https://github.com/apache/incubator-druid/blob/master/docs/content/development/extensions-core/mysql.md)  


[Issues for me](https://github.com/apache/incubator-druid/issues?q=is%3Aopen+is%3Aissue+label%3A%22Difficulty+-+Easy%22)

Issue
===
Peon error java.net.BindException: Address already in use
---
See also [hint](https://groups.google.com/d/msg/druid-user/UJo0OUBxxF8/AuNKrvrIAgAJ)  

> ForkingTaskRunner which was not freeing the internal map of used ports. This was causing the middleManagers to slowly use up all of the ports from druid.indexer.runner.startPort 

```
2019-04-12T18:48:19,618 ERROR [main] org.apache.druid.server.initialization.jetty.JettyServerModule - Jetty lifecycle event failed [class org.eclipse.jetty.server.Server]
java.net.BindException: Address already in use
	at sun.nio.ch.Net.bind0(Native Method) ~[?:1.8.0_201]
	at sun.nio.ch.Net.bind(Net.java:433) ~[?:1.8.0_201]
	at sun.nio.ch.Net.bind(Net.java:425) ~[?:1.8.0_201]
	at sun.nio.ch.ServerSocketChannelImpl.bind(ServerSocketChannelImpl.java:223) ~[?:1.8.0_201]
	at sun.nio.ch.ServerSocketAdaptor.bind(ServerSocketAdaptor.java:74) ~[?:1.8.0_201]
	at org.eclipse.jetty.server.ServerConnector.openAcceptChannel(ServerConnector.java:340) ~[jetty-server-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.server.ServerConnector.open(ServerConnector.java:308) ~[jetty-server-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.server.AbstractNetworkConnector.doStart(AbstractNetworkConnector.java:80) ~[jetty-server-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.server.ServerConnector.doStart(ServerConnector.java:244) ~[jetty-server-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:68) [jetty-util-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.server.Server.doStart(Server.java:398) ~[jetty-server-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:68) [jetty-util-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.apache.druid.server.initialization.jetty.JettyServerModule$2.start(JettyServerModule.java:383) [druid-server-0.13.0-incubating.jar:0.13.0-incubating]
	at org.apache.druid.java.util.common.lifecycle.Lifecycle.start(Lifecycle.java:311) [java-util-0.13.0-incubating.jar:0.13.0-incubating]
	at org.apache.druid.guice.LifecycleModule$2.start(LifecycleModule.java:134) [druid-api-0.13.0-incubating.jar:0.13.0-incubating]
	at org.apache.druid.cli.GuiceRunnable.initLifecycle(GuiceRunnable.java:107) [druid-services-0.13.0-incubating.jar:0.13.0-incubating]
	at org.apache.druid.cli.CliPeon.run(CliPeon.java:348) [druid-services-0.13.0-incubating.jar:0.13.0-incubating]
	at org.apache.druid.cli.Main.main(Main.java:118) [druid-services-0.13.0-incubating.jar:0.13.0-incubating]
2019-04-12T18:48:19,630 ERROR [main] org.apache.druid.cli.CliPeon - Error when starting up.  Failing.
java.net.BindException: Address already in use
	at sun.nio.ch.Net.bind0(Native Method) ~[?:1.8.0_201]
	at sun.nio.ch.Net.bind(Net.java:433) ~[?:1.8.0_201]
	at sun.nio.ch.Net.bind(Net.java:425) ~[?:1.8.0_201]
	at sun.nio.ch.ServerSocketChannelImpl.bind(ServerSocketChannelImpl.java:223) ~[?:1.8.0_201]
	at sun.nio.ch.ServerSocketAdaptor.bind(ServerSocketAdaptor.java:74) ~[?:1.8.0_201]
	at org.eclipse.jetty.server.ServerConnector.openAcceptChannel(ServerConnector.java:340) ~[jetty-server-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.server.ServerConnector.open(ServerConnector.java:308) ~[jetty-server-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.server.AbstractNetworkConnector.doStart(AbstractNetworkConnector.java:80) ~[jetty-server-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.server.ServerConnector.doStart(ServerConnector.java:244) ~[jetty-server-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:68) ~[jetty-util-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.server.Server.doStart(Server.java:398) ~[jetty-server-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:68) ~[jetty-util-9.4.10.v20180503.jar:9.4.10.v20180503]
	at org.apache.druid.server.initialization.jetty.JettyServerModule$2.start(JettyServerModule.java:383) ~[druid-server-0.13.0-incubating.jar:0.13.0-incubating]
	at org.apache.druid.java.util.common.lifecycle.Lifecycle.start(Lifecycle.java:311) ~[java-util-0.13.0-incubating.jar:0.13.0-incubating]
	at org.apache.druid.guice.LifecycleModule$2.start(LifecycleModule.java:134) ~[druid-api-0.13.0-incubating.jar:0.13.0-incubating]
	at org.apache.druid.cli.GuiceRunnable.initLifecycle(GuiceRunnable.java:107) [druid-services-0.13.0-incubating.jar:0.13.0-incubating]
	at org.apache.druid.cli.CliPeon.run(CliPeon.java:348) [druid-services-0.13.0-incubating.jar:0.13.0-incubating]
	at org.apache.druid.cli.Main.main(Main.java:118) [druid-services-0.13.0-incubating.jar:0.13.0-incubating]
Heap
 garbage-first heap   total 983040K, used 144519K [0x00000006c0000000, 0x00000006c0101e00, 0x00000007c0000000)
  region size 1024K, 133 young (136192K), 34 survivors (34816K)
 Metaspace       used 55453K, capacity 56442K, committed 56960K, reserved 1097728K
  class space    used 7957K, capacity 8243K, committed 8320K, reserved 1048576K

```