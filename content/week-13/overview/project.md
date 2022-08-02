---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

## Introduction
Up until now we wrote CI/CD pipelines for the NodeWeightTracker application. Once it gets deployed to the environments we want to be able to monitor all of our services so we need to collect metrics and logs. To be able to collect them and visualize them we are going to set up a Monitoring system. During this week we will deploy together both the Prometheus and the Elasticsearch stacks into our Kubernetes cluster to understand how we can use them to improve our observability.

## Project Overview
Two workshops will be held this week:
- **Prometheus Stack:** In this workshop you will learn how to monitor your Kubernetes cluster infrastructure using the Prometheus Operator.
- **Elasticsearch Stack (ELK):** In this workshop you will learn how to use the Elasticsearch operator to deploy your logging system in Kubernetes.

## Goals
- Complete the Prometheus Workshop:
  - https://github.com/sela-rhinops/bootcamp-monitoring
- Complete the Elasticsearch Workshop:
  - https://github.com/sela-rhinops/bootcamp-logging

## Considerations
- Knowing monitoring tools is essential for any DevOps engineer. During this week we will study the most common Stacks but there are other similar tools that are used for the same purposes (Splunk, Datadog, etc)
- In addition, each cloud provider offer their own solutions:
  - AWS: CloudWatch
  - GCP: Cloud Monitoring
  - Azure: Azure Monitor

## Expected Result
- A monitoring system based on the Prometheus Stack is configured in your cluster
- A logging system based on the ELK Stack is configured in your cluster

## Bonus
- Redirect your WeightTracker application logs to store them into elasticsearch
- Redirect your Ingress Controller logs to store them into elasticsearch in it's own index

## Delivery
- Send a screenshot of the dashboards (Grafana/Kibana)
