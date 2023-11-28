---
name: Azure AI Search On Your Data
description: Chat with your data using OpenAI and AI Search.
languages:
- bicep
- azdeveloper
products:
- azure-openai
- azure-cognitive-search
- azure-app-service
- azure
page_type: sample
urlFragment: azure--ai-search-on-your-data
---

# Azure AI Search On Your Data

> [!IMPORTANT]
> As of November 15, 2023, Azure Cognitive Search has been renamed to Azure AI Search.

### Project Setup

Open the project in your local VS Code using the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers):

1. Start Docker Desktop (install it if not already installed)
1. Open the project
1. In the VS Code window that opens, once the project files show up (this may take several minutes), open a terminal window
1. Run `azd auth login`
1. Now you can follow the instructions in [Deploying from scratch](#deploying-from-scratch) below

### Deploying from scratch

Execute the following command, if you don't have any pre-existing Azure services and want to start from a fresh deployment.

1. Run `azd up` - This will provision Azure resources and deploy this sample to those resources, including building the search index based on the files found in the `./data` folder.
    * **Important**: Beware that the resources created by this command will incur immediate costs, primarily from the AI Search resource. These resources may accrue costs even if you interrupt the command before it is fully executed. You can run `azd down` or delete the resources manually to avoid unnecessary spending.
    * You will be prompted to select two locations, one for the majority of resources and one for the OpenAI resource, which is currently a short list. That location list is based on the [OpenAI model availability table](https://learn.microsoft.com/azure/cognitive-services/openai/concepts/models#model-summary-table-and-region-availability) and may become outdated as availability changes.