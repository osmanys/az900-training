![Exam AZ-900](../images/az900.png "Exam AZ-900")

# [Predict costs and optimize spending for Azure](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/)

## [Introduction](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/1-introduction)

- Learn the different options you have to purchase Azure services
- Estimate costs with the Azure pricing calculator
- Predict and optimize costs with Azure Cost Management and Azure Advisor
- Apply best practices for saving on infrastructure costs
- Apply best practices for saving on licensing costs

## [Purchase Azure products and services](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/1a-purchasing-products)

### Usage meters
When you provision an Azure resource, Azure creates one or more meter instances for that resource. The meters track the resources' usage, and generate a usage record that is used to calculate your bill.

## [Factors affecting costs](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/1b-factors-affecting-cost)

### Resource type
Costs are resource-specific, so the usage that a meter tracks and the number of meters associated with a resource depend on the resource type.

### Services
Azure usage rates and billing periods can differ between Enterprise, Web Direct, and Cloud Solution Provider (CSP) customers. Some subscription types also include usage allowances, which affect costs.

### Location
Azure has datacenters all over the world. Usage costs vary between locations that offer particular Azure products, services, and resources based on popularity, demand, and local infrastructure costs.

### Azure billing zones
Bandwidth refers to data moving in and out of Azure datacenters. Most of the time inbound data transfers (data going into Azure datacenters) are free. For outbound data transfers (data going out of Azure datacenters), the data transfer pricing is based on **Billing Zones**.

|**Zone**|**Areas**|
|-|-|
|Zone 1|United States, US Government, Europe, Canada, UK, France, Switzerland|
|Zone 2|East Asia, Southeast Asia, Japan, Australia, India, Korea|
|Zone 3|Brazil, South Africa, UAE|
|DE Zone 1|Germany|

>In most zones, the first outbound 5 gigabytes (GB) per month are free. After that amount, you are billed a fixed price per GB.

## [Exercise - Estimate costs with the Azure pricing calculator](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/2-estimate-costs-with-the-azure-pricing-calculator)

### Introducing the Azure pricing calculator

|**Option**|	**Description**|
|-|-|
|Region|	Lists the regions from which you can provision a product. Southeast Asia, central Canada, the western United States, and northern Europe are among the possible regions available for some resources.|
|Tier|	Sets the type of tier you wish to allocate to a selected resource, such as Free Tier, Basic Tier, etc.|
|Billing Options|	Highlights the billing options available to different types of customers and subscriptions for a chosen product.|
|Support Options|	Allows you to pick from included or paid support pricing options for a selected product.|
|Programs and Offers|	Allows you to choose from available price offerings according to your customer or subscription type.|
|Azure Dev/Test Pricing|	Lists the available development and test prices for a product. Dev/Test pricing applies only when you run resources within an Azure subscription that is based on a Dev/Test offer.|

### Estimate a solution
We can use the Azure pricing calculator to figure out what the solution will cost and export our estimate to share with the team. From the **Example Scenarios** tab, you can add all the resources involved with a common solution to the problem you are trying to solve to estimate all the potential costs. You can also add individual products from the **Products** tab to create an estimate for your custom solution.

>If you have resources that are not location-sensitive, you can save a lot of money by locating them in less expensive regions. Checking the pricing calculator can help you determine the most cost-effective place to put these services.

### Share and save your estimate
We now have an estimate for our solution. We can save this estimate, so we can come back to it later and adjust it if necessary. We can also export it to Excel for further analysis or share the estimate via a URL.

### Check your knowledge
1. **Which tab of the Azure pricing calculator will you use to put together your estimate?**
    - [ ] Estimate
    - [x] Products
2. **True or false: You can share your estimate through an Excel spreadsheet or through a URL.**
    - [x] True
    - [ ] False

## [Exercise - Predict and optimize with Cost Management and Azure Advisor](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/3-predict-and-optimize-with-cost-management-and-advisor)

### What is Azure Advisor?
Azure Advisor is a free service built into Azure that provides recommendations on high availability, security, performance, operational excellence, and cost. Advisor analyzes your deployed services and looks for ways to improve your environment across each of these areas.

Advisor makes cost recommendations in the following areas:
- Reduce costs by eliminating unprovisioned Azure ExpressRoute circuits.
- Buy reserved instances to save money over pay-as-you-go.
- Right-size or shutdown underutilized virtual machines.

![Azure Advisor](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/media/3-advisor-recommendations.png)

### Azure Cost Management
Azure Cost Management is another free, built-in Azure tool that can be used to gain greater insights into where your cloud money is going. You can see historical breakdowns of what services you are spending your money on and how it is tracking against budgets that you have set. You can set budgets, schedule reports, and analyze your cost areas.

![Azure Cost Management](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/media/3-cost-management.png)

### Check your knowledge
1. ***Azure Advisor provides recommendations for _________.***
    - [ ] Costs only
    - [x] High availability, security, performance, operational excellence, and cost
    - [ ] High availability, performance, and cost
2. **Azure Cost Management allows you to _________.**
    - [x] See historical breakdowns of what services you are spending your money on.
    - [ ] See estimates of what your services might cost if you make a change.

## [Exercise - Estimate the Total Cost of Ownership with the Azure TCO calculator](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/3a-total-cost-of-ownership)

The pricing calculator and cost management advisor can help you predict and analyze your spend for new or existing services.

- Step 1: Open the TCO calculator
- Step 2: Define your workloads
- Step 3: Adjust assumptions
- Step 4: View the report

![Azure TCO calculator](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/media/3a-tco-calculator-report.png)

## [Save on infrastructure costs](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/4-save-on-infrastructure-costs)

### Use Azure credits
Visual Studio subscribers can activate a monthly credit benefit that allows you to experiment with, develop, and test new solutions on Azure.
- $50 per month for Visual Studio Professional
- $150 per month for Visual Studio Enterprise

### Use spending limits
By default, Azure subscriptions that have associated monthly credits (which includes trial accounts) have a spending limit to ensure you aren't charged once you have used up your credits.

### Use reserved instances
If you have virtual machine workloads that are static and predictable, using reserved instances is a fantastic way to potentially save up to 70 to 80 percent off the pay-as-you-go cost.

### Choose low-cost locations and regions
The cost of Azure products, services, and resources can vary across locations and regions, and if possible, you should use them in those locations and regions where they cost less.
>Some resources are metered and billed according to how much outgoing network bandwidth they consume (egress). You should provision connected resources that are bandwidth metered in the same region to reduce egress traffic between them.

### Research available cost-saving offers
Keep up to date with the latest Azure customer and subscription offers, and switch to offers that provide the most significant cost-saving benefit.

### Right-size underutilized virtual machines
Recall from our previous discussion that Azure Cost Management and Azure Advisor might recommend right-sizing or shutting down VMs. Right-sizing a virtual machine is the process of resizing it to a proper size.

### Deallocate virtual machines in off hours
If you have virtual machine workloads that are only used during certain periods, but you're running them every hour of every day, you're wasting money. These VMs are great candidates to shut down when not in use and start back up on a schedule, saving you compute costs while the VM is deallocated.

### Delete unused virtual machines
This advice may sound obvious, but if you aren't using a service, you should shut it down.

### Migrate to PaaS or SaaS services
Lastly, as you move workloads to the cloud, a natural evolution is to start with infrastructure-as-a-service (IaaS) services and then move them to platform-as-a-service (PaaS) services, as appropriate, in an iterative process.
PaaS services typically provide substantial savings in both resource and operational costs.

### Check your knowledge
1. **Which one of these approaches is not a cost-saving solution?**
    - [ ] Deallocate virtual machines during off hours.
    - [ ] Use Azure Reserved Virtual Machine Instances.
    - [x] Load balance your virtual machines for incoming messages.
    - [ ] Right-size underutilized virtual machines.
2. **True or false: PaaS is typically less expensive than IaaS.**
    - [x] True
    - [ ] False

## [Save on licensing costs](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/5-save-on-licensing-costs)

### Linux vs. Windows
Many of the Azure services you deploy have the choice of running on Windows or Linux. In some cases, the cost of the product can be different based on the OS you choose.

### Azure Hybrid Benefit for Windows Server
Many customers have invested in Windows Server licenses and would like to repurpose this investment on Azure. The Azure Hybrid Benefit gives customers the right to use these licenses for virtual machines on Azure.
- Each two-processor license or each set of 16-core licenses is entitled to two instances of up to eight cores or one instance of up to 16 cores.
- Standard Edition licenses can only be used either on-premises or in Azure, but not both. That means you can't use the same license for an Azure VM and a local computer.
- Datacenter Edition benefits allow for simultaneous usage both on-premises and in Azure so that the license will cover two running Windows machines.

### Azure Hybrid Benefit for SQL Server
Azure Hybrid Benefit for SQL Server is an Azure-based benefit that enables you to use your SQL Server licenses with active Software Assurance to pay a reduced rate.

![Azure Hybrid Benefit for SQL Server](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/media/5-sql-tradein-value.png)

### Use Dev/Test subscription offers
The [Enterprise Dev/Test](https://azure.microsoft.com/offers/ms-azr-0148p/) and [Pay-As-You-Go (PAYG) Dev/Test](https://azure.microsoft.com/offers/ms-azr-0023p/) offers are a benefit you can take advantage of to save costs on your non-production environments. This benefit gives you several discounts, most notably for Windows workloads, eliminating license charges and only billing you at the Linux rate for virtual machines.

### Bring your own SQL Server license
If you are a customer on an Enterprise Agreement and already have an investment in SQL Server licenses, and they have freed up as part of moving resources to Azure, you can provision **bring your own license** (BYOL) images off the Azure Marketplace, giving you the ability to take advantage of these unused licenses and reduce your Azure VM cost.
>An Enterprise Agreement subscription is required to use these certified BYOL images.

### Use SQL Server Developer Edition
Many people are unaware that SQL Server Developer Edition is a free product **for nonproduction use**. Developer Edition has all the same features that Enterprise Edition has, but for nonproduction workloads, you can save dramatically on your licensing costs.

### Use constrained instance sizes for database workloads
Many customers have high requirements for memory, storage, or I/O bandwidth. But they also often have low requirements for CPU core counts. Based on this popular request, Microsoft has made available the most popular VM sizes (DS, ES, GS, and MS) in new sizes that constrain the vCPU count to one half or one-quarter of the original VM size, while maintaining the same memory, storage, and I/O bandwidth.

### Check your knowledge
1. **True or false: If you already have Windows Server licenses, you have to pay for them again on Azure.**
    - [ ] True
    - [x] False
2. **True or false: Azure has money-saving options for test and development servers.**
    - [x] True
    - [ ] False

## [Summary](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/6-summary)

We've talked through the Azure pricing calculator and how you can use it to estimate your costs on Azure and compare pricing between different service offerings. We looked at savings options, how to export pricing estimates, and at tools that Azure has available to help you keep your cloud spend in check.
- Azure Advisor provides recommendations in many areas, including cost.
- Azure Cost Management gives you reporting and billing information, so you can gain insights into where you're spending your money.

We then explored best practices to help you save money on both infrastructure and licensing.

### Check your knowledge
1. **Which one of the following systems is used to determine Azure costs for each billing period?**
    - [ ] The Azure website
    - [ ] Number of created virtual machines
    - [ ] The Azure pricing calculator
    - [x] Usage meters
2. **Which of the following factors affects costs?**
    - [ ] Global infrastructure
    - [x] Location
    - [ ] Availability zone
3. **Complete the following sentence. As an Azure customer, Azure Reservations offer discounted prices if you _________**
    - [x] Make upfront commitments on compute capacity
    - [ ] Provision many resources
    - [ ] Have a free account
    - [ ] Set Spending Limits

\
[![Home](../images/next.png)](../README.md)