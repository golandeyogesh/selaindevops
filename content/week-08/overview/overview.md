---
title: "Overview"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 10
---

This week we will learn about a technology that revolutionized the world by changing the way we handle our applications.

Up until now we automated the process of provisioning the infrastructure for our WeightTracker application and we configured a whole CI/CD process to manage it. However, when we packaged the application to create our build artifact we used a zip file which contains only the application and it's dependencies. By using containers we will be able to package the application together with it's runtime so the deployment process and the operations after it will we much more easier.

![containers](/images/docker-containers.png)