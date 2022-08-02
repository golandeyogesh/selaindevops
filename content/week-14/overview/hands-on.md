---
title: "Hands-On"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 60
---

- **Sela Labs** A collection of labs created by Sela
  - Objective: In this repository you will find a collection of labs and demos covering all the topics regarding Kubernetes.
  - Steps:
    1) Go to the repository URL
    2) Enter the lab's files and follow the instructions
- Link: https://gitlab.com/sela-kubernetes-workshop

- **Exercise 01:** Start containers using Kubectl
  - Objective: In this scenario, you'll learn how to use Kubectl to create and launch Deployments, Replication Controllers and expose them via Services without writing yaml definitions. This allows you to quickly launch containers onto the cluster.
  - Steps:
    1) Launch Cluster
    2) Kubectl Run
    3) Kubectl Expose
    4) Kubectl Run and Expose
    5) Scale Containers
- Link: https://www.katacoda.com/courses/kubernetes/kubectl-run-containers

- **Exercise 02:** Deploy Containers Using YAML
  - Objective: In this scenario, you'll learn how to use Kubectl to create and launch Deployments, Replication Controllers and expose them via Services by writing yaml definitions.
  - Steps:
    1) Create Deployment
    2) Create Service
    3) Scale Deployment
- Link: https://www.katacoda.com/courses/kubernetes/creating-kubernetes-yaml-definitions

- **Exercise 03:** Deploy Guestbook example on Kubernetes
  - Objective: This scenario explains how to launch a simple, multi-tier web application using Kubernetes and Docker. The Guestbook example application stores notes from guests in Redis via JavaScript API calls. Redis contains a master (for storage), and a replicated set of redis 'slaves'.
  - Steps:
    1) Start Kubernetes
    2) Redis Master Controller
    3) Redis Master Service
    4) Replication Slave Pods
    5) Redis Slave Service
    6) Frontend Replicated Pods
    7) Guestbook Frontend Service
    8) Access Guestbook Frontend
- Link: https://www.katacoda.com/courses/kubernetes/guestbook

- **Exercise 04:** Networking Introduction
  - Objective: In this scenario you will learn about Kubernetes advanced networking capabilities that allow Pods and Services to communicate inside the cluster's network and externally.
  - Steps:
    1) Cluster IP
    2) Target Port
    3) NodePort
    4) External IPs
    5) Load Balancer
- Link: https://www.katacoda.com/courses/kubernetes/networking-introduction

- **Exercise 05:** Create Ingress Routing
  - Objective: In this scenario you will learn how to deploy and configure Ingress rules to manage incoming HTTP requests.
  - Steps:
    1) Create Deployment
    2) Deploy Ingress
    3) Deploy Ingress Rules
    4) Test
- Link: https://www.katacoda.com/courses/kubernetes/create-kubernetes-ingress-routes

- **Exercise 06:** Liveness and Readiness Healthchecks
  - Objective: In this scenario, you'll learn how Kubernetes checks containers health using Readiness and Liveness Probes.
  - Steps:
    1) Launch Cluster
    2) Readiness Probe
    3) Liveness Probe
- Link: https://www.katacoda.com/courses/kubernetes/liveness-readiness-healthchecks

- **Exercise 07:** Use Kubernetes to manage Secrets
  - Objective: In this scenario, you'll learn how manage secrets using Kubernetes. Kubernetes allows you to create secrets that are mounted to a pod via environment variables or as a volume.
  - Steps:
    1) Start Kubernetes
    2) Create Secrets
    3) Consume via Environment Variables
    4) Consume via Volumes
- Link: https://www.katacoda.com/courses/kubernetes/managing-secrets

- **Exercise 08:** Deploying a service from source onto Kubernetes
  - Objective: In this tutorial, we'll show you the basics of deploying a service into Kubernetes from source code to a running Kubernetes cluster.
  - Steps:
    1) The container
    2) Running your containerized service
    3) Kubernetes and manifests
    4) The Container Registry
    5) Running the service in Kubernetes
    6) Automating the deployment process
- Link: https://www.katacoda.com/courses/kubernetes/deploy-service-from-source

- **Exercise 09:** Helm Package Manager
  - Objective: This scenario teaches you how to use Helm, the package manager for Kubernetes, to deploy Redis. Helm simplifies discovering and deploying services to a Kubernetes cluster.
  - Steps:
    1) Install Helm
    2) Search For Chart
    3) Deploy Redis
    4) See Results
- Link: https://www.katacoda.com/courses/kubernetes/helm-package-manager

- **Playground:** Play with Kubernetes
  - Objective: This is not really a Hands-On exercise but a playground where you can just play with Kubernetes.
  - Steps:
    1) Have fun playing with Kubernetes :)
- Link: https://labs.play-with-k8s.com/