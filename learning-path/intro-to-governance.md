![Exam AZ-900](../images/az900.png "Exam AZ-900")

# [Apply and monitor infrastructure standards with Azure Policy](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/)

## [Introduction](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/1-introduction)

You need good governance when:
- You have multiple engineering teams working in Azure
- You have multiple subscriptions in your tenant
- You have regulatory requirements that must be enforced
- You want to ensure standards are followed for all IT allocated resources

In this module, you will:
- Apply policies to control and audit resource creation
- Learn how role-based security can fine-tune access to your resources
- Understand Microsoft's policies and privacy guarantees
- Learn how to monitor your resources

## [Define IT compliance with Azure Policy](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/2-azure-policy)

**Azure Policy** is an Azure service you use to create, assign and, manage policies. These policies enforce different rules and effects over your resources so that those resources stay compliant with your corporate standards and service level agreements.

### What is a policy definition?
A policy definition expresses what to evaluate and what action to take. For example, you could ensure all public websites are secured with HTTPS, prevent a particular storage type from being created, or force a specific version of SQL Server to be used.

### Applying Azure policy
To apply a policy, we can use the Azure portal, or one of the command-line tools such as Azure PowerShell by adding the *Microsoft.PolicyInsights* extension.

### Identifying non-compliant resources
We can use the applied policy definition to identify resources that aren't compliant with the policy assignment through the Azure portal.

![Policy Compliance](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/media/2-policy-compliance.png)

### Assign a definition to a scope of resources
Once you've defined one or more policy definitions, you'll need to assign them. A policy assignment is a policy definition that has been assigned to take place within a specific scope.
This scope could range from a full subscription down to a resource group.

### Policy effects
Requests to create or update a resource through Azure Resource Manager are evaluated by Azure Policy first. Policy creates a list of all assignments that apply to the resource and then evaluates the resource against each definition.

| Policy Effect | What happens? |
| - | - |
| Deny | The resource creation/update fails due to policy. |
| Disabled | The policy rule is ignored (disabled). Often used for testing. |
| Append | Adds additional parameters/fields to the requested resource during creation or update. A common example is adding tags on resources such as Cost Center or specifying allowed IPs for a storage resource. |
| Audit, AuditIfNotExists | Creates a warning event in the activity log when evaluating a non-compliant resource, but it doesn't stop the request. |
| DeployIfNotExists | Executes a template deployment when a specific condition is met. For example, if SQL encryption is enabled on a database, then it can run a template after the DB is created to set it up a specific way. |

### View policy evaluation results

![Policy Portal](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/media/2-policy-portal.png)

### Removing a policy definition
Finally, you can delete policy requirements through the portal, or through the PowerShell command *Remove-AzPolicyAssignment* as shown below.

```powershell
Remove-AzPolicyAssignment -Name 'audit-vm-manageddisks' -Scope '/subscriptions/<subscriptionID>/resourceGroups/<resourceGroupName>'
```

## [Organize policy with initiatives](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/3-initiatives)

### Defining initiatives
Initiative definitions simplify the process of managing and assigning policy definitions by grouping a set of policies into a single item. For example, you could create an initiative named Enable Monitoring in Azure Security Center, with a goal to monitor all the available security recommendations in your Azure Security Center.

![Define Initiatives](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/media/3-define-initiatives.png)

## [Enterprise governance management](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/4-management-groups)

**Azure Management Groups** are containers for managing access, policies, and compliance across multiple Azure subscriptions.

![Management Groups Tree](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/media/4-management-groups-tree.png)

You can manage your Azure subscriptions more effectively by using Azure Policy and Azure role-based access controls (RBACs). These provide distinct governance conditions that you can apply to each management group. The resources and subscriptions you assign to a management group automatically inherit the conditions that you apply to that management group.

## [Define standard resources with Azure Blueprints](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/5-azure-blueprints)

To help you with auditing, traceability, and compliance of your deployments, use **Azure Blueprint** artifacts and tools.

Azure Blueprints is a declarative way to orchestrate the deployment of various resource templates and other artifacts, such as:
- Role assignments
- Policy assignments
- Azure Resource Manager templates
- Resource groups

### How is it different from Resource Manager templates?
The Azure Blueprints service is designed to help with environment setup. This setup often consists of a set of resource groups, policies, role assignments, and Resource Manager template deployments. A blueprint is a package to bring each of these artifact types together and allow you to compose and version that package—including through a CI/CD pipeline.

Nearly everything that you want to include for deployment in Blueprints can be accomplished with a Resource Manager template. However, a Resource Manager template is a document that doesn't exist natively in Azure. Resource Manager templates are stored either locally or in source control. The template gets used for deployments of one or more Azure resources, but once those resources deploy there's no active connection or relationship to the template.

### How it's different from Azure Policy
A blueprint is a package or container for composing focus-specific sets of standards, patterns, and requirements related to the implementation of Azure cloud services, security, and design that can be reused to maintain consistency and compliance.
A policy is a default-allow and explicit-deny system focused on resource properties during deployment and for already existing resources. It supports cloud governance by validating that resources within a subscription adhere to requirements and standards.

A policy can be included as one of many artifacts in a blueprint definition. Blueprints also support using parameters with policies and initiatives.

## [Explore your service compliance with Compliance Manager](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/6-azure-compliance)

### Microsoft Privacy Statement
The **Microsoft privacy statement** explains what personal data Microsoft processes, how Microsoft processes it, and for what purposes.

### What is the Microsoft Trust Center?
**Trust Center** is a website resource containing information and details about how Microsoft implements and supports security, privacy, compliance, and transparency in all Microsoft cloud products and services.

### What is the Service Trust Portal?
The **Service Trust Portal** (STP) hosts the Compliance Manager service, and is the Microsoft public site for publishing audit reports and other compliance-related information relevant to Microsoft's cloud services. STP users can download audit reports produced by external auditors and gain insight from Microsoft-authored reports that provide details on how Microsoft builds and operates its cloud services.

### Compliance Manager
**Compliance Manager** is a workflow-based risk assessment dashboard within the Service Trust Portal that enables you to track, assign, and verify your organization's regulatory compliance activities related to Microsoft professional services and Microsoft cloud services such as Office 365, Dynamics 365, and Azure.

![Compliance Manager](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/media/6-compliancemanager.png)

>Compliance Manager is a dashboard that provides a summary of your data protection and compliance stature and recommendations for improvement. The Customer Actions provided in Compliance Manager are recommendations only; it is up to each organization to evaluate the effectiveness of these recommendations in their respective regulatory environment prior to implementation. Recommendations found in Compliance Manager should not be interpreted as a guarantee of compliance.

## [Monitor your service health](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/7-monitoring)

### Azure Monitor
**Azure Monitor** maximizes the availability and performance of your applications by delivering a comprehensive solution for collecting, analyzing, and acting on telemetry from your cloud and on-premises environments. It helps you understand how your applications are performing and proactively identifies issues affecting them and the resources they depend on.

#### Data sources
- Application monitoring data
- Guest OS monitoring data
- Azure resource monitoring data
- Azure subscription monitoring data
- Azure tenant monitoring data

#### Diagnostic settings
- Enable guest-level monitoring
- Performance counters: collect performance data
- Event Logs: enable various event logs
- Crash Dumps: enable or disable
- Sinks: send your diagnostic data to other services for more analysis
- Agent: configure agent settings

#### Getting more data from your apps
- Application Insights
- Azure Monitor
- Azure Monitor for VMs

#### Responding to alert conditions
**Alerts**. Azure Monitor proactively notifies you of critical conditions using alerts, and can potentially attempt to take corrective actions. Alert rules based on metrics can provide alerts in almost real-time, based on numeric values. Alert rules based on logs allow for complex logic across data, from multiple sources.

**Autoscale**. Azure Monitor uses Autoscale to ensure that you have the right amount of resources running to manage the load on your application effectively. Autoscale enables you to create rules that use metrics, collected by Azure Monitor, to determine when to automatically add resources to handle increases in load. Autoscale can also help reduce your Azure costs by removing resources that are not being used. You can specify a minimum and maximum number of instances, and provide the logic that determines when Autoscale should increase or decrease resources.

#### Visualize monitoring data
- Dashboards
- Views
- Power BI

#### Integrate with other services
You'll often need to integrate Azure Monitor with other systems, and build customized solutions that use your monitoring data. Other Azure services can work with Azure Monitor to provide this integration.

### Azure Service Health
**Azure Service Health** is a suite of experiences that provide personalized guidance and support when issues with Azure services affect you.
- **Azure Status** provides a global view of the health state of Azure services.
- **Service Health** provides you with a customizable dashboard that tracks the state of your Azure services in the regions where you use them. In this dashboard, you can track active events such as ongoing service issues, upcoming planned maintenance, or relevant Health advisories.
- **Resource Health** helps you diagnose and obtain support when an Azure service issue affects your resources. It provides you with details about the current and past state of your resources. It also provides technical support to help you mitigate problems.

## [Summary](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/8-summary)

### Check your knowledge
- **True or false: You can download published audit reports and other compliance-related information related to Microsoft’s cloud service from the Service Trust Portal**
    - [x] True
    - [ ] False
- **Which Azure service allows you to configure fine-grained access management for Azure resources, enabling you to grant users only the rights they need to perform their jobs?**
    - [ ] Locks
    - [ ] Policy
    - [ ] Initiatives
    - [x] Role-based Access Control
- **Which Azure service allows you to create, assign, and, manage policies to enforce different rules and effects over your resources and stay compliant with your corporate standards and service-level agreements (SLAs)?**
    - [x] Azure Policy
    - [ ] Azure Blueprints
    - [ ] Azure Security Center
    - [ ] Role-based Access Control
- **Which of the following services provides up-to-date status information about the health of Azure services?**
    - [ ] Compliance Manager
    - [ ] Azure Monitor
    - [ ] Service Trust Portal
    - [x] Azure Service Health
- **Where can you obtain details about the personal data Microsoft processes, how Microsoft processes it, and for what purposes?**
    - [x] Microsoft Privacy Statement
    - [ ] Compliance Manager
    - [ ] Azure Service Health
    - [ ] Trust Center

\
[![Control and organize Azure resources with Azure Resource Manager](../images/next.png)](control-and-organize-with-azure-resource-manager.md)