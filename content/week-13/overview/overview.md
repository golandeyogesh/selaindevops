---
title: "Overview"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 10
---

Monitoring provides feedback from production and delivers information about an application’s performance and usage patterns. When performance or other issues arise, relevant data about the issues are sent back to development teams through automated monitoring. Besides helping us track issues that may arise in production we can also use monitoring to automatically scale up or down a specific service depending on it's usage.

Monitoring covers different types of data but the most common are: metrics and logs. With metrics we can see how is the performance of our application and even the machines themselves, and with logs we can see exactly what is going on at the application level by inspecting the application logs.

This week we are going to focus on what happens after we deploy our applications to our environments. We are going to set up a monitoring system that consists on the Prometheus Stack to collect metrics and visualize them and the Elasticsearch Stack to collect logs and visualize them.



![Prom+Elk](/images/prom-elk.png)


