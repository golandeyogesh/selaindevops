---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

## Introduction

Last week we learned about Docker and how it can help us package and deploy applications with ease and even used it in our CI/CD pipelines for the NodeWeightTracker application, but that was a very simple application with a relatively simple architecture. Today the Microservices architecture is getting even more popular with the rise of tools like Docker and Kubernetes so as DevOps engineers we need to understand what it is about and how do we manage all those services.

## Project Overview

- This week's project is a very special one as we are all going to work as a team to solve the following scenario:

  - The developement team just finished taking the "Sela Calculator" application that was once written as a Monolith and broke it down into multiple Microservices. Now it's our job as the DevOps team to finish all the tasks that are needed to manage the lifecycle of all the different Microservices.

  - The "Sela Calculator" application is a simple calculator that makes basic mathematical operations between two given numbers. When it was a monolith all the operations were calculated by the same application but now that it was refactored to work as a microservice there is a single service for each operation and a service for the UI. The application still looks the same but the backend was heavily changed.

  ![sela-calculator](/images/sela-calculator.png)

  - As you may have guessed, each service has its own repository (stored in Gitlab):
    - [UI Service](https://gitlab.com/sela-calculator/ui-service)
    - [Sum Service](https://gitlab.com/sela-calculator/sum-service)
    - [Multiplication Service](https://gitlab.com/sela-calculator/multiplication-service)
    - [Division Service](https://gitlab.com/sela-calculator/division-service)
    - [Substraction Service](https://gitlab.com/sela-calculator/subtraction-service)

  - Also, all the deployment configuration files should be stored in a separated repository (also in Gitlab):
    - [Deployment Repository](https://gitlab.com/sela-calculator/sela-calculator-deployment)

  ![sela-calculator-architecture](/images/sela-calculator-architecture.png)

## Goals

  - Our objective as the DevOps team is to configure the entire DevOps processes for the refactored application, including:
    - Configure DevOps Tools
    - Dockerize the microservices
    - Configure the CI/CD process for the application
    - Improve the application according to the microservices best practices

  - To facilitate the development the Project Manager divided the work into specific tasks. Because we don't have a planning system such as Jira or Azure DevOps he creates a branch for each task in the relevant repository and wrote a file named "Task.md" explaining what needs to be done.

  - Note that for merging a branch it's required to do it through a pull request and someone else has to approve it (you don't have permissions to create new branches on the remote repository so you must work in the existing branches)

## Project Infrastructure

- For this project the IT team is in charge of providing the required infrastructure which is composed as show below by 3 servers:
  - Jenkins Controller
  - Test Environment
  - Production Environment

![Jenkins-Environment](/images/jenkins-infra.png)

- Due resources limitation, Jenkins jobs must run in the same server as the Jenkins Controller.

- The DevOps manager recommends to configure the Jenkins infrastructure in one of the following ways:
  1. By deploying Jenkins as a docker container and configuring the same host as a Jenkins Agent
  2. By creating a custom Docker image of the Jenkins Controller that includes all the required tools to run the jobs directly from the Jenkins Controller
  3. By installing Jenkins without Docker, then installing the required tools for the jobs in the same server and running jobs from the Jenkins Controller

## Project Tasks

- **Task 01: Project Manager**
  - Associated Repository: None
  - Description:
    - Create a board in https://trello.com/ to track the project's progress
    - Assign the tasks to the members of the team
    - Ensure tasks are done in the correct order

- **Task 02: Configure Jenkins**
  - Associated Repository: None
  - Description:
    - Install Jenkins Controller
    - Configure a Jenkins Agent with the required tools for CI/CD or ensure that the Jenkins Controller will be able to run the jobs.

- **Task 03: Dockerize UI Service**
  - Associated Repository: ui-service
  - Description:
    - Create a Dockerfile for the application
    - Create an empty public repository for the service in quay.io (into the "bootcampseladevops" organization)

- **Task 04: Configure CI Pipeline for UI Service**
  - Associated Repository: ui-service
  - Description:
    - Configure a CI pipeline that does the following:
      - Get the sources from Gitlab
      - Build the docker image (created in the previous task)
      - Push the image to the quay.io repository (created in the previous task)
    - Note that the CI should be triggered automatically after each change on the master branch

- **Task 05: Dockerize Sum Service**
  - Associated Repository: sum-service
  - Description:
    - Create a Dockerfile for the application
    - Create an empty public repository for the service in quay.io (into the "bootcampseladevops" organization)

- **Task 06: Configure CI Pipeline for Sum Service**
  - Associated Repository: sum-service
  - Description:
    - Configure a CI pipeline that does the following:
      - Get the sources from Gitlab
      - Build the docker image (created in the previous task)
      - Push the image to the quay.io repository (created in the previous task)
    - Note that the CI should be triggered automatically after each change on the master branch

- **Task 07: Dockerize Subtraction Service**
  - Associated Repository: subtraction-service
  - Description:
    - Create a Dockerfile for the application
    - Create an empty public repository for the service in quay.io (into the "bootcampseladevops" organization)

- **Task 08: Configure CI Pipeline for Subtraction Service**
  - Associated Repository: subtraction-service
  - Description:
    - Configure a CI pipeline that does the following:
      - Get the sources from Gitlab
      - Build the docker image (created in the previous task)
      - Push the image to the quay.io repository (created in the previous task)
    - Note that the CI should be triggered automatically after each change on the master branch

- **Task 09: Dockerize Division Service**
  - Associated Repository: division-service
  - Description:
    - Create a Dockerfile for the application
    - Create an empty public repository for the service in quay.io (into the "bootcampseladevops" organization)

- **Task 10: Configure CI Pipeline for Division Service**
  - Associated Repository: division-service
  - Description:
    - Configure a CI pipeline that does the following:
      - Get the sources from Gitlab
      - Build the docker image (created in the previous task)
      - Push the image to the quay.io repository (created in the previous task)
    - Note that the CI should be triggered automatically after each change on the master branch

- **Task 11: Dockerize Multiplication Service**
  - Associated Repository: multiplication-service
  - Description:
    - Create a Dockerfile for the application
    - Create an empty public repository for the service in quay.io (into the "bootcampseladevops" organization)

- **Task 12: Configure CI Pipeline for Multiplication Service**
  - Associated Repository: multiplication-service
  - Description:
    - Configure a CI pipeline that does the following:
      - Get the sources from Gitlab
      - Build the docker image (created in the previous task)
      - Push the image to the quay.io repository (created in the previous task)
    - Note that the CI should be triggered automatically after each change on the master branch

- **Task 13: Create a docker-compose for the application deployment**
  - Associated Repository: sela-calculator-deployment
  - Description:
    - Write a docker-compose.yaml to deploy the application
    - Note that this task depends on all the previous tasks

- **Task 14: Create a CD pipeline for the application deployment**
  - Associated Repository: sela-calculator-deployment
  - Description:
    - Configure a CD pipeline that does the following:
      - Deploy to Test Environment using Continuous Deployment
      - Wait for approval
      - Deploy to Production Environment using Continuous Delivery
    - Note that this task depends on all the previous tasks

- **Task 15: Configure CD Triggers**
  - Associated Repository: None
  - Description:
    - Ensure that CD Job is triggered after a succesful CI run.
    - Note that this task depends on all the previous tasks

## Considerations

- Each member of the team has to complete at least **one** task
- A task is considered done only after it's merged into the master branch
- The project is considered completed only after **all** tasks are completed
- The environments details will be published through Discord
- All work must be done in the repositories that we provide
- All the docker images must be stored in the registry that we provide
- It's okay to help each other with the tasks but by the end of the project each student should have merged at least one branch into master.
- This project will be reviewed as a team but bonuses are individual
- Note that **this project is the base for Week 10 Bonus** so make sure it's done in the best possible way

## Expected Result

- A Dockerfile in the master branch of each one of the application repositories.
- A Jenkinsfile for CI in the master branch of each one of the application repositories.
- A docker-compose.yaml file in the master branch of the deployment repository.
- A Jenkinsfile for CD in the master branch of the deployment repository.
- A full automated CI/CD process to build and deploy the calculator application in a single VM on two different environments (Test using Continuous Deployment and Production using Continuous Delivery)

## Bonus

1. The Developement team made a mistake when refactoring the UI service. The UI service is currently reaching the operations API's from the client instead from the backend. Therefore all operations API's should be exposed publicly which is an unnecessary expousure that can represent a security risk.

2. To make the application more interesting and understand how microservices are decoupled and independent from one another let's take each one of the backend services and write it in a different language:
   - Sum Service: Java
   - Subtraction Service: C# (dotnet core)
   - Multiplication Service: Golang
   - Division Service: Python

3. Create the required dockerfiles for the rewritten application's services in the new languages

4. The Company wants to stop using quai.io to store it's artifacts. To be able to do this the following task was defined:
  - **Task 16 (Bonus): Configure a private Artifact Manager/Container Registry**
    - Associated Repository: None
    - Description:
      - Ask for an additional VM to set up the Artifact Manager/Container Registry in it.
      - Install and configure one of the following:
        - Jfrog Artifactory
        - Sonatype Nexus Repository
        - Docker Registry (On-Premise)
      - Change CI Pipelines to push the images to the configured Artifact Manager/Container Registry

## Delivery

- This project doesn't really have a delivery because you will be working on our provided environments and repositories.