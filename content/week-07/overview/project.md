---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

## Introduction
For the last few weeks we have been using terraform to provision the infrastructure of our application and we are using ansible to automate the deployment process, which is quite respectable but not enough. This week we will finish automating the entire process by using CI/CD methodologies to orchestrate the use of both tools and deploy the changes made to the code continuously and automatically.

## Project Overview
This week’s project consists of using Azure Pipelines to configure a complete CI/CD pipeline for the WeightTracker application that includes building the application and deploying it into (an existent) infrastructure. As a bonus we are going to create an additional CI/CD pipeline to automate the infrastructure updates when our Terraform code changes.

![Pipeline](/images/Bootcamp-Project-CICD.png)

## Goals

1) Create an Azure DevOps Organization
2) Create a CICD (yaml) / CI (classic) Pipeline using Azure Pipelines (preferably using yaml over Classic)
3) CI pipeline should trigger automatically on every commit
4) Use Azure Artifacts to store your build Artifacts
5) Create a CD Job using Yaml job (yaml) / Azure Release Pipelines (classic)
6) Configure your CD stage to deploy to Staging using Continuous Deployment
7) Configure your CD stage to deploy to Production using Continuous *Delivery*


## Considerations
- You can store your source code in Github, Azure Repos or both
- It will be easier for you if your terraform source code is stored in its own repository
- It will be easier for you if your ansible source code is stored in its own repository
- Focus on achieving this week's objectives, next week you will have time to organize what you have done so far
- Use the Ansible playbooks from the last week to deploy the application
- Use Azure Pipeline Library when it comes to configurations / secrets

## Expected Result
- Full CI/CD pipeline that automates the process of building and deploying the application in a pre existent infrastructure
- In case of making a change to the code and pushing it, it will be automatically deployed to the Staging environment
- Deployment to production must consist of a *manual approval*

## Bonus
- Bonus A: Create a CI/CD Pipeline for the infrastructure (in the way you consider best)
- Bonus B: Implemented the infracost tool in your bonus A CI/CD for terraform.
            It can be in a PR or on a Commit.


## Delivery
- Fill out the following form: [Delivery Form](https://forms.gle/WRs5SRp3JUW2ewR8A) 
- Any additional files that have not been uploaded to git for security reasons must be submitted by discord
- Grant contributor access to rhinopsbootcamp@outlook.com at your subscription level
- Grant rhinopsbootcamp@outlook.com access to your application (okta)
- Add rhinopsbootcamp@outlook.com as a Admin user in your Azure DevOps Project.
