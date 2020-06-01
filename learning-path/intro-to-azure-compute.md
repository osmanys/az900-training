![Exam AZ-900](../images/az900.png "Exam AZ-900")

# [Core Cloud Services - Azure compute options](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-compute/)

## [Introduction](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-compute/1-introduction)

- Identify compute options in Azure
- Select compute options that are appropriate for your business

## [Essential Azure compute concepts](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-compute/2-essential-azure-compute-concepts)

Azure compute is an on-demand computing service for running cloud-based applications.

There are four common techniques for performing compute in Azure:
- Virtual machines
- Containers
- Azure App Service
- Serverless computing

## [Explore Azure Virtual Machines](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-compute/3-virtual-machines)

Azure Virtual Machines (VMs) let you create and use virtual machines in the cloud. They provide infrastructure as a service (IaaS) in the form of a virtualized server and can be used in many ways.

### Scaling VMs in Azure

#### What are availability sets?
An availability set is a logical grouping of two or more VMs that help keep your application available during planned or unplanned maintenance.

![Availability sets](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-compute/media/3-availability-sets.png)

#### What are virtual machine scale sets?
Azure Virtual Machine Scale Sets let you create and manage a group of identical, load balanced VMs.

#### What is Azure Batch?
Azure Batch enables large-scale job scheduling and compute management with the ability to scale to tens, hundreds, or thousands of VMs.

## [Explore Containers in Azure](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-compute/4-containers)

A container is a modified runtime environment built on top of a host OS that executes your application. A container doesn't use virtualization, so it doesn't waste resources simulating virtual hardware with a redundant OS. This environment typically makes containers more lightweight than VMs.

### Azure Container Instances

Azure Container Instances (ACI) offers the fastest and simplest way to run a container in Azure. You don't have to manage any virtual machines or configure any additional services. It is a PaaS offering that allows you to upload your containers and execute them directly with automatic elastic scale.

### Azure Kubernetes Service

The task of automating, managing, and interacting with a large number of containers is known as orchestration. Azure Kubernetes Service (AKS) is a complete orchestration service for containers with distributed architectures with multiple containers.

### Using containers in your solutions

Containers are often used to create solutions using a *microservice architecture*. This architecture is where you break solutions into smaller, independent pieces. For example, you may split a website into a container hosting your front end, another hosting your back end, and a third for storage. This split allows you to separate portions of your app into logical sections that can be maintained, scaled, or updated independently.

>Imagine your website backend has reached capacity but the front end and storage aren't being stressed. You could scale the back end separately to improve performance, or you could decide to use a different storage service. Or you could even replace the storage container without affecting the rest of the application.

### Migrating apps to containers

![Migrating apps to containers](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-compute/media/4-kub-migration.png)

## [Explore Azure App Service](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-compute/5-appservice)

### App Service costs

You pay for the Azure compute resources your app uses while it processes requests based on the App Service Plan you choose. The App Service plan determines how much hardware is devoted to your host - for example, whether it's dedicated or shared hardware, and how much memory is reserved for it. There is even a free tier you can use to host small, low-traffic sites.

### Web apps

App Service includes full support for hosting web apps using ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP, or Python.

### API apps

Much like hosting a website, you can build REST-based Web APIs using your choice of language and framework. You get full Swagger support, and the ability to package and publish your API in the Azure Marketplace.

### Web jobs

WebJobs allows you to run a program (.exe, Java, PHP, Python, or Node.js) or script (.cmd, .bat, PowerShell, or Bash) in the same context as a web app, API app, or mobile app. They can be scheduled, or run by a trigger. WebJobs are often used to run background tasks as part of your application logic.

### Mobile app back-ends

Use the Mobile Apps feature of Azure App Service to quickly build a back-end for iOS and Android apps.

## [Explore Serverless computing in Azure](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-compute/6-serverless-computing)

- **Abstraction of servers**: Serverless computing abstracts the servers you run on. You never explicitly reserve server instances; the platform manages that for you. Each function execution can run on a different compute instance, and this execution context is transparent to the code. With serverless architecture, you simply deploy your code, which then runs with high availability.

- **Event-driven scale**: Serverless computing is an excellent fit for workloads that respond to incoming events. Events include triggers by timers (for example, if a function needs to run every day at 10:00 AM UTC), HTTP (API and webhook scenarios), queues (for example, with order processing), and much more. Instead of writing an entire application, the developer authors a function, which contains both code and metadata about its triggers and bindings.

- **Micro-billing**: With serverless computing, they pay only for the time their code runs. If no active function executions occur, they're not charged.

## [Summary](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-compute/7-summary)

### Check your knowledge

- **Suppose you have an existing application running locally on your own server. You need additional capacity but prefer to move to Azure instead of buying upgraded on-premises hardware. Which compute option would likely give you the quickest route to getting your application running in Azure?**
    - [ ] Serverless computing
    - [ ] Containers
    - [x] Virtual machines

- **Imagine that you work on a photo-sharing application that runs on millions of mobile devices. Demand is unpredictable because you see a spike in usage whenever a locally or nationally significant event occurs. Which Azure compute resource is the best match for this workload?**
    - [x] Serverless computing
    - [ ] Containers
    - [ ] Virtual machines

- **The compute options give you different levels of control over the configuration of the environment in which your application runs. Which of the following lists the compute options in order of your control from "most control" to "least control"?**
    - [ ] Serverless computing, containers, virtual machines
    - [ ] Containers, serverless computing, virtual machines
    - [x] Virtual machines, containers, serverless computing

\
[![Core Cloud Services - Azure data storage options](../images/next.png)](intro-to-data-in-azure.md)