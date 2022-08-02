---
title: "Project"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 30
---

### Introduction
Up until now you received the virtual machines and you had to deploy the WeightTracker application and manage the database by yourself. This week’s project will be to provision your own infrastructure in Microsoft Azure following best practices and deploy the WeightTracker application into it.


### Project Overview
For this project you will need to create all the infrastructure required for the WeightTracker application. All the infrastructure is not only the virtual machines where you’ve been deploying the application but also everything around it, security, networking, etc. Aspects such as organization, security, performance and cost optimization will be taken into account during the evaluation.


#### Goals

![Project-3-Basic](/images/week-3-project-basic.png)

- Create the infrastructure above including: 
  - Create a Resource Group for your Project
  - Create a Virtual Network with two subnets: the "public" and the "private" subnets
  - Deploy the web server into the public subnet and allow users to reach the application from everywhere
  - Deploy the database server into the private subnet and ensure that there is no public access to the database (only from the application)
- Configure the database
- Configure the web server
- Ensure the application is up and running (and work automatically after reboot)
- Grant contributor access to rhinopsbootcamp@outlook.com at your subscription level (required in order to be able to perform the evaluation)


### Considerations
- Ensure your Network Security Group (NSG) allows you to access the servers and allows communication between the web server and the database
- Make sure the database cannot be accessed from the internet (it's not publicly exposed)
- Take into account that you have a limited budget so keep servers down when not needed and use the smallest instances possible to keep costs low
- If you wish, you can use another cloud provider (but take into account that the costs will be on your own)

### Expected Result
- All the infrastructure needed to deploy the WeightTracker application
- The WeightTracker application deployed into it and reachable from your browser
- Database server not accessible from the internet
- Ensure that your application and databases start automatically when an instance is rebooted 
- Ensure that your data is persistent
- The user rhinopsbootcamp@outlook.com have contributor access to your subscription

### Bonus
![Project-3-Bonus](/images/week-3-project-bonus.png)
- **Bonus A:** Ensure that your solution is High Available by using multiple application servers (as shown in the diagram above)
- **Bonus B:** Use the Azure PostgreSQL managed Service (Note that this can be an expensive service)
- **Bonus C:** Make your solution elastic by using Virtual Machine Scale Sets

**Note:** Up to 2 bonuses will be evaluated. However, in case of doing all of them, the points will be awarded to the two best and you will receive feedback for each of them.

### Delivery
- Grant contributor access to rhinopsbootcamp@outlook.com at your subscription level
- Grant rhinopsbootcamp@outlook.com access to your application, Please set the password to be:  SelaBootcamp4! (okta)
- Fill out the following form: [Delivery Form](https://forms.gle/Utwc9n5A3zrfnze3A)
- Send a print screen in your 1-on-1 channel showing the resources created in your resource group
- Send on your 1-on-1 channel a screenshot of the Weight Tracker application running in your browser (after adding some data)
