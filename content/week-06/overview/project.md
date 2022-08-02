---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

## Introduction
Last week we created a Terraform template that automates the process of provisioning our infrastructure in the Cloud. This week we are going to add Ansible to our toolbox in order to automate the whole configuration of the servers and deploy our NodeWeightTracker application using Configuration Management practices.

## Project Overview
This week we are going to write an Ansible playbook(s) to configure the servers created by terraform and then, install the NodeWeightTracker application (including all its dependencies). In addition, after everything we did so far we are ready to move to production. To achieve this we will need to provision 2 identical environments, one for staging and another for production.

![Environments](/images/week-6-envs.png)

## Goals
- Use Terraform to provision the infrastructure 
- Use Ansible to deploy the NodeWeightTracker application
- Create two environments: Staging and Production
- Both environments must be identical except for the size of the vms (production ones must be larger)
- In this project using a Managed Postgresql is required (previously Bonus "B")

## Considerations
- Ansible Playbooks should be stored in a repository
- Ansible uses Yaml files for its playbooks which is a widely used markup language and you should start get used to it's strict syntax.
- This project should be quite easier than previous projects, so take advantage of the remaining time to polish and improve your work so far.
- Make sure that all your code is clean and organized
- This week has a single bonus that can be very complex (it's not worth trying to do it before having finished the base project and having corrected the feedback received so far)

## Expected Result
- Two environments provisioned by Terraform
- The Weight Tracker Application deployed using Ansible

## Bonus
- Create a third environment called "POC" in which you must use Windows servers and deploy the application  using Ansible

## Delivery
- Grant contributor access to rhinopsbootcamp@outlook.com at your subscription level
- Grant rhinopsbootcamp@outlook.com access to your application (okta)
- Fill out the following form: [Delivery Form](https://forms.gle/CTDhJk9ocYA74Ap97)
- Send on your 1-on-1 channel a screenshot of the Weight Tracker application running in your browser (after adding some data)
