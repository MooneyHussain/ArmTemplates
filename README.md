# ARM Templates 

## Description
A useful collection of ARM templates that I intially (found tricky) to deploy

## Deployment 
Easiest form is to use [Powershell](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-template-deploy) for the official documentation. 

``` powershell 
Connect-AzAccount 

Select-AzSubscription -SubscriptionName <yourSubscriptionName> 

New-AzResourceGroup -Name ExampleResourceGroup -Location "UK South" 

New-AzResourceGroupDeployment -Name ExampleDeployment -ResourceGroupName ExampleResourceGroup `
  -TemplateFile c:\MyTemplates\storage.json `
  -TemplateParameterFile c:\MyTemplates\storage.parameters.json

# Not all the commands are mandatory. 
# You may not need `Select-AzSubscription` or `New-AzResourceGroup` 
```
#### Note 
To use the above script you need the latest azure module. To get this open powershell as an administrator and run `Install-Module Az`.
