![Exam AZ-900](../images/az900.png "Exam AZ-900")

# [Control and organize Azure resources with Azure Resource Manager](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/)

## [Introduction](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/1-introduction)

- Use resource groups to organize Azure resources
- Use tags to organize resources
- Apply policies to enforce standards in your Azure environments
- Use resource locks to protect critical Azure resources from accidental deletion

## [Principles of resource groups](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/2-principles-of-resource-groups)

### What are resource groups?
Resource groups are a fundamental element of the Azure platform. A resource group is a logical container for resources deployed on Azure.
- **Logical grouping**:
Resource groups exist to help manage and organize your Azure resources.
![Resource group](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/media/2-rg.png)
- **Life cycle**:
If you delete a resource group, all resources contained within are also deleted.
- **Authorization**:
Resource groups are also a scope for applying role-based access control (RBAC) permissions.
- **Authorization**:
Resource groups are also a scope for applying role-based access control (RBAC) permissions. By applying RBAC permissions to a resource group, you can ease administration and limit access to allow only what is needed.

### Create a Resource Group
- Azure portal
- Azure PowerShell
- Azure CLI
- Templates
- Azure SDKs (like .NET, Java)

### Explore a resource group and add a resource
When creating resources, you usually have the option to create a new resource group as an alternative to using an existing resource group. This simplifies the process a bit, but as you see in your new organization, can lead to resources spread across resource groups with little thought as to how to organize them.

### Use resource groups for organization
- **Consistent naming convention**:
You can start with using an understandable naming convention.
- **Organizing principles**:
Resource groups can be organized in a number of ways, let's take a look at a few examples.

![Resource Type](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/media/2-resource-type-rg.png)

![Environment](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/media/2-environment-rg.png)

![Department](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/media/2-department-rg.png)

![Environment and Department](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/media/2-env-dept-rg.png)

- **Organizing for authorization**:
Since resource groups are a scope of RBAC, you can organize resources by who needs to administer them.

- **Organizing for life cycle**:
If you delete a resource group, you delete all the resources in it.

- **Organizing for billing**:
Lastly, placing resources in the same resource group is a way to group them for usage in billing reports.

## [Use tagging to organize resources](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/3-use-tagging-to-organize-resources)

### What are tags?
Tags are name/value pairs of text data that you can apply to resources and resource groups. Tags allow you to associate custom details about your resource.

### Apply tags to resources
Not all resource types support tags, and tags can't be applied to classic resources.
![Tags](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/media/3-tags-displayed.png)

### Use tags for organization
You can retrieve all the resources in your subscription with a specific tag name or value. Tags enable you to retrieve related resources from different resource groups. This approach is helpful when you need to organize resources for billing or management.

## [Use policies to enforce standards](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/4-use-policies-to-enforce-standards)

### What is Azure Policy?
Azure Policy is a service you can use to create, assign, and manage policies. These policies can enforce these rules when resources are created, and can be evaluated against existing resources to give visibility into compliance.

### Create a policy
Policies can be created and assigned through the Azure portal, Azure PowerShell, or Azure CLI.
>Please note that the policy assignment may take up to 30 minutes to take effect. Because of this delay, in the following steps the policy validation may succeed but the deployment will still fail. If this happens, allow for additional time and retry your deployment.

### Use policies to enforce standards
You've seen how you could use policies to ensure that our resources have the tags that organize our resources. There are other ways policies can be used to our benefit.

## [Secure resources with role-based access control](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/5-role-based-access)

RBAC provides fine-grained access management for Azure resources, enabling you to grant users the specific rights they need to perform their jobs. RBAC is considered a core service and is included with all subscription levels at no cost.

Using RBAC, you can:
- Allow one user to manage VMs in a subscription, and another user to manage virtual networks.
- Allow a database administrator (DBA) group to manage SQL databases in a subscription.
- Allow a user to manage all resources in a resource group, such as VMs, websites, and virtual subnets.
- Allow an application to access all resources in a resource group.

### How RBAC defines access
RBAC uses an allow model for access. When you are assigned to a role, RBAC allows you to perform specific actions, such as read, write, or delete. Therefore, if one role assignment grants you read permissions to a resource group, and a different role assignment grants you write permissions to the same resource group, you will have both read and write permissions on that resource group.

### Best Practices for RBAC
- Segregate duties within your team and grant only the amount of access to users that they need to perform their jobs. Instead of giving everybody unrestricted permissions in your Azure subscription or resources, allow only specific actions at a particular scope.
- When planning your access control strategy, grant users the lowest privilege level that they need to do their work.
- Use **Resource Locks** to ensure critical resources aren't modified or deleted (as you'll see in the next unit).

## [Use resource locks to protect resources](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/6-use-resource-locks-to-protect-resources)

### What are resource locks?
Resource locks are a setting that can be applied to any resource to block modification or deletion. Resource locks can set to either **Delete** or **Read-only**.
- **Delete** will allow all operations against the resource but block the ability to delete it.
- **Read-only** will only allow read activities to be performed against it, blocking any modification or deletion of the resource.

Resource locks can be applied to subscriptions, resource groups, and to individual resources, and are inherited when applied at higher levels.

## [Check your Knowledge](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/7-quiz)

- **Tags can be applied to any type of resource on Azure**
    - [ ] True
    - [x] False
- **Tags applied at a resource group level are propagated to resources within the resource group.**
    - [ ] True
    - [x] False
- **Which of the following features does not apply to resource groups?**
    - [ ] Resources can be in only one resource group.
    - [ ] Resources can be moved from one resource group to another resource group.
    - [x] Resource groups can be nested.
    - [ ] Role-based access control can be applied to the resource group.
- **Which of the following approaches might be a good usage of tags?**
    - [ ] Using tags to associate a cost center with resources for internal chargeback
    - [ ] Using tags in conjunction with Azure Automation to schedule maintenance windows
    - [ ] Using tags to store environment and department association
    - [x] All of the above are good ways to use tags
- **Which of the following approaches would be the most efficient way to ensure a naming convention was followed across your subscription?**
    - [ ] Send out an email with the details of your naming conventions and hope it is followed
    - [x] Create a policy with your naming requirements and assign it to the scope of your subscription
    - [ ] Give all other users except for yourself read-only access to the subscription. Have all requests to create resources sent to you so you can review the names being assigned to resources, and then create them.
- **Which of the following items would be good use of a resource lock?**
    - [x] An ExpressRoute circuit with connectivity back to your on-premises network
    - [ ] A non-production virtual machine used to test occasional application builds
    - [ ] A storage account used to temporarily store images processed in a development environment

## [Summary](https://docs.microsoft.com/en-us/learn/modules/control-and-organize-with-azure-resource-manager/8-summary)

- We've taken a look at several features you can use to put organization and control around your Azure resources.
- We talked about how resource groups worked, and some ways you can use them to organize your resources.
- We looked at how tags allow you to add custom contextual information to your resources, for use in areas such as billing and filtering.
- We saw how we could use policies to enforce standards across our Azure resources.
- We used resource locks to prevent accidental deletion of critical resources.

\
[![Predict costs and optimize spending for Azure](../images/next.png)](predict-costs-and-optimize-spending.md)
