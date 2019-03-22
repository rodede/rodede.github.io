---
layout: post
title: Voxxed days Bucharest 2019
description: Voxxed days Buchares 20-22 March 2019
categories: programming
---
[Official page](https://romania.voxxeddays.com/bucharest/2019-03-20/)


* Do not remove this line (it will not be displayed)  
{:toc}

## 1st Day-Workshop

[MicroProfile](https://romania.voxxeddays.com/2019/02/24/hands-on-cloud-native-java-with-microprofile-kubernetes-and-istio/)  with Emily Jiang and Graham Charters  
[Initial project](https://github.com/OpenLiberty/tutorial-microprofile.git)  
[Class project](https://github.com/gcharters/workshop-cloud-native-java/blob/master/README.md)  

### Module 4: Microservice Deployment and Update  

#### Deploying microservices to Kubernetes  

Deploy microservices in Open Liberty Docker containers to Kubernetes and manage them with the Kubernetes CLI, kubectl.

[Guide](https://openliberty.io/guides/kubernetes-intro.html)

#### Configuring microservices running in Kubernetes

Explore how to externalize configuration using MicroProfile Config and configure your microservices using Kubernetes ConfigMaps and Secrets.

[Guide](https://openliberty.io/guides/kubernetes-microprofile-config.html)


#### Checking the health of microservices on Kubernetes

Learn how to check the health of microservices on Kubernetes by setting up readiness probes to inspect MicroProfile Health Check endpoints.

[Guide](https://openliberty.io/guides/kubernetes-microprofile-health.html)


#### Managing microservice traffic using Istio

Explore how to manage microservice traffic using Istio.

[Guide](https://openliberty.io/guides/istio-intro.html)

## 2nd Day Presentations

- Devops-1 team with **Cecilia**  
- **Venkat** paradigms 
- [MongoDB+Spring](https://github.com/dangeabunea/VoxxedDaysBucharest2019)  
- [Kafka Stream](https://github.com/Stream-Processing-with-Kafka-Streams/workshop)  

```  
#!/bin/sh

docker network create kafka

docker run -d --net=kafka --name=zookeeper -e ZOOKEEPER_CLIENT_PORT=2181 confluentinc/cp-zookeeper:5.0.0
docker run -d --net=kafka --name=kafka -p 9092:9092 -e KAFKA_ZOOKEEPER_CONNECT=zookeeper:2181 -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://localhost:9092 -e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1 confluentinc/cp-kafka:5.0.0

docker ps  
```  

- Serverless with **Arun**

## 3rd Day Presentations

- Drinking Kafka/RabbitMQ coffee with MHeckler  
- Fn servless Java DeLaBaSSe  
- Kubernetes lab with Laurentiu [Source](https://github.com/lspil/voxxeddays2019)
[PDF samples ][1]
[PPT presentation ][2]

[1]:{{ site.url }}/assets/files/samples.pdf
[2]:{{ site.url }}/assets/files/presentation.pptx  


