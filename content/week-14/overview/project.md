---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

## Introduction

We already configured a CI/CD process that package the application into container images and deploy it using the most simple orchestrator which is docker-compose. This week instead of using docker-compose we are going to use Kubernetes, a very popular tool that will help us manage containers in a reliable way accross multiple servers.

## Project Overview

- First of all we will create a Kubernetes Cluster in Microsoft's Azure Kubernetes Service (AKS) for the project infrastructure.

![AKS](/images/aks-1.png)

- Once the cluster is created we are going to run our NodeWeightTracker application on top of AKS. This means that we need to write all the configuration files that are needed for running our application in a Kubernetes Cluster.

## Goals

- Deploy an AKS cluster
- Deploy a PostgreSQL database on AKS
- Deploy the NodeWeightTracker application on AKS meeting the following requirements:
  - The NodeWeightTracker application must be accessible from the internet
  - The NodeWeightTracker application must be exposed to the internet on port 80
  - The NodeWeightTracker must have at least 3 instances to ensure high availability
  - Postgresql must be accessible only within the cluster
  
## Considerations

- You can deploy the AKS cluster from the Azure Portal with minimal changes on the default configurations (Infrastructure as Code is not required)
- Note that with our type of azure subscription it is not possible to deploy a cluster across multiple availability zones
- The PostgreSQL database can be easily deployed by using a Helm chart

## Expected Result

- An AKS cluster with the NodeWeightTracker and Postgresql deployed following the requirements listed above.

## Bonus

- What do we do with a service that tracks weight without a calculator? So besides the NodeWeightTracker application we are going to deploy all the services that compose the Calculator application into our Kubernetes cluster.
- Change the CD of the NodeWeightTracker application to automatically deploy the application into the K8s cluster after a succesful CI run
- Store the sensitive information as a Kubernetes Secret
- Expose the application using the nginx ingress controller

## Delivery

- Send a link to the repos containing your code