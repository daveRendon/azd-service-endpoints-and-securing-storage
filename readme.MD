# Service Endpoints and Securing Storage. Part of the Az-500 - Lab 12

👉 https://blog.azinsider.net/working-with-service-endpoints-and-securing-storage-d781a2f4f4df?source=friends_link&sk=09d4fd371f3f819228eddec1163a9ef6


This scenario is aligned with the Az-500 path and focuses on the following tasks:
 - Create a storage endpoint so traffic destined to Azure Storage always stays within the Azure backbone network.
 - Configure the storage endpoint so only resources from a specific subnet can access the storage.
 - Confirm that resources outside of the specific subnet cannot access the storage.

This scenario can be deployed to Azure using the [Azure Developer CLI - AZD](https://learn.microsoft.com/en-us/azure/developer/azure-developer-cli/overview). 

💪 This template scenario is part of the larger **[Microsoft Trainer Demo Deploy Catalog](https://aka.ms/trainer-demo-deploy)**.

## ⬇️ Installation
- [Azure Developer CLI - AZD](https://learn.microsoft.com/en-us/azure/developer/azure-developer-cli/install-azd)
    - When installing AZD, the above the following tools will be installed on your machine as well, if not already installed:
        - [GitHub CLI](https://cli.github.com)
        - [Bicep CLI](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/install)
    - You need Owner or Contributor access permissions to an Azure Subscription to  deploy the scenario.

## 🚀 Deploying the scenario in 3 easy steps:

1. From within a new folder on your machine, run `azd init` to initialize the deployment.
```
azd init -t daverendon/azd-service-endpoints-and-securing-storage
```
2. Next, run `azd up` to trigger an actual deployment.
```
azd up
```
You will get prompted during the AZD deployment step for the location/region.

3. If you want to delete the scenario from your Azure subscription, use `azd down`
```
azd down --purge --force
```

⏩ Note: running `azd down` deletes the RG and Resources, but will keep the artifacts on your local machine.

## What is the demo scenario about?

- Use the [demo guide](https://github.com/daverendon/azd-service-endpoints-and-securing-storage/blob/main/demoguide/demoguide.md)

Your organization segments core IT apps and services (such as DNS and security services) from other parts of the business, including your manufacturing department. However, in some scenarios, apps and services in the core area need to communicate with apps and services in the manufacturing area. In this scenario, you configure connectivity between the segmented areas. This is a common scenario for separating production from development or separating one subsidiary from another.


## 💭 Feedback and Contributing
Feel free to create issues for bugs, suggestions or Fork and create a PR with new demo scenarios or optimizations to the templates. 
If you like the scenario, consider giving a GitHub ⭐
 

