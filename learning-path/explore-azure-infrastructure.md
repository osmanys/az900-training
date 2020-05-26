![Exam AZ-900](../images/az900.png "Exam AZ-900")

# [Core Cloud Services - Azure architecture and service guarantees](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/)

## [Introduction]()

- Explore the physical structure of Azure infrastructure
- Understand the service level agreements provided by Azure
- Learn how to provide service level agreements for your apps

## [Understand Datacenters and Regions in Azure](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/2-azure-datacenter-locations)

### What is a region?

A region is a geographical area on the planet containing at least one, but potentially multiple datacenters that are nearby and networked together with a low-latency network. Azure intelligently assigns and controls the resources within each region to ensure workloads are appropriately balanced.

>Some services or virtual machine features are only available in certain regions, such as specific virtual machine sizes or storage types. There are also some global Azure services that do not require you to select a particular region, such as Microsoft Azure Active Directory, Microsoft Azure Traffic Manager, and Azure DNS.

![Azure regions](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/media/2-regions-small.png)

## [Understand Geographies in Azure](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/3-geographies)

Azure divides the world into geographies that are defined by geopolitical boundaries or country borders. An Azure geography is a discrete market typically containing two or more regions that preserve data residency and compliance boundaries.

>Data residency refers to the physical or geographic location of an organization's data or information. It defines the legal or regulatory requirements imposed on data based on the country or region in which it resides and is an important consideration when planning out your application data storage.

## [Understand Availability Zones in Azure](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/4-availability-zones)

### What is an Availability Zone?

Availability Zones are physically separate datacenters within an Azure region.

Each Availability Zone is made up of one or more datacenters equipped with independent power, cooling, and networking. It is set up to be an isolation boundary. If one zone goes down, the other continues working. Availability Zones are connected through high-speed, private fiber-optic networks.

![Availability Zone](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/media/4-availability-zones.png)

## [Understand Region Pairs in Azure](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/5-region-pairs)

### What is a region pair?

Each Azure region is always paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away. This approach allows for the replication of resources (such as virtual machine storage) across a geography that helps reduce the likelihood of interruptions due to events such as natural disasters, civil unrest, power outages, or physical network outages affecting both regions at once. If a region in a pair was affected by a natural disaster, for instance, services would automatically fail over to the other region in its region pair.

![Region pair](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/media/5-region-pairs.png)

## [Understand Service-Level Agreements for Azure](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/6-service-level-agreements)

- SLAs describe Microsoft's commitment to providing Azure customers with specific performance standards.
- There are SLAs for individual Azure products and services.
- SLAs also specify what happens if a service or product fails to perform to a governing SLA's specification

> Azure does not provide SLAs for most services under the Free or Shared tiers. Also, free products such as Azure Advisor do not typically have an SLA.

There are three key characteristics of SLAs for Azure products and services:
- Performance Targets
- Uptime and Connectivity Guarantees
- Service credits

## [Compose SLAs across services](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/7-composite-sla)

When combining SLAs across different service offerings, the resultant SLA is called a *Composite SLA*. The resulting composite SLA can provide higher or lower uptime values, depending on your application architecture.

## [Improve your app reliability in Azure](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/8-improve-app-slas)

You can use SLAs to evaluate how your Azure solutions meet business requirements and the needs of your clients and users. By creating your own SLAs, you can set performance targets to suit your specific Azure application. This approach is known as an *Application SLA*.

### Resiliency

Resiliency is the ability of a system to recover from failures and continue to function. It's not about avoiding failures, but responding to failures in a way that avoids downtime or data loss. The goal of resiliency is to return the application to a fully functioning state following a failure. High availability and disaster recovery are two crucial components of resiliency.

When designing your architecture you need to design for resiliency, and you should perform a *Failure Mode Analysis* (FMA). The goal of an FMA is to identify possible points of failure and to define how the application will respond to those failures.

### Cost and complexity vs. high availability

Availability refers to the time that a system is functional and working. Maximizing availability requires implementing measures to prevent possible service failures. However, devising preventative measures can be difficult and expensive, and often results in complex solutions.

> - For example: A workload that requires 99.99 percent uptime shouldn't depend upon a service with a 99.9 percent SLA.
> - For example: An SLA that defines an uptime of 99.999% only allows for about 5 minutes of total downtime per year

## [Summary](https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/9-summary)

Microsoft provides more global presence than any other cloud provider with over 54 regions distributed worldwide. This infrastructure gives you the scale needed to bring your applications closer to users around the world.

### Check your knowledge

- **Deploying an app can be done directly to what level of physical granularity?**
    - [x] Region
    - [ ] Datacenter
    - [ ] Server rack

- **To use Azure datacenters that are made available with power, cooling, and networking capabilities independent from other datacenters in a region, choose a region that supports _________?**
    - [ ] Geography distribution
    - [ ] Service-Level Agreements (SLAs)
    - [x] Availability Zones

- **Application availability refers to what?**
    - [ ] The service level agreement of the associated resource.
    - [ ] Application support for an availability zone.
    - [x] The overall time that a system is functional and working.

\
[![Core Cloud Services - Manage services with the Azure portal](../images/next.png)](tour-azure-portal.md)