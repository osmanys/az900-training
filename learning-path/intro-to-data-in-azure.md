![Exam AZ-900](../images/az900.png "Exam AZ-900")

# [Core Cloud Services - Azure data storage options](https://docs.microsoft.com/en-us/learn/modules/intro-to-data-in-azure/)

## [Introduction](https://docs.microsoft.com/en-us/learn/modules/intro-to-data-in-azure/1-introduction)

- Survey the data storage options in Azure
- Discover how Azure data storage can meet your business demands
- Compare Azure data storage with on-premises storage

## [Benefits of using Azure to store data](https://docs.microsoft.com/en-us/learn/modules/intro-to-data-in-azure/2-benefits-of-using-azure-to-store-data)

### Benefits of using Azure to store data
- Automated backup and recovery
- Replication across the globe
- Support for data analytics
- Encryption capabilities
- Multiple data types
- Data storage in virtual disks
- Storage tiers

### Types of data
- **Structured data**: Structured data is data that adheres to a schema, so all of the data has the same fields or properties.
- **Semi-structured data**: Semi-structured data doesn't fit neatly into tables, rows, and columns. Instead, semi-structured data uses tags or keys that organize and provide a hierarchy for the data. Semi-structured data is also referred to as non-relational or NoSQL data.
- **Unstructured data**: Unstructured data encompasses data that has no designated structure to it. For example, a blob can hold a PDF document, a JPG image, a JSON file, video content, etc.

## [How Azure data storage can meet your business storage needs](https://docs.microsoft.com/en-us/learn/modules/intro-to-data-in-azure/3-how-azure-storage-meets-your-business-storage-needs)

### How Azure data storage can meet your business storage needs
- **Azure SQL Database**: Azure SQL Database is a relational database as a service (DaaS) based on the latest stable version of the Microsoft SQL Server database engine.
- **Azure Cosmos DB**: Azure Cosmos DB is a globally distributed database service. It supports schema-less data that lets you build highly responsive and Always On applications to support constantly changing data.
- **Azure Blob storage**: Azure Blob Storage is unstructured, meaning that there are no restrictions on the kinds of data it can hold. Blobs are highly scalable and apps work with blobs in much the same way as they would work with files on a disk, such as reading and writing data.
-**Azure Data Lake Storage**: The Data Lake feature allows you to perform analytics on your data usage and prepare reports. Data Lake is a large repository that stores both structured and unstructured data.
- **Azure Files**: Azure Files offers fully managed file shares in the cloud that are accessible via the industry standard Server Message Block (SMB) protocol.
- **Azure Queue**: Azure Queue storage is a service for storing large numbers of messages that can be accessed from anywhere in the world.
- **Disk Storage**: Disk storage provides disks for virtual machines, applications, and other services to access and use as they need, similar to how they would in on-premises scenarios.

### Storage tiers
- **Hot storage tier**: optimized for storing data that is accessed frequently.
- **Cool storage tier**: optimized for data that are infrequently accessed and stored for at least 30 days.
- **Archive storage tier**: for data that are rarely accessed and stored for at least 180 days with flexible latency requirements.

### Encryption for storage services
- Azure Storage Service Encryption (SSE)
- Client-side encryption

### Replication for storage availability
A replication type is set up when you create a storage account. The replication feature ensures that your data is durable and always available. Azure provides regional and geographic replications to protect your data against natural disasters and other local disasters like fire or flooding.

## [Comparison between Azure data storage and on-premises storage](https://docs.microsoft.com/en-us/learn/modules/intro-to-data-in-azure/4-comparison-azure-and-on-prem-storage)

- **Cost effectiveness**: An on-premises storage solution requires dedicated hardware and Azure data storage provides a pay-as-you-go pricing model.
- **Reliability**: On-premises storage requires data backup, load balancing, and disaster recovery strategies. Azure data storage provides data backup, load balancing, disaster recovery, and data replication as services to ensure data safety and high availability.
- **Storage types**: Sometimes multiple different storage types are required for a solution, such as file and database storage. Azure data storage provides a variety of different storage options including distributed access and tiered storage. 
- **Agility**: Requirements and technologies change. For an on-premises deployment, these changes may mean provisioning and deploying new servers and infrastructure pieces, which are a time consuming and expensive activity.
Azure data storage gives you the flexibility to create new services in minutes.

## [Check your knowledge](https://docs.microsoft.com/en-us/learn/modules/intro-to-data-in-azure/5-knowledge-check)

- **Suppose you work at a startup with limited funding. Why might you prefer Azure data storage over an on-premises solution?**
    - [ ] To ensure you run on a specific brand of hardware, which will let you form a marketing partnership with that hardware vendor.
    - [x] The Azure pay-as-you-go billing model lets you avoid buying expensive hardware.
    - [ ] To get exact control over the location of your data store.
- Which of the following situations would yield the most benefits from relocating an on-premises data store to Azure?
    - [x] Unpredictable storage demand that increases and decreases multiple times throughout the year.
    - [ ] Long-term, steady growth in storage demand.
    - [ ] Consistent, unchanging storage demand.
- A newly released mobile app using Azure data storage has just been mentioned by a celebrity on social media, seeing a huge spike in user volume. To meet the unexpected new user demand, what feature of pay-as-you-go storage will be most beneficial?
    - [x] The ability to provision and deploy new infrastructure quickly
    - [ ] The ability to predict the service costs in advance
    - [ ] The ability to meet compliance requirements for data storage

## [Summary](https://docs.microsoft.com/en-us/learn/modules/intro-to-data-in-azure/6-summary)

- Storage of both structured and unstructured data
- High security that supports global compliance standards
- Load balancing, high availability, and redundancy capabilities
- The ability to send large volumes of data directly to the browser using features such as Azure Blob storage

\
[![Core Cloud Services - Azure networking options](../images/next.png)](intro-to-azure-networking.md)