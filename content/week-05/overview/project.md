---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

## Introduction

Terraform is a widely used Infrastructure as code ( IaC ) tool that helps automate the provisioning of infrastructure and when used in combination with tools like Ansible we can automate the whole process from nothing to having applications running in already configured infrastructure.

![Terraform](/images/terraform-logo.png)

## Project Overview

In this week’s project we are going to recreate the infrastructure of the WeightTracker application but this time instead of doing it manually we are going to use Terraform to automate this process. The infrastructure that you have to deploy is the same as last week's project with the first bonus (High Availability).

![Project-3-Bonus](/images/week-4-project-env.png)

## Goals

1. Use Terraform to define all the infrastructure
2. Use Terraform variables to configure at least 5 parameters for your template
3. Configure a terraform output, so the vm password can be retrieved during automation (Linux servers must be configured with password authentication instead of SSH keys)
4. Create a terraform module to reuse the code that creates the virtual machines
5. Install the WeightTracker application and the Database into the VMs created by terraform (the installation can be done manually)
6. Ensure the application is up and running (and work automatically after reboot)


## Considerations

- Remember to run terraform destroy during the development to avoid spending too much from your student credits (provision it prior your delivery)
- Manage the entire project on Git
- Remember to keep your code clean and documented
- Ensure your Network Security Group (NSG) allows you to access the servers and allows communication between the web server and the database
- Make sure the database cannot be accessed from the internet (it’s not publicly exposed)
- Take into account that you have a limited budget so keep servers down when not needed and use the smallest instances possible to keep costs low

## Expected Result

- A Terraform template that deploys the required infrastructure
- The WeightTracker application up and running
- Database server is not accessible from the internet
- Ensure that your application and databases start automatically when an instance is rebooted
- The user rhinopsbootcamp@outlook.com have contributor access to your subscription
- The user rhinopsbootcamp@outlook.com have access to your application (okta)

## Bonus

1. Use a Terraform backend to store the Terraform state in Azure Blob Storage
2. Use the Azure PostgreSQL manged service instead of a VM (Bonus "B" from previous week)
3. Implement the bonus "C" (Elasticity) from the previous project using Terraform 

## Delivery

- Grant contributor access to rhinopsbootcamp@outlook.com at your subscription level
- Grant rhinopsbootcamp@outlook.com access to your application (okta)
- Fill out the following form: [Delivery Form](https://forms.gle/Abc1NF1xdN8TS8pu9)
- Send on your 1-on-1 channel a screenshot of the Weight Tracker application running in your browser (after adding some data)
