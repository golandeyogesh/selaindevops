# Bootcamp Portal

## Description

This repository contains the source code of the bootcamp portal website. The bootcamp portal is a website that is used as an index to organize all the bootcamp information. The information is separated by weeks and each week in turn is organized into sections as shown below:

- **Overview:** Introduces the topic of the week, explains the motivation for studying it and explains how it relates to what was previously studied.
- **Objectives:** Define the learning objectives of the week (what results are expected to be obtained at the end of the week)
- **Project:** Explains the project of the week and defines the requirements and guidelines for its implementation
- **Quiz Topics:** List the topics to evaluate during the quiz of the week
- **Resources:** Provides a list of recommended resources for self-learning
- **Recordings:** Access the recording of the week lectures
- **Slides:** Access to the slides used during the week lectures

## Infrastructure

The portal infrastructure is deployed in Azure using the "Static Web App" service and GitHub Actions is used to automatically deploy the changes introduced in the main branch. The website is exposed using the domain "rhinops.io" which is being managed in “Azure DNS”. In addition, Azure blob storage is used to store lecture recordings.

Azure resources details:
- **Azure Subscription:** 51693fff-9399-4139-9c8e-57c93f889896
- **Resource Group:** Rhinops
- **Portal Static Web App:** devops-bootcamp
- **Recordings Blob Storage:** devopsbootcamp/
- **Azure DNS Zone:** rhinops.io

## Access Management

The portal uses the Authentication and Authorization features provided by "Azure Static Web Apps" to control access to the portal through the use of "Role Management" which is controlled through the Azure portal and the "staticwebapp.config.json" file that it’s located in the repository root. For more details see the official documentation of "Azure Static Web Apps": https://docs.microsoft.com/en-us/azure/static-web-apps/authentication-authorization?tabs=invitations 

## CI/CD

A Github Action workflow is configured to deploy automatically any change in the master branch into the Azure Static Web App
