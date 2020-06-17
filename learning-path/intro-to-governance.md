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

![Policy portal](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/media/2-policy-portal.png)

### Removing a policy definition
Finally, you can delete policy requirements through the portal, or through the PowerShell command *Remove-AzPolicyAssignment* as shown below.

```powershell
Remove-AzPolicyAssignment -Name 'audit-vm-manageddisks' -Scope '/subscriptions/<subscriptionID>/resourceGroups/<resourceGroupName>'
```

## [Organize policy with initiatives](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/3-initiatives)



## []()



## []()



## []()



## []()



## [Summary]()



\
[![](../images/next.png)](.md)