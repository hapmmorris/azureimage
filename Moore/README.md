# Azure Marketplace VM with CreateUIDefinition

[![Deploy to Azure](https://aka.ms/deploytoazurebutton?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhapmmorris%2Fazureimage%2Fmaster%2FMoore%2Fazuredeploy.json/uiFormDefinitionUri/https%3A%2F%2Fraw.githubusercontent.com%2Fhapmmorris%2Fazureimage%2Fmaster%2FMoore%2FuiFormDefinition.json)

This template allows deploying a linux VM using new or existing resources for the Virtual Network, Storage and Public IP Address.  It also allows for choosing between SSH and Password authentication.  The templates uses conditions and logic functions to remove the need for nested deployments.

This template contains extra parameters to allow for the existing resources use cases, which is a common scenario for Azure Applications in the Azure Marketplace.

createUiDefinition.json is also included.

Before submitting to Marketplace, the following steps will need to be performed

- Rename ```azuredeploy.json``` to ```mainTemplate.json```
- Remove ```azuredeploy.parameters.json``` from the list of files to be submitted
- Update the GUID in ```mainTemplate.json``` for Customer Usage Attribution
  - https://docs.microsoft.com/en-us/azure/marketplace/marketplace-solution-templates
- Create a zip package of all the dependencies including the templates files, scripts, UI definition etc
  - https://docs.microsoft.com/en-us/azure/marketplace/cloud-partner-portal/azure-applications/cpp-skus-tab#package-details-for-solution-template 
  
  `Tags: new, exiting, resource, vm, condition, conditional`
