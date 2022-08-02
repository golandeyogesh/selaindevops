---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

## Introduction

In this week's project we will get to know the application that we will use throughout the Bootcamp: The Weight Tracker App. As it would happen in real life, you have the documentation provided by the developers team at your disposal, but making it work is your sole responsibility.

![scripts](/images/weight-tracker.png)

## Project Overview

The Weight Tracker App is a web application that helps you track your weight and see your progress over time. The application must be deployed using two servers: one for the application and one for the database (using Postgresql). Also the application uses Okta to control access.

Some important notes:

- The application source code available for download in this [Github repository](https://github.com/sela-rhinops/bootcamp-app).
- For this project you will receive 2 ubuntu servers.
- You will have to create a free Okta account for this project

## Goals

- Fork the application repository to create your own repository
- Access the servers
- Configure the database server (postgresql)
- Configure the web server (install prerequisites)
- Deploy the application (developed on nodejs)
- Test that the application is running and reachable
- Make sure your application keeps running even if any of the servers is restarted
- Note that the application uses Okta for authentication

## Considerations 

- Make sure you meet each of the project requirements
- Ensure that all application dependencies are installed
- Ensure that the web server can reach the db server
- Note that by default PostgreSQL is not reachable from outside the server and it should be changed in order to allow communication with the web server
- Ensure that the web server can authenticate with the database
- Ensure that the port you are configuring the web server to serve the application is open
- Make sure you understand every single thing you do

## Bonus

#### Part 1: Create and build a website
- Create "ASP.NET Core Web App" project
- Check your csproj content
- Add "Newtonsoft.Json"
- Check your csproj again, what changed? 
- Restore Nuget Packages
- Compile (rebuild) your project
- Which files and folders were created? 
- Publish your application

#### Part 2: Create website on your Microsoft machine
- Add IIS to your windows server
- Create a new IIS application pool
- Create website (use port 5100 and your new application pool)
- Copy your website to your windows server
- Browse to "http://localhost:5100/" from your microsoft machine
- Does it works? If not, make it work

#### Notes
- For this project you will receive a windows server
- Store your application source code on a public git repository
- Create a README.md file explaining the build and installation process (use markdown capabilities to create a better documentation)

## Expected Result

- The Weight Tracker application is running and accessible through http//<web-server-ip>:8080 in your browser

![scripts](/images/project-1-exres.png)

## Delivery

- Grant rhinopsbootcamp@outlook.com access to your application, Please set the password to be:  SelaBootcamp4! (okta)
- Fill out the following form: [Delivery Form](https://forms.gle/pj8uKVTBcTk6GPur8)
- Send on your 1-on-1 channel a screenshot of the Weight Tracker application running in your browser (after adding some data)
- Send on your 1-on-1 channel a screenshot of you IIS application
