---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

### Introduction

A package manager is a programming language’s tool to create project environments and easily import external dependencies. You don’t have to reinvent the wheel and are able to make the most out of the tools that are at your disposal. They are commonly used everywhere so as a DevOps engineer it's vital to be familiar with them.

### Project Overview

In this project you will create and publish your own package (choosing the platform that you prefer) in both public and private repositories. Also you will install a Global Repository Management to store all your packages in a single place.

![package-repositories](/images/package-repositories.png)

### Goals

- Create a package using the platform of your choice
- Publish the package to the global repository
- Configure a "Global Artifact Manager" such as Nexus, Artifactory, Github Packages
- Publish your package in your private repository

### Considerations

- Check that the platform of your choice is supported in the free version of the repository manager (for example Artifactory supports only Maven, Gradle, Ivy, SBT and Generic repositories)
- Packages are not expected to be published automatically (we haven't talked about CI/CD yet)
- You can use the platform of your choice but if you don't have prior knowledge, we recommend starting with npm since it's the simplest

### Expected Result

- Your package is published in the global repository
- Your package is published in your own private repository 

### Bonus

- Create packages for multiple platforms

### Delivery

- Send on your Discord private channel the following:
  - Link to your git repository that contains the package source code
  - Screenshot of your package published in the global repository
  - Screenshot of your package published in your own private repository