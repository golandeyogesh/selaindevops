---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

## Introduction

When we built our application trought the CI/CD pipeline we didn't package it in the best possible way. All we did was to compress the application with it's dependencies into a zip file which allowed us to deploy the application automatically after configuring the required runtime in the target server. However, today one of the most useful and best ways to package applications are Containers because they allows us to package the application together with it dependencies and runtime in a single artifact.

## Project Overview

This week's project consists on writing a Dockerfile to package your NodeWeightTracker application into an image and configure a CI/CD process to automate the deployment. However this week we will raise the level a bit to achieve a CI/CD process that complies with best practices and implement the practice of Pipeline as Code.

Regarding the architecture of our solution we will keep the same infrastrucutre but this time we will run the application as a container:

![docker-envs](/images/docker-envs.png)

In this project we will manage the code of our application using one of the most common and simple Git workflow usually called the "Feature Branch Workflow" in which branches named with the prefix "feature/" are used to work on the code independently and then the code is integrated into the master/main branch to be deployed in the target environments.

![feature-branch](/images/feature-branch.png)

To optimize the worflow you will need to configure a branch policy for the master/main branch to enforce Code Review by using Pull Requests and a Build Validation Policy to ensure that the changes are ok before integrating them.

![branch-policy](/images/branch-policy.png)

Finally, the CI/CD process must meet the following requirements:

  - For Feature Branches:
    - Whenever a new change is pushed to a feature branch this should start the CI pipeline that will take the Dockerfile from the repository and build an image to ensure that everything is ok (note that we don't want to push it to the registry since we have not yet reached the integration branch, our only objective is to provide the developer with an indication of whether their code is correct or not).
  
  - For Master/Main Branch:
    - Whenever a new change is pushed to the main/master branch this should start the CI process that will take the Dockerfile from the repository, build an image and push it to a container registry (Azure ACR).
    - Then the CD consists on pulling the image from the registry and deploying it into the staging environments automatically (Continuous Deployment) and then wait for approval to deploy into the Production environment (Continuous Delivery)

![docker-cicd](/images/docker-cicd.png)

Last but not least, you should configure your pipelines using Yaml pipelines to implement the "Pipeline as Code" practice. In this case you will need a single pipeline (instead of a Build Pipeline and a Release Pipeline) but that uses different stages to separate the processes and integrates with the "Environments" feature so that, among other things, you can configure approvals for the stage that deploy to production. Your pipeline should look something like this:

```
name: <<YOUR PIPELINE NAME CONFIG>>

trigger:
- master
- feature/*

pool:
  vmImage: ubuntu-latest

variables:
  YOURVARKEYS: YOURVARVALUES
  ...

stages:

# Continuous Integration Process
- stage: CI
  jobs:
  - job: BuildAndPushDocker
    workspace: 
      clean: all
    steps:
    - <<YOUR TASKS>>

# Continuous Deployment Process for Staging Environment
- stage: DeployToStaging
  condition: and(succeeded(), eq(variables['build.sourceBranch'], 'refs/heads/master'))
  jobs:
  - deployment: staging
    displayName: Deploy to Staging
    environment:
      name: <<YOUR ENVIRONMENT NAME>>
      resourceType: VirtualMachine
    strategy:
      runOnce:
        deploy:
          steps:
          - <<YOUR TASKS>>
          
# Continuous Delivery Process for Production Environment
- stage: DeployToProduction
  condition: and(succeeded(), eq(variables['build.sourceBranch'], 'refs/heads/master'))
  jobs:
  - deployment: production
    displayName: Deploy to Production
    environment:
      name: <<YOUR ENVIRONMENT NAME>>
      resourceType: VirtualMachine
    strategy:
      runOnce:
        deploy:
          steps:
          - <<YOUR TASKS>>
```

## Goals
- Write a Dockerfile for your NodeWeightTracker application and add it to the application's repository.
- Configure a branch policy to avoid commiting to the master/main branch directly forcing code review and build validations.
- Write a CI/CD pipeline that uses the Dockerfile to package your application into an image, push it to Azure Container Registry and deploy it into the target environments (automatically to Staging and after approval to Production).
- Ensure your pipeline is totally configured with yaml (pipeline as code)

## Considerations
- Follow best practices when writing the Dockerfile
- The multi-stage pattern in your Dockerfile allows you to build faster and smaller images
- Remember that when using yaml builds the entire CI/CD process is configured in a single pipeline but divided into stages.
- To be able to configure manual approvals for certain stages (as you did when you used release pipelines with the UI) it's necessary to integrate your yaml pipeline with "Azure Pipelines Environments"
- To avoid unexpected issues, make sure your VM has all the requirements (docker that can be run containers without sudo) before configuring the environment.
- Make sure your containers know how to run automatically in case of any problem (for example after a server reboot)

## Expected Result
- A Dockerfile to package the NodeWeightTracker application into an image.
- Branch policies to force code review and build validation configured for the master/main branch
- A CI/CD pipeline to automate the application lifecycle
- Images stored on Azure Container Registry (ACR)
- CI/CD implementing the principle of "Pipeline as Code" by using Yaml with multiple stages
![Environments](/images/docker-pipeline.png)

## Bonus
- Write a docker-compose.yaml file that deploys the application and the database for development purposes only (do not use it as a part of the CI/CD)
- Use a private Azure Container Registry to store your images

## Delivery
- Fill out the following form: [Delivery Form](https://forms.gle/YCh63qWYS3JiC4Bw6)
- Any additional files that have not been uploaded to git for security reasons must be submitted by discord
- Grant contributor access to rhinopsbootcamp@outlook.com at your subscription level
- Grant rhinopsbootcamp@outlook.com access to your application (okta)
- Grant rhinopsbootcamp@outlook.com Contributor access to your Azure DevOps Project
