---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

## Introduction

We already configured a CI/CD process that package the application into container images and deploy them on our infrastructure. This week instead of using docker on top of VMs we are going to use Kubernetes, a very popular tool that will help us manage containers in a reliable way accross multiple servers.

## Project Overview

- First of all we will create a Kubernetes Cluster in Microsoft's Azure Kubernetes Service (AKS) for the project infrastructure.

![AKS](/images/aks-1.png)

- Once the cluster is created we are going to run our NodeWeightTracker application on top of AKS. This means that we need to write all the configuration files that are needed for running our application in a Kubernetes Cluster.

![AKS](/images/kubernetes-resources.png)

- Finally we will, update or CI/CD process to deploy our already dockerized application into the Kubernetes cluster.

![AKS](/images/k8s-cicd.png)

## Goals

- Provision an AKS cluster
- Install the Nginx ingress controller
- Deploy the NodeWeightTracker application on AKS meeting the following requirements:
  - The NodeWeightTracker application must be accessible from the internet
  - The NodeWeightTracker application must be exposed to the internet on port 80
  - The NodeWeightTracker must have at least 3 instances to ensure high availability
  - Use configmaps/secrets to store your application configurations
  - You must expose your application using the ingress controller
  
## Considerations

- You can deploy the AKS cluster from the Azure Portal with minimal changes on the default configurations (Infrastructure as Code is not required)
- Note that with our type of azure subscription it's not possible to deploy a cluster across multiple availability zones

## Expected Result

- An AKS cluster with the NodeWeightTracker is deployed following the requirements listed above.
- Your application lifecycle is automated with a CI/CD process

## Bonus

1. Helm: Package your kubernetes manifests using helm and use it to deploy your application in your CI/CD pipeline.
2. PostgreSQL on Kubernetes: Instead of using the PostgreSQL managed service of Azure, deploy the database into the AKS cluster (ensure the database is accessible only within the cluster)
3. Terraform: Manage your Azure resources using Infrastructure as Code

## Delivery

- Send a link to the repos containing your source code
- Fill out the following form: [Delivery Form](https://forms.gle/i7hLhmAPw3mBfkfAA)
- Any additional files that have not been uploaded to git for security reasons must be submitted by discord
- Grant contributor access to selaindiabootcamp@outlook.com at your subscription level
- Grant selaindiabootcamp@outlook.com access to your application (okta)
- Grant selaindiabootcamp@outlook.com Contributor access to your Azure DevOps Project
