---
title: "Overview"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 10
---

When developing an application there are three main design patterns that are commonly used to design the architecture of the application. They are the:
  - **Monolithic Architecture**: is a single application stack that contains all functionality within that 1 application. This is tightly coupled, both in the interaction between the services and how they are developed and delivered. 
  - **Service Oriented Architecture (SOA)**: is a well-established style of software design, that is similar to the microservices architecture style. SOA structures apps into discrete, reusable services that communicate through an enterprise service bus (ESB). 
  - **Microservices**: are both an architecture and an approach to writing software. With microservices, apps are broken down into their smallest components, independent from each other. Each of these components, or processes, is a microservice.

  Microservices are distributed and loosely coupled, so they don’t impact one another. This has benefits for both dynamic scalability and fault tolerance: individual services can be scaled as needed without requiring heavy infrastructure or can failover without impacting other services.

  Now that we learned Docker we can see how it is very useful when working with Microservices as it encapsulates your microservice into containers which can then be independently maintained and deployed. Each of these containers will be responsible for one specific business functionality.

  This week is mostly about learning the fundamental concepts of the Microservices Architechture so that we can understand what is it about.

  ![Example](/images/microservices-example.png)